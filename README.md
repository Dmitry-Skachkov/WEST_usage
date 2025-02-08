# WEST_usage
WEST code can be installed inside Quantum Espresso (QE) directory.

Load necessary modules:

> vpkg_require openmpi/4.1.5:intel-2020

> vpkg_require intel-mkl/2020u4

> vpkg_require python/3.8.6

> cd {QE directory}

Download the source code:
> git clone -b 'v6.1.0' --single-branch --depth 1 https://github.com/west-code-development/West.git West

Configure the system
> make conf PYT=python3 PYT_LDFLAGS="`python3-config --ldflags --embed`"

Make installation
> make all

Check that the executables are place in bin directory

```
wstat.x
wfreq.x
wbse.x
westpp.x
```

