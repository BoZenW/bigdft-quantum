# How to compile BigDFT-suite

The following procedure has been tested on ubuntu machines, and ubuntu-WSL2

## Prerequisites

Download BigDFT source code:
```bash
git clone https://gitlab.com/l_sim/bigdft-suite
git checkout 1.9.4 # switch to stable version
```

Dependencies:
```bash
sudo apt-get install gfortran cmake autoconf pkg-config #fortran compiler, cmake
sudo apt-get install libblas-dev liblapack-dev #blas and lapack
sudo apt-get install openmpi-bin openmpi-common libopenmpi-dev # open-mpi
```

## Install

```bash
cd $(BigDFT-src-location)
mkdir build
cd build
#python ../Installer.py autogen
python ../Installer.py build -f ../rcfiles/ubuntu_MPI.rc
```
