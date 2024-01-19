# NCI notes

Some notes on using R within NCI gadi.

## Installing devtools, Rcpp and other packages that need compilation

On NCI R has been built with the intel compiler, and there are multiple options here. One option I have found that works, without throwing up a lot of warning messages is to use the LLVM Intel compiler, by running (or equivalent latest version)


```sh
module load R/4.1.0  # Or whatever version you want
module load intel-compiler/2021.2.0  # Ideally the compiler R was built with
module load intel-mkl/2021.2.0  # This is from the NCI docs and it seems to be required sometimes
```

To find the compiler that R was built with (it is apparently recommended to use that for building devtools) then you can find it in:

```sh
cat /apps/R/4.1.0/README.nci  # Replace 4.1.0 with the version of R you need
```
## Installing MCMCpack and some other R packages

*From the NCI help*

> [!quote]
> Note, that some packages can not be build with Intel compilers. The problem usually happens when a package using complex variables. In such cases, you need to switch to GNU compilers. This is done by modifying ~/.R/Makevars file in your $HOME directory. Putting the following lines in this file:
> ```makefile
> CXX=g++
> CXX11=g++
> CXX14=g++
> CXX17=g++
> CC=gcc
> ```
> will force R to use gcc/g++ instead of icc. Do not forget to comment out these lines (i.e. add # symbol in front of each line) after installing that problematic package.

### Running an RStudio interface

- For creating some GIS workflow on the ARE Rstudio interface I have placed the following in my modulefiles (Advanced setup) section:
    - `intel-compiler-llvm/2022.0.0 gdal/3.6.4 geos/3.11.2 proj/8.1.1 udunits/2.2.26`

## R and pkg versions (1/12/23)

R 4.2.2, pmwg_0.2.5.9001, mcce_0.2.4.9002   (No multi-core)
R 4.0.0, pmwg_0.2.5.9001 mcce_0.0.0.9012    (multicore) - oldstate
R 4.0.0, pmwg_0.2.5.9001 mcce_0.0.2.9000    (multicore) - oldstate2
R 4.0.0, pmwg_0.2.5.9001  mcce_0.1.1  (multicore) - oldstate3
R 4.0.0, pmwg_0.2.5.9001  mcce_0.2.3  (multicore) - oldstate4
R 4.0.0, pmwg_0.2.5.9001 mcce_0.2.4.9002 (multicore)
R 4.1.0, pmwg_0.2.5.9001 mcce_0.2.4.9002 (multicore)
R 4.2.2, pmwg_0.2.5.9001 mcce_0.2.4.9002 (no multicore)
R 4.3.1, pmwg_0.2.5.9001 mcce_0.2.4.9002 (no multicore)


## Installing gcc R

```bash

```