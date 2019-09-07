## Useful conda commands

### Replicate an existing environment
First activate the environment that you want to copy. 

`source activate <env_name>`

`conda env export | grep -v "^prefix: " > <env_name>.yml`

To install the environment do the following:

`conda env create -f <env_name>.yml`
