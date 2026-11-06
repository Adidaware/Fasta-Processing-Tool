# FASTA Processing Tool

Command-line tools for two common FASTA chores: splitting a mixed protein/secondary-structure file into two clean files, and counting nucleotides in every sequence. Both tools are built on a shared FASTA parser, validate their inputs, and come with unit tests.

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white) ![pytest](https://img.shields.io/badge/tested%20with-pytest-0A9EDC?logo=pytest&logoColor=white)

## 🧰 Tools

### `secondary_structure_splitter.py`
Splits a FASTA file that mixes amino-acid sequences and secondary-structure strings (such as PDB `ss.txt`) into two files.

* Records whose header contains `amino acid sequence` go to **`pdb_protein.fasta`**.
* All other records go to **`pdb_ss.fasta`**.

```bash
python secondary_structure_splitter.py -i ss.txt
```

### `nt_fasta_stats.py`
Counts A, G, C, T and N in every sequence and writes a tab-separated report:

| Header | NCBI Accession | A_count | G_count | C_count | T_count | N_count |
| :--- | :--- | ---: | ---: | ---: | ---: | ---: |

```bash
python nt_fasta_stats.py -i genes.fasta -o genes_stats.tsv
```

## 🚀 Getting Started

```bash
git clone https://github.com/Adidaware/Fasta-Processing-Tool.git
cd Fasta-Processing-Tool
pip install -r requirements.txt   # only needed to run the tests
```

The tools themselves use only the Python standard library.

## ✅ Tests

```bash
python -m pytest
```

The tests cover FASTA parsing, header/sequence list validation, nucleotide counting, accession extraction and file output.

## 📁 Repository Layout

```
├── secondary_structure_splitter.py       # protein / secondary-structure splitter
├── nt_fasta_stats.py                     # per-sequence nucleotide counts
├── test_secondary_structure_splitter.py
├── test_nt_fasta_stats.py
└── .coveragerc                           # coverage settings (tests excluded)
```

## 👤 Author

**Aditya Daware** · [LinkedIn](https://www.linkedin.com/in/aditya-daware) · [GitHub](https://github.com/Adidaware)
