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
* `bioko_data_wrangling.Rmd` - some example scripts for how to preprocess the Bioko Island data for the purpose of running a MASH simulation, along with some discussion questions considering how we use the data
* `bioko-mash-macro-workflow.Rmd` - a tutorial for how to simulate Bioko Island, and calibrating using the Bioko Island data.


------

Update, following tutorial session on January 17, 2020: more detailed step-by-step notes on how to get access to the `macro.pfsi` library in an RStudio session.

For the sake of centralized convenience, we will show how to set up everything remotely on the cluster. It is possible to run everything locally instead, but it will require a few extra steps for configuring things.

  1. Permissions:
    * Make sure that you belong to the group `ihme-malaria` (use `id` in the terminal to see)
    * Make sure that you have access to the `proj_mmc` project flag, for running the RStudio session (`qconf -su proj_mmc` in terminal)
    * Submit helpdesk tickets, if access isn't yet granted
  2. Clone the repo to your home directory -

  ```git clone https://github.com/dd-harp/modeling-tutorial.git```

  3. Launch the RStudio session on the cluster

  ``` /ihme/singularity-images/rstudio/shells/jpy_rstudio_qsub_script.sh -i /ihme/singularity-images/rstudio/latest.img -t rstudio -f 4 -h 120 -m 8G -P proj_mmc -q i ```

  4. In a web browser, navigate to the URL for the RStudio session once it launches. Use the correct web address, but also the correct port (which will be assigned on an individual basis)
  5. Within the RStudio session, browse to the repo's directory
  6. Set up by running `macro-pfsi-download.Rmd` to download the library. Feel free to customize `output_dir` and `lib_loc` to pick your favorite location for storing libraries.
  7. Begin the tutorial by running `mash-macro-workflow.Rmd`, making sure to use the correct paths for loading the `macro.pfsi` library.
