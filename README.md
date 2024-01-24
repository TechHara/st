# st

Calculates count, min, max, mean, and standard deviation of data with O(1) space complexity.

## Build & Install
```shell
# build
mkdir build && cd build
cmake .. -DCMAKE_CXX_FLAGS=-O3
make -j4

# install
sudo install -v st /usr/local/bin
```

## Usage
```shell
seq 100000000 | st
#count	100000000
#min	1
#mean	5e+07
#max	1e+08
#stddev	2.88675e+07

ls -l | awk -v OFS="\t" '$1=$1' | cut -f5 | st
#warning: skipping empty line at 1
#count	5
#min	104
#mean	590
#max	2034
#stddev	811.389
```