## Making the required folders

Should not be necessary again - this is where the new software and the modulefile to interact with it will be located.

```sh
ls /g/data/ut81
mkdir /g/data/ut81/apps
mkdir /g/data/ut81/apps/R
mkdir /g/data/ut81/apps/modulefiles
```

# Get the software

In this case it will be R, from CRAN - but theoretically this could be anything we want to build ourselves. I'll show a very R-centric build process here

First get and extract the file, we'll also rename the folder - this is all in the users local directory.
```sh
wget https://cran.r-project.org/src/base/R-4/R-4.3.2.tar.gz
tar xaf R-4.3.2.tar.gz
mv R-4.3.2 R-4.3.2-src
mkdir R-4.3.2-bld
cd R-4.3.2-bld
```

Now we can use the configure script, telling it where we want the final product to go.

```sh
../R-4.3.2-src/configure  --prefix=/g/data/ut81/apps/R/4.3.2/ --enable-R-shlib --with-readline

```

I found I needed java (I think) to build it successfully. Now we are configured we can build the software with make.

```sh
module load java/jdk-13.33
make
make check
make install
```

# Accessing the software

Now that we have built the software we need to configure a module file to load it and use it.

We'll put the module file in our `/g/data` and call it R-ut81/4.3.2
```sh
cd /g/data/ut81/apps/modulefiles
mkdir R-ut81
cd R-ut81
vim 4.3.2 # (Or nano etc)
```

Our module file should have this as the contents

```
#%Module1.0
set             path            /g/data/ut81/apps/R
set             version         4.3.2

prepend-path    PATH            $path/$version/bin
```

# Testing the software

On the login node you should be able to see the new version of R - so lets test that
```sh
module avail R
module load R-ut81/4.3.2
R --version
```

# Setting up the site library

To keep the libraries separate for the custom built R I have also edited the `Renviron` file.

```sh
cd /g/data/ut81/apps/R/4.3.2/
vim lib64/R/etc/Renviron
```

We want that file to have an changed line or two at the end. You may need to play around with it - but what I had that works is to finish with:

```
R_LIBS_USER=${HOME}/R_ut81/${R_PLATFORM}-library/4.3
R_LIBS_USER=${R_LIBS_USER:-'%U'}
R_LIBS_SITE=${R_LIBS_SITE:-'%S'}
```

So we set the default user package location to be in the home directory `R_ut81` folder followed by the actual R version. We can also remove any site wide setting if there is anything there.

The only final steps are to adjust your scripts and your .bashrc so that your jobs can find the modulefiles. See the main [[NCI]] page for help there.