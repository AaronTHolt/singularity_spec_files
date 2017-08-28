BootStrap:docker
From:centos:latest


##%environment

%runscript

echo "Adding Intel compiler, mkl, and mpi to environment"

# Intel ROOT
export INTEL=/curc/sw/intel/17.4/compilers_and_libraries_2017.4.196/linux

# Intel Compiler
source $INTEL/bin/compilervars.sh intel64

# Intel MPI
source $INTEL/mpi/bin64/mpivars.sh intel64

# Intel MKL
source $INTEL/mkl/bin/mklvars.sh intel64



%post

yum check-update

# Omnipath user libraries
yum install -y libhfi1 libpsm2
yum install -y perftest


# Other useful libraries
yum install -y pciutils
yum install -y which

# Editors
yum install -y vim emacs

# GCC make bison flex etc
yum groupinstall -y 'Development Tools'

# Version Control
yum install -y git

