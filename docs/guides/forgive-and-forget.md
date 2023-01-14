# Forgive and Forget list of commands
In no particular order or subject

**dont forget to use mamba and install pip packets last**
* conda create a new environment with a file **better**
    ```bash
    mamba env create --prefix ./env --file environment.yml
    ```
* export the dependencies to the environment.yml file 
* export dependencies that we manually installed.

* Install a package with mamba:
   ```bash
    mamba install matplotlib
    ```
* Install a package with conda:
    ```bash
    conda install matplotlib
    ```
* Dry install a package 
    ```bash
    conda install matplotlib --dry-run
    ```
* Rebuilding a conda environment from scratch
    ```bash
    mamba env list --file environment.yml --force
    ```
* Delete an environment
    ```bash
    mamba env remove --name <environment>
    ```
* List all environments 
    ```bash
    mamba env list
    ```
* create environment using requirements.txt
    ```bash
    mamba create --name <environment_name> --file requirements.txt
    ```