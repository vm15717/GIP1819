---
layout: page
---
## Abaqus Macros
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
```python
odbName='__JobName__'
odb=openOdb(odbName+'.odb',readOnly=True)
step1=odb.steps['__StepName__']
frame=step1.frames['__FrameNumber__']
#Field Outputs 'U' - Displacement 'RF' - Reaction Forces 'S' - Stress Output etc..
displ=frame.fieldOutputs['__FieldOutputKey__']
displvalues=displ.values
```
