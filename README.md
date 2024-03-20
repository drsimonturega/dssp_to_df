# dssp_to_df

This is a very short Python script that loads a *.cif file containing dssp data into a pandas dataframe,  I am currently working with the pdb code 5B04,  that's ok for now but at some point in the future we may want to change that.

The imports is using a pandas ```pd.read_csv()''' command that does most of the work, with the columns to import being selected with the list ```col_lst```;
```df = pd.read_csv("5b04.cif", sep = " ", skiprows = 38428, skipinitialspace = True, ```
```    header = None, usecols = col_lst, skipfooter = 1, engine='python')```
The header titles for the columns or my interpretation of them are given as a list below,
```["chain", "res_num", "AA", "ss", "kappa helix", "3-10 helix", "alpha helix", ```
```            "pi helix", "geometrical bend", "chirality_1", "chirality_2" "beta bridge label",```
```            "beta bridge label", "BP1", "BP2",  "ACC", "N-H-->O", "O-->H-N", "N-H-->O",```
```            "O-->H-N", "TCO", "KAPPA", "ALPHA", "PHI", "PSI", "X-CA", "Y-CA","Z-CA" ]```

The dssp database is here, 
[DSSP (Dictionary of Secondary Structure in Proteins)](https://pdb-redo.eu/dssp)


The references for the DSSP database tools, 
1 W. Kabsch and C. Sander, Biopolymers, 1983, 22, 2577-2637 (DOI:10.1002/bip.360221211).
2 R. P. Joosten, T. A. H. te Beek, E. Krieger, M. L. Hekkelman, R. W. W. Hooft, R. Schneider, C. Sander and G. Vriend, Nucleic Acids Res., 2011, 39, D411-D419 (DOI:10.1093/nar/gkq1105).
