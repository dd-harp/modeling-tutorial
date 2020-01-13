# MASH Tutorials

Use these scripts to get started simulating with MASH-MACRO.

**First -** Make sure that you have downloaded the `macro.pfsi` library. If you are not able to load the library in R, use the script `macro-pfsi-download.Rmd` to load the library in an appropriate location and then you should be good to go.

Directories:

* `report_sources` - where to put all of the `.Rmd` scripts
* `scripts` - where to put auxiliary scripts
* `sim_outputs` - where to put
* `data` - store data, either unprocessed (`raw`) or preprocessed (`clean`)

Specific scripts:

* `mash-macro-workflow.Rmd` - a tutorial for how to set up and analyze a nontrivial simulation
* `bioko-data-wrangling` - some example scripts for how to preprocess the Bioko Island data for the purpose of running a MASH simulation
* `bioko-mash-macro-workflow.Rmd` - a tutorial for how to simulate Bioko Island, and calibrating using the Bioko Island data.
