## DiffCSP++
Official Implementation of Space Group Constrained Crystal Generation (DiffCSP++). Andre's implementation.

### Dependencies

```
python==3.8.13
torch==1.9.0
torch-geometric==1.7.2
pytorch_lightning==1.3.8
pymatgen==2022.9.21
```

Also include a .env file in the root directory with the following absolute paths:
```
export PROJECT_ROOT="<root directory of cloned repo>"
export HYDRA_JOBS="<subfolder for hydra>"
export WABDB_DIR="<subfolder for wabdb>"
export export WANDB_API_KEY="<your W&B api key here>"
```

### Training

For the CSP task

```
python diffcsp/run.py data=<dataset> expname=<expname>
```

For the Ab Initio Generation task

```
python diffcsp/run.py data=<dataset> model=diffusion_w_type expname=<expname>
```

The ``<dataset>`` tag can be selected from perov (not perov_5), mp_20, mpts_52 and carbon_24. 
I have edited run.py to allow me to access subdirectories, and also change 'fork' to 'thread'.
