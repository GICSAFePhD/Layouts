# Source-code

<table bakground="FFF">
<tr> <td><b>Part</b></td> <td><b>Description</b></td> <td><b>Repository URL</b></td> </tr>
<!-- Pegar tabla de excel inicio -->

<tr><td rowspan="1" align="center">APP</td>
<td>Run Main.py to use the full tool</td><td><a href="https://github.com/GICSAFePhD/App">Link</a></td></tr>
  
<tr><td rowspan="1" align="center">RNA</td>
<td>Railway Network Analyzer</td><td><a href="https://github.com/GICSAFePhD/RNA">Link</a></td></tr>
 
<tr><td rowspan="1" align="center">ACG</td>
<td>Automatic Code Generator (under repairment)</td><td><a href="https://github.com/GICSAFePhD/ACG">Link</a></td></tr>
  
<tr><td rowspan="1" align="center">AGG</td>
<td>Automatic Graphic Generator (to be implemented)</td><td><a href="https://github.com/GICSAFePhD/AGG">Link</a></td></tr>
  
<tr><td rowspan="1" align="center">ATA</td>
<td>Automatic Test Analyzer (to be implemented)</td><td><a href="https://github.com/GICSAFePhD/ATA">Link</a></td></tr>
  
<tr><td rowspan="1" align="center">ATG</td>
<td>Automatic Test Generator (to be implemented)</td><td><a href="https://github.com/GICSAFePhD/ATG">Link</a></td></tr>
  
<tr><td rowspan="1" align="center">railML</td>
<td>railML library</td><td><a href="https://github.com/GICSAFePhD/railML">Link</a></td></tr>
 
<tr><td rowspan="1" align="center">Layouts</td>
<td>Examples</td><td><a href="https://github.com/GICSAFePhD/Layouts">Link</a></td></tr>  

<!-- Pegar tabla de excel fin -->
</table>

## Usage

1. Download the seven folders
2. In APP/main.py edit INPUT_FILE and OUTPUT_FILE
* OUTPUT_FILE can be any name with extension .railml
* INPUT_FILE must exists in \Layouts as a .railml file

```python
i = 10
INPUT_FILE  = "C:\PhD\RailML\Layouts\Example_"+str(i)+".railml"
OUTPUT_FILE = "C:\PhD\RailML\Layouts\Example_"+str(i)+"_B.railml"
```
index i was used to select examples, but any name can be used instead, if it exists in \Layouts

3. Set up configuration

* Function move_signals can be enabled (to avoid signal overlapping) or disabled (to allow signal overllaping).
```python
move_signals(signals,nodes,TRUE / FALSE)
```
* The distance to avoid overllaping is set as 90
```python
move_step = 90
```
* Function reduce_signals can be commented to enable / disable signalling simplification.(to avoid signal overlapping) or disabled (to allow signal overllaping)
```python
reduce_signals(signals,signal_placement)
```
* The distance for horizontal inheritance can be set in 
```python
def signal_simplification_by_proximity(signal_placement,crossing_nodes,platforms_node):
    distance = 300
    ...
```
* The distance for CDL zones can be set in 
```python
def find_signal_positions(nodes,netPaths,switchesIS,tracks,trainDetectionElements,bufferStops,levelCrossingsIS,platforms):
    signal_placement = {}
    step = 200
    ...
```
* The distance for every rail element can be set in their respective functions

```python
def find_signals_lineborders(netPaths,nodes,borders,signals):
    step = 100
    ...
```
```python
def find_signals_bufferStops(netPaths,nodes,bufferStops,signals):
    step = 100
    ...
```
```python
def find_signals_joints(signal_placement,nodes,netPaths,trainDetectionElements,signals):
    distance = 200
    ...
```
```python
def find_signals_platforms(signal_placement,nodes,netPaths,platforms,signals):
    distance = 300
    ...
```
```python
def find_signals_crossings(signal_placement,nodes,netPaths,levelCrossingsIS,signals):
    distance = 250
    ...
```
Switches cannot be configured, they use the CDL configuration.

