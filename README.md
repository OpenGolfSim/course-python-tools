Python tools for processing lidar, geotiffs, and feature extraction for automation of most course building steps.


Install mamba and conda-forge on the dev machine

```bash
conda install -n base -c conda-forge mamba
```

Create environment

```bash
mamba env create --prefix ./ogs_python_tools -f environment.yml
```

Activate environment

```bash
conda activate ./ogs_python_tools

```


Then to pack the conda environment:
```bash
# exit the environment
conda deactivate

# clean up unneeded files
conda clean --all --name ogs_python_tools -y

# create the packed environment
conda pack -n ogs_python_tools -o out/ogs_python_tools.tar.gz
```

To install/unpack python tools:
```bash
mkdir myenv
tar -xf example.tar.gz -C myenv
```