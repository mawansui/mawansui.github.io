---
permalink: /hacks/
title: "Quick Hacks"
excerpt: "This is a collection of quick hacks that I find/come up with when working on a multitude of unrelated tasks."
author_profile: true
---

This is a collection of quick hacks that I find/come up with when working on a multitude of unrelated tasks. Intended for quick lookup. Search this page by keyword to find relevant notes. For mode detail on any of the Quick Hacks published here, please visit [my blog on Medium](https://medium.com/chemoinformatics), where I explain the meaning behind the commands and the code.

---

**Q**: How to calculate the number of molecules in an `.sdf` file from the command line?  
**A**: `fgrep -c '$$$$' <sdfile>` or `fgrep -c "M END" <sdfile>`  
**Tags**: linux, sdf

---

**Q**: How to calculate the number of molecules in a `.mol2` file from the command line?  
**A**: `fgrep -c "@<TRIPOS>ATOM" <mol2file>`  
**Tags**: linux, mol2

---

**Q**: How to unite (concatenate) several `.sdf` files into a single file using only the command line?   
**A**: `cat *.sdf > new_file.sdf`   
**Tags**: linux, sdf

---

**Q**: How to quickly convert SDF to SMILES using `Babel`?  
**A**: `babel -isdf YOURFILE.sdf -osmi YOURNEWFILE.smi`  
> You can provide the paths without parentheses.

**Tags**: babel

---

**Q**: How to quickly convert SDF to SMILES using `molconvert`?   
**A**: `molconvert smiles input.sdf -o output.smiles`  
**Tags**: molconvert

---

**Q**: How to quickly learn how many molecules does a `.smi` file contain?  
> Usually, the `.smi` files contain one SMILES string per line, so you can just count the number of lines in the file: 

**A**: `wc -l input.smi`  
**Tags**: linux

---

**Q**: How to read molecules from SMILES and render them in Jupyter Notebook?  
**A**:  

```python
from rdkit import Chem
m = Chem.MolFromSmiles("c1ccccc1OC")
```  

**Tags**: rdkit, jupyter

---

**Q**: How to make a SMILES string out of an RDKit molecule object?  
**A**:

```python
smiles_string = Chem.MolToSmiles(m, isomericSmiles = True)
```
  
**Tags**: rdkit, jupyter

---

**Q**: How to make molecules draw inline in Jupyer Notebook?  
**A**: 

```python
from rdkit import Chem
from rdkit.Chem.Draw import IPythonConsole
from rdkit.Chem import Draw
IPythonConsole.ipython_useSVG=True
```
  After running this, molecules will draw inline.
  
**Tags**: rdkit, jupyter

---

**Q**: How to list all files in a directory in such a way to see the creation date?  
**A**: `ls -ltr`  
**Tags**: linux

---

**Q**: How to read an `.sdf` file in RDKit?   
**A**:

```python
iterator = Chem.SDMolSupplier("your_sdf_file.sdf")
mols = [m for m in iterator if m is not None]
```
  
**Tags**: rdkit, jupyter

---

**Q**: How to color only specific chains in a specific color using ChimeraX?  
**A**: You can either use `color /<CHAIN LETTER> color name` or `color :<RESIDUE_NAME> color name`. Please consult the list of all available colors [here](https://www.rbvi.ucsf.edu/chimerax/docs/user/commands/colornames.html#builtin).  
**Tags**: chimerax, graphics

---

**Q**: How to download and open a PDB structure from ChimeraX?  
**A**: `open pdb:4tv9`.  
**Tags**: chimerax, graphics, pdb

---

**Q**: How to download and open a PDB structure from PyMOL?  
**A**: `fetch 4tv8`.  
**Tags**: pymol, graphics, pdb

---

**Q**: How to color a single ligand in ChimeraX in nice-looking colors by element?  
**A**: `color :3GT byelement`, where `3GT` is the residue code.  
**Tags**: chimerax, graphics

---

**Q**: How to calculate 3D-conformations for a molecule in RDKit and then calculate 3D descriptors for each conformer?  
**A**:

```python
from rdkit import Chem
from rdkit.Chem import AllChem
from rdkit.Chem import Descriptors3D

m = Chem.MolFromSmiles("CCCOC")
m = Chem.AddHs(m)
AllChem.EmbedMolecule(m)
AllChem.UFFOptimizeMolecule(m)
cids = AllChem.EmbedMultipleConfs(m, numConfs=10, pruneRmsThresh=1)
for cid in cids:
    AllChem.MMFFOptimizeMolecule(m, confId = cid)
    
    # you can either do:
    Descriptors3D.Asphericity(m, confId=cid)
    
    # or:
    Chem.rdMolDescriptors.CalcMORSE(m, confId = cid)
```
  Please check the list of all available 3D RDKit descriptors and their calculation methods [here](https://www.rdkit.org/docs/source/rdkit.Chem.rdMolDescriptors.html).  
  **Tags**: rdkit, descriptors

---

**Q**: How to unzip a `.tar.gz` archive in Linux?  
**A**: `tar -xzf yourfile.tar.gz`  
**Tags**: linux

---

**Q**: How to unzip a `.gz` archive in Linux?   
**A**: `gunzip yourfile.gz`  
**Tags**: linux

---

**Q**:  
**A**:  
**Tags**:

---
