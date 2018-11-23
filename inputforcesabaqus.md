---
layout: page
---
## Python Scripting in Abaqus
### Input Forces into Abaqus
Steps:  
1.Create a Static Step  
```python
mdb.models['__ModelName__'].StaticStep(name='__StepName__', previous='__PreviousStepName__')   
```
2.Create a NodeSet and Nodelabel or Extract Nodes from Existing Instance
```python
#Get Nodes from the Instance
instanceNodes = mdb.models['__ModelName__'].rootAssembly.instances['__InstanceName__'].nodes
```
3.Import Forces
```python
#Import Forces from a CSV file (if available)
file=csv.reader(open('filename','r'))
n=[]
for row in file:
        n.append(row)
```
4.Apply forces to each node
```python
#Loop through each node label to apply force to each node
for i in range(0,len(n)):
        nodeLabel=[i]
        #Apply the three components of forces to each node
        [cf11,cf22,cf33]=map(float,n[i])
        #Create a mesh node object for each node label
        meshNodeObj = instanceNodes.sequenceFromLabels(nodeLabel)
        #Create a region using the mesh node object. Do not forget to import regionToolSet at the start
        myRegion = regionToolset.Region(nodes=meshNodeObj)
        #Apply forces
        mdb.models['__ModelName'].ConcentratedForce(name='__LoadName__', createStepName='__StepName__', 
           region=myRegion, cf1=cf11, cf2=cf22, cf3=cf33, distributionType=UNIFORM, field='', 
           localCsys=None)
```   

