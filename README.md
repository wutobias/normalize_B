What is it doing?
=================
This is a python script for normalizing B factors in a PDB file. Each atom is normalized individually based on the average B factor of all atoms within a given radius. For the normalization, only non-hydrogen atoms are evaluated.

The python script spits out two pdb files (PREFIX is the prefix of your pdb file):
1) PREFIX_norm.pdb: A pdb file containing only normalized B factors
2) PREFIX_std.pdb:  A pdb file containing B factors reported as the normalized difference to the mean. Here, the normalization comes from the standard deviation of the b factors of all atoms within a given radius. This can be understood of the B factor reported as a Standard score (see https://en.wikipedia.org/wiki/Standard_score)

Usage
=====
```
python normalize_B.py <PREFIX.pdb> <radius>
```

**PREFIX.pdb**
This is your query pdb file.

**radius**
This is the radius (in Angstrom) used for searching atoms within each query atom that can be used for the B factor normalization.

Dependencies
============
* parmed
* numpy
* scipy

Contact
=======
tobias.wulsdorf@gmail.com
