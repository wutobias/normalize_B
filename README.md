# normalize_B
This is a python script for normalizing B factors in a PDB file. 

What is it doing?
=================
The normalization factor for each individual atom is calculated as the average B factor of all atoms within a given radius. The python script spits out two pdb files (PREFIX is the prefix of your pdb file):
1) PREFIX_norm.pdb: A pdb file containing only normalized B factors
2) PREFIX_std.pdb:  A pdb file containing B factors reported as the normalized difference to the mean. Here, the normalization comes from the standard deviation of the b factors of all atoms within a given radius. This can be understood of the B factor reported as a Standard score (see https://en.wikipedia.org/wiki/Standard_score)

Usage
=====
```
python normalize_B.py <PREFIX.pdb> <radius>
```

**PREFIX.pdb** 
Your query pdb file
**radius** 
The radius (in Angstrom) that is used for searching atoms that are used for the B factor normalization

Dependencies
============
* parmed
* numpy
* scipy

Contact
=======
tobias.wulsdorf@gmail.com
