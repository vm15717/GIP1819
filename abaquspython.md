---
layout: page
---
## Abaqus Macros
### Python Scripting in Abaqus
### Inputting Forces into Abaqus
Steps:  
1.Create a Static Step  
```python
mdb.models['__ModelName__'].StaticStep(name='__StepName__', previous='__PreviousStepName__')   
#Get Nodes from the Instance
instanceNodes = mdb.models['__ModelName__'].rootAssembly.instances['__InstanceName__'].nodes
print s
```
2.Create a NodeSet and Nodelabel  
3.Create a region using the nodeset   
4.Apply forces to nodes  

