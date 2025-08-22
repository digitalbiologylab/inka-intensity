# inka-250402


## Installation and Usage Guide

### 1. Install Miniconda
If you don’t have **Miniconda** installed, please follow the instructions here:  
👉 [Miniconda Installation Guide](https://www.anaconda.com/docs/getting-started/miniconda/install)

### 2. Create Conda Environment
This project uses an environment including both **Python** and **R**, defined in the file `py312_r.yml`.

If you want to change the environment name, modify the line:

```yaml
name: py312_r_env
```

Run the following command to create the environment (only needed once if it doesn’t already exist):

```bash
conda env create -f py312_r.yml
```


## 3. Go to INKA Program Directory
Clone the INKA repository:

```bash
git clone https://github.com/digitalbiologylab/inka-250402
```

Navigate into the program folder:

```bash
cd inka-250402
```

Then go to the analysis folder:

```bash
cd inka_20220330
```

Execute the main R Markdown script:

```bash
Rscript -e "rmarkdown::render('./_script.rmd')"
```

Alternatively, you can create a small script `run_script.sh` with the following content:

```bash
conda activate py312_r_env
Rscript -e "rmarkdown::render('./_script.rmd')"
```

