# SeSG (Search String Generator)

Implementation and experimentation of SeSG, a search string generator that uses text mining techniques to build a search string from a supplied Quasi-Gold Standard.

### :warning: Note

This is a research algorithm, susceptible to errors and imperfections.

### :file_folder: Structure
This is the directory structure. In summary, there is a folder with the results of the quasi-experiment (complete-results), a folder with the output of the execution (exits), a folder with the input files of the execution (files-qgs) and the codes that form the SeSG.

```bash
├── SeSG
│   ├── complete-results
│   │   ├── azeem-review
│   │       └── ...
│   │   ├── hosseini-review
│   │       └── ...
│   │   └── vasconcellos-review
│   │       └── ...
│   ├── exits
│   │   ├── snowballing-images
│   │   ├── manual-exit.csv
│   │   ├── result.csv
│   │   └── sentences.txt
│   ├── files-qgs
│   │   ├── review-azeem
│   │       ├── gs-pdf
│   │       ├── gs-txt
│   │       ├── qgs-txt
│   │       ├── GS.csv
│   │       └── QGS.csv
│   │   ├── review-hosseini
│   │       └── ...
│   │   └── review-vasconcellos
│   │       └── ...
│   ├── README.md
│   ├── SeSG-azeem-random.py
│   ├── requirements.txt
│   ├── SeSG-hosseini-random.py
│   └── SeSG-vasconcellos-random.py

```

###  :runner: Running

To run SeSG, simply run some of the .py files present at the root of the directory.

####  :one: Azeem et al.

The file `SeSG-azeem.py` performs the experiment for the study by Azeem et al. [[1]](#1). For this to happen, some parameters passed within the code must be:

```bash
author = 'azeem'
pub_year_one = 2018  # 0 = disable pub_year
pub_year_two = 1999  # 0 = disable pub_year
qgs_size = 5
gs_size = 15
```

####  :two: Hosseini et al.

The file `SeSG-hosseini.py` performs the experiment for the study by Hosseini et al. [[2]](#2). For this to happen, some parameters passed within the code must be:

```bash
author = 'hosseini'
pub_year_one = 2016  # 0 = disable pub_year
pub_year_two = 0  # 0 = disable pub_year
qgs_size = 15
gs_size = 46
```

####  :three: Vasconcellos et al.

The file `SeSG-vasconcellos.py` performs the experiment for the study by Vasconcellos et al. [[3]](#3). For this to happen, some parameters passed within the code must be:

```bash
author = 'vasconcellos'
pub_year_one = 2015  # 0 = disable pub_year
pub_year_two = 0  # 0 = disable pub_year
qgs_size = 10
gs_size = 30
```

###  :bar_chart: Results

###   :bangbang: Requirements
* Python 2.7
* Torch 1.2.0+
* Numpy 1.15.4+
* Pandas 0.23.4+
* Graphviz 0.11+
* scikit-learn 0.20.1+
* Fuzzywuzzy 0.17.0+
* pyscopus 0.9.0
* pytorch_transformers 1.0.0+
* python-Levenshtein 0.12.0

### :page_facing_up: References
<a id="1">[1]</a> Azeem, M. I., Palomba, F., Shi, L., & Wang, Q. (2019). [Machine learning techniques for code smell detection: A systematic literature review and meta-analysis.](https://www.sciencedirect.com/science/article/abs/pii/S0950584918302623) Information and Software Technology, 108, 115-138.

<a id="2">[2]</a> Hosseini, S., Turhan, B., & Gunarathna, D. (2017). [A systematic literature review and meta-analysis on cross project defect prediction.] (https://ieeexplore.ieee.org/abstract/document/8097045/) IEEE Transactions on Software Engineering, 45(2), 111-147.

<a id="3">[3]</a> Vasconcellos, F. J., Landre, G. B., Cunha, J. A. O., Oliveira, J. L., Ferreira, R. A., & Vincenzi, A. M. (2017). [Approaches to strategic alignment of software process improvement: A systematic literature review.] (https://www.sciencedirect.com/science/article/pii/S0164121216301893) Journal of systems and software, 123, 45-63.