# Directory

<table bakground="FFF">
<tr> <td><b>Example</b></td> <td><b>Section</b></td> <td><b>Repository URL</b></td> </tr>
<!-- Pegar tabla de excel inicio -->

  
<tr><td rowspan="4" align="center">1</td>
<td>Description</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_1/Readme.md#description">Link</a></td></tr>
<tr><td>Step by step</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_1/Readme.md#step-by-step">Link</a></td></tr>
<tr><td>Original table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_1/Readme.md#original-table">Link</a></td></tr>
<tr><td>Generated table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_1/Readme.md#generated-table">Link</a></td></tr>

<tr><td rowspan="4" align="center">2</td>
<td>Description</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_2/Readme.md#description">Link</a></td></tr>
<tr><td>Step by step</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_2/Readme.md#step-by-step">Link</a></td></tr>
<tr><td>Original table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_2/Readme.md#original-table">Link</a></td></tr>
<tr><td>Generated table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_2/Readme.md#generated-table">Link</a></td></tr>
  
<tr><td rowspan="4" align="center">3</td>
<td>Description</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_3/Readme.md#description">Link</a></td></tr>
<tr><td>Step by step</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_3/Readme.md#step-by-step">Link</a></td></tr>
<tr><td>Original table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_3/Readme.md#original-table">Link</a></td></tr>
<tr><td>Generated table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_3/Readme.md#generated-table">Link</a></td></tr>
  
<tr><td rowspan="4" align="center">4</td>
<td>Description</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_4/Readme.md#description">Link</a></td></tr>
<tr><td>Step by step</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_4/Readme.md#step-by-step">Link</a></td></tr>
<tr><td>Original table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_4/Readme.md#original-table">Link</a></td></tr>
<tr><td>Generated table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_4/Readme.md#generated-table">Link</a></td></tr>

<tr><td rowspan="4" align="center">5</td>
<td>Description</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_5/Readme.md#description">Link</a></td></tr>
<tr><td>Step by step</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_5/Readme.md#step-by-step">Link</a></td></tr>
<tr><td>Original table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_5/Readme.md#original-table">Link</a></td></tr>
<tr><td>Generated table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_5/Readme.md#generated-table">Link</a></td></tr>
  
<tr><td rowspan="4" align="center">6</td>
<td>Description</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_6/Readme.md#description">Link</a></td></tr>
<tr><td>Step by step</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_6/Readme.md#step-by-step">Link</a></td></tr>
<tr><td>Original table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_6/Readme.md#original-table">Link</a></td></tr>
<tr><td>Generated table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_6/Readme.md#generated-table">Link</a></td></tr>
  
<tr><td rowspan="4" align="center">7</td>
<td>Description</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_7/Readme.md#description">Link</a></td></tr>
<tr><td>Step by step</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_7/Readme.md#step-by-step">Link</a></td></tr>
<tr><td>Original table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_7/Readme.md#original-table">Link</a></td></tr>
<tr><td>Generated table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_7/Readme.md#generated-table">Link</a></td></tr>
  
<tr><td rowspan="4" align="center">8</td>
<td>Description</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_8/Readme.md#description">Link</a></td></tr>
<tr><td>Step by step</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_8/Readme.md#step-by-step">Link</a></td></tr>
<tr><td>Original table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_8/Readme.md#original-table">Link</a></td></tr>
<tr><td>Generated table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_8/Readme.md#generated-table">Link</a></td></tr>
  
<tr><td rowspan="4" align="center">9</td>
<td>Description</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_9/Readme.md#description">Link</a></td></tr>
<tr><td>Step by step</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_9/Readme.md#step-by-step">Link</a></td></tr>
<tr><td>Original table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_9/Readme.md#original-table">Link</a></td></tr>
<tr><td>Generated table</td><td><a href="https://github.com/GICSAFePhD/RailML/tree/main/Layouts/Example_9/Readme.md#generated-table">Link</a></td></tr>
<!-- Pegar tabla de excel fin -->
</table>
