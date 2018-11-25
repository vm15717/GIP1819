---
layout: page
---
### Python Scripting in Abaqus
### Reading Field Outputs from Abaqus  
Necessary Imports
```python
from abaqusConstants import *
from odbAccess import *
from textRepr import *
import numpy as np
#If you want to output results in a CSV format
import csv 
```
Reading Outputs from Odb file
```python
odbName='__JobName__'
odb=openOdb(odbName+'.odb',readOnly=True)
step1=odb.steps['__StepName__']
frame=step1.frames['__FrameNumber__']
#Field Outputs 'U' - Displacement 'RF' - Reaction Forces 'S' - Stress Output etc..
output=frame.fieldOutputs['__FieldOutputKey__']
outputvalues=output.values
```
Example:  
Getting Displacements Out
```python
output=frame.fieldOutputs['U']  
outputvalues=output.values
```
Matrix of displacement Values 
```python
#Create a Matrix of Zeros with 3 columns.
dispres=np.zeros(shape=[len(outputvalues),3])
for k in range(len(outputvalues)):
    dispres[k]=np.array(outputvalues[k].data,dtype='object')
header2=np.array(['U1','U2','U3'],dtype=object)
dispres=np.vstack((header2,dispres))
```
Write the Output to a CSV file
```python
with open('results1.csv','wb') as csvfile:
    filewriter=csv.writer(csvfile, delimiter=',',quotechar='|',quoting=csv.QUOTE_MINIMAL)
    for i in range(len(dispres)):
       filewriter.writerow(dispres[i])
```
