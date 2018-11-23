---
layout: page
---
### Python Scripting in Abaqus
### Editing the Input File to get Matrix Outputs
Get Mass and Stiffness Matrices from Abaqus 
Edit Keyword Block
```python
mdb.models['__ModelName__'].keywordBlock.synchVersions(storeNodesAndElements=False)
```
Replace a Line in the Keyword Block 
```python
mdb.models['__ModelName__'].keywordBlock.replace(26, """
** ----------------------------------------------------------------
* Step, name=exportmatrix
# Generate Mass and Stiffness Matrices
*matrix generate, mass, stiffness
# Format can be changed. matrix input outputs the matrices as sparse matrices and the file extension is .mtx
*matrix output, mass, stiffness, format=matrix input
*end step
**""")
```
