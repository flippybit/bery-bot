# ReadTheDocs Flow

## This guide is a note for future me

dear future me,  
your memory is bad !  
I know you been busy building hardware and other stuff...  
let me put you up to date with this part of the project.  
but before maybe i list you the reasons why you choose this format and not make a SPA with angular or other webstuff.
1. everyone else is doing it.
2. you love jupyter-notebooks
3. sphinx plays nice with jupyter.
4. readthedocs plays nice with sphinx.
5. its easy to host and pubish (i know you could do something more cool but KISS)  

**you can refresh your memory following these URLS**     
you stole this template from https://example-jupyter-book.readthedocs.io/intro.html




### Some of the building stuff you need to follow to continue.
it uses jupyter notebooks and uses pip for building the proyect, but you hate pip thats why you choose `conda`
 
 not sure how sphinx works but you use it the flow goes like this 

`_config.yml` is where you should make the changes to your notebook
conf.py is where they are reflected.

to modify conf.py use `jupyter-book conf sphinx ~/path/to/notebooks/_config.yml`  
`.readthedocs.yml` is where all the build parameters that readthedocs.io uses to host this proyect

### **.readthedocs.yml**
**remember** we have modified this file to suite our needs, these are the modifications:  
* we use mamba to build this (we hate the slow conda) 
  ```yaml
  build:
  os: ubuntu-20.04
  tools:
    python: "mambaforge-4.10" <-----
  ```
  i know its confusing to set python to mamba but such is life 

* dont touch this line im not sure if we need to use it or not
  
  ```yaml
   jobs:
   pre_build:
      # Generate the shpinx config  jupyter book so it builds
      -  "jupyter-book config sphinx docs/"
  ```
*   and last but not least we indicate the use of a conda environment instead of pip
    ```yaml
    conda:
      environment: environment.yml
    ```

