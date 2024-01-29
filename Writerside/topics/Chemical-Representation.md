# Chemical Representation

Chemicals can be thought of as graphs: a series of nodes (atoms) and edges (bonds) that define the chemical structure.
While methods exist that can take graphs as an input (Graph Neural Networks for instance), one often converts chemical structure into a numerical vector (in a somewhat lossy manner) using a process called "chemical fingerprinting". 

> It is important to note that AIRCHECK **only** provides precomputed chemical fingerprints of enriched DEL compounds,
> while the complete chemical structures will not be provided as they remain the intellectual properties
> of the data providers. It is a violation of the AIRCHECK terms of agreement to try and determine chemical structure from these
> fingerprints

There are several approaches to chemical fingerprinting. AIRCHECK uses up to 9 of these. Unless otherwise marked, all fingerprints are hashed/count versions:

- ECFP4: Extended connectivity fingerprints with 2048 bits and a radius of 4
- ECFP6: Extended connectivity fingerprints with 2048 bits and a radius of 6
- FCFP4: Feature connectivity fingerprints with 2048 bits and a radius of 4
- FCFP6: Feature connectivity fingerprints with 2048 bits and a radius of 6
- MACCS: 166 bit common substructure fingerprint **BINARY**
- RDK: The rdkit graph based fingerprint with 2048 bits and max length of 7 **BINARY**
- AVALON: 2048 bit fingerprint from Avalon
- TOPTOR: Topological Torsion fingerprint with 2048 bits
- ATOMPAIR: Atom Pair fingerprint with 2048 bits

Not all the datasets in AIRCHECK will have all 9 of these fingerprints: the datasets will be marked with which fingerprints will
be available after downloading. More information regarding the various chemical fingerprint formats can be found [here](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4932683/).
