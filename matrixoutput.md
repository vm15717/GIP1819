---
layout: page
---
### Python Scripting in Abaqus
### Editing the Input File to get Matrix Outputs
```python
mdb.models['Model-1'].keywordBlock.synchVersions(storeNodesAndElements=False)
mdb.models['Model-1'].keywordBlock.replace(26, """
** ----------------------------------------------------------------
* Step, name=exportmatrix
*matrix generate, mass, stiffness
*matrix output, mass, stiffness, format=matrix input
*end step
**""")
```
