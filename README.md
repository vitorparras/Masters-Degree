# Master's Degree

[![License: All rights reserved](https://img.shields.io/badge/License-All%20rights%20reserved-lightgrey.svg)](License)
[![OpenSSF Scorecard](https://api.scorecard.dev/projects/github.com/vitorparras/Masters-Degree/badge)](https://scorecard.dev/viewer/?uri=github.com/vitorparras/Masters-Degree)
[![Contributor Covenant](https://img.shields.io/badge/Contributor%20Covenant-2.1-4baaaa.svg)](CODE_OF_CONDUCT.md)

Coursework from my Master's program: exercises, source code, experiments and
reports, organized by academic module. Published as a study reference.

> **Academic integrity:** this material documents work I submitted. Use it to
> learn and compare; do not submit it, in whole or in part, as your own.

## Table of contents

- [Modules](#modules)
- [Running the code](#running-the-code)
- [Repository layout](#repository-layout)
- [Contributing](#contributing)
- [Security](#security)
- [Code of conduct](#code-of-conduct)
- [License](#license)

## Modules

### Algorithm Analysis and Design

- [Research on Elementary Graph Algorithms](<Academic Modules/Algorithm Analysis and Design/Research on Elementary Graph Algorithms.pdf>)
  (PDF): representations, breadth-first and depth-first search, and their
  complexity.

### Digital Image Processing

Nine exercise sets in Python, with MATLAB/Octave scripts for the last one.
Reports and comments are in Portuguese.

| # | Topic | Folder |
|---|---|---|
| 1 | Fundamentals: sampling, quantization, basic operations | [`# 1 - Fundamentos`](<Academic Modules/Digital Image Processing/Exercises/# 1 - Fundamentos>) |
| 2 | Noise and enhancement: noise models, histogram and contrast | [`# 2 - Ruído e Realce`](<Academic Modules/Digital Image Processing/Exercises/# 2 - Ruído e Realce>) |
| 3 | Spatial filtering | [`# 3 - Filtragem`](<Academic Modules/Digital Image Processing/Exercises/# 3 - Filtragem>) |
| 4 | Color models | [`# 4 - ModelosCores`](<Academic Modules/Digital Image Processing/Exercises/# 4 - ModelosCores>) |
| 5 | Frequency-domain filtering | [`# 5 - FiltragemDominioFrequecia`](<Academic Modules/Digital Image Processing/Exercises/# 5 - FiltragemDominioFrequecia>) |
| 6 | Segmentation | [`# 6 - Segmentação`](<Academic Modules/Digital Image Processing/Exercises/# 6 - Segmentação>) |
| 7 | Mathematical morphology | [`# 7 - Morfologia Matemática`](<Academic Modules/Digital Image Processing/Exercises/# 7 - Morfologia Matemática>) |
| 8 | Texture representation and analysis | [`# 8 - Representação e Análise de Textura`](<Academic Modules/Digital Image Processing/Exercises/# 8 - Representação e Análise de Textura>) |
| 9 | Feature space and classification: k-NN, hold-out and k-fold | [`# 9 - Espaço de Características e Classificação`](<Academic Modules/Digital Image Processing/Exercises/# 9 - Espaço de Características e Classificação>) |

### High Performance Computing

| Activity | Content | Folder |
|---|---|---|
| 1 | Numerical integration (trapezoidal rule) parallelized with **Pthreads** and **OpenMP**; experiment runner and report comparing precision and speed-up by thread count | [`Academic activity 1`](<Academic Modules/High Performance Computing/Academic activity 1>) |
| 2 | The same problem distributed with **MPI**, with report | [`Academic activity 2`](<Academic Modules/High Performance Computing/Academic activity 2>) |
| — | [Study guide for exam 1](<Academic Modules/High Performance Computing/Study guide Exam 1.md>) | |

## Running the code

Compiled binaries are not versioned; build from source.

**Digital Image Processing (Python 3.10+)**

```bash
python -m venv .venv && source .venv/bin/activate   # on Windows: .venv\Scripts\activate
pip install numpy matplotlib opencv-python pillow scikit-image scipy scikit-learn
cd "Academic Modules/Digital Image Processing/Exercises/# 1 - Fundamentos"
python ex.py
```

The `.m` scripts in exercise 9 run in MATLAB or GNU Octave.

**High Performance Computing (GCC, OpenMP, Pthreads, MPI)**

```bash
cd "Academic Modules/High Performance Computing/Academic activity 1"
gcc -O2 -fopenmp integral_openmp.c -o integral_openmp
gcc -O2 -pthread integral_pthreads.c -o integral_pthreads
python run_experiments.py          # runs the matrix of threads x step sizes

cd "../Academic activity 2"
mpicc -O2 integral_mpi.c -o integral_mpi
mpiexec -n 4 ./integral_mpi
```

## Repository layout

```text
Masters-Degree/
├── Academic Modules/
│   ├── Algorithm Analysis and Design/
│   ├── Digital Image Processing/
│   │   └── Exercises/            # one folder per exercise set, with images and scripts
│   └── High Performance Computing/
│       ├── Academic activity 1/  # Pthreads and OpenMP, experiments, report
│       └── Academic activity 2/  # MPI, report
├── .github/                      # Issue templates, workflows, Dependabot
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── SECURITY.md
└── License
```

## Contributing

This is a personal academic archive, so contributions are limited to errata and
reproducibility fixes. See [CONTRIBUTING.md](CONTRIBUTING.md). Questions about
the material are welcome in
[Discussions](https://github.com/vitorparras/Masters-Degree/discussions).

## Security

Found a problem in this repository's code or configuration? Follow
[SECURITY.md](SECURITY.md) and report it privately.

## Code of conduct

This project follows the [Contributor Covenant](CODE_OF_CONDUCT.md). By
participating you agree to uphold it.

## License

**All rights reserved.** Copyright © Vitor Hugo Parras. You may read the
material for study; copying, modifying or redistributing it requires written
permission. See [License](License) (in English and Portuguese).
