#Preprocessing workflow for DESI imaging, thermo, centroid mode data
###Input: PathName: directory of the imzML files
###Author: Nazanin z. Kermani, Imperial College London 2016.
Workflow:

1. read imzML files
2. log transformation
3. normalization
4. peak matching by heuristic hierarchical agglomerative clustering
5. solvent peaks identification and exclusion
   * exclude ions that occur less than minPixels =3
   * find potential noisy spectra (corrected by the test for spatial randomness) 
6. complete spatial randomness test
