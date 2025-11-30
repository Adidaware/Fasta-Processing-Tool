# FASTA Processing Toolkit

## What does this code do ?
This is a set of Python command-line tools written to make working with FASTA files easier. It helps automate tasks like separating mixed sequence files and calculating nucleotide statistics.

I built this with **robust error handling** and included **unit tests** to ensure reliability.

## The Tools

### Secondary Structure Splitter (`secondary_structure_splitter.py`)
Sometimes FASTA files contain both amino acid sequences and secondary structure data mixed together. This script reads a file and splits them into two separate clean files.
* **Input:** A mixed FASTA file.
* **Output:** `pdb_protein.fasta` (Protein sequences) and `pdb_ss.fasta` (Secondary structures).


