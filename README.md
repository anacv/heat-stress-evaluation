# Heat Stress Evaluation
This repository supports the coordination of the EURO-CORDEX heat stress evaluation, as part of the broader [EURO-CORDEX joint evaluation](https://github.com/euro-cordex/joint-evaluation) effort.


### Preparing a working environment

All the scripts and notebooks are reproducible at the existing jsc-cordex data exchange infrastructure at Jülich Supercomputing Centre (JSC). More details for data exchange and access are available [here](https://github.com/euro-cordex/joint-evaluation#data-exchange).

To this aim, the climate4R conda metapackage must be previously installed:

```
micromamba create -n R4.3 -c conda-forge  "r-base==4.3.*" r-climate4r
```

Once succesfully installed:
```
micromamba activate R4.3
```

Heat stress indices will be calculated with the [HeatStress package](https://github.com/anacv/HeatStress), thus it should be installed in R by doing:

```
install.packages("remotes")
remotes::install_github("anacv/HeatStress")
```

A list of all available indices and the atomic functions calculating them is printed on screen with:

```
library(HeatStress)
indexShow()
```
