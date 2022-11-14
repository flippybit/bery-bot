# Forgive and Forget list of commands
In no particular order or subject

**dont forget to use mamba and install pip packets last**
* conda create a new environment with a file **better**
    ```bash
    mamba env create --prefix ./env --file environment.yml
    ```
* export the dependancies to the environment.yml file 
* export dependancies that we manually installed.

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