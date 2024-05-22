# zenglab_server
This is PKU ZengHu‘s lab server wiki repository
This wiki references the laboratory management manual by [StatBiomed](https://github.com/StatBiomed/sbms-server)
For lab member use:
- Current  LAN IP in PKU [http://10.128.243.62/](http://10.128.243.62/)
- this is a dynamic address, which means it may change after reboot
## Login,  account data management
See instructions in the [SSH&DataManagement.md](https://github.com/ZenghuPKU/zenglab_server/SSH&DataManagement.md) page

## Environment with Conda

Installing anaconda ,miniconda, mamba  yourself to create base environment for your own. But for specific task, **create your own conda environment**, so that you can control all versions of the packages for your analysis, which is important for reproducibility. Follow the [conda manual](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) to manage your environments.
For pipeline (such as Snakemake) or software you create for your own ,leave a copy on public Conda or wet lab team can access to them easily 

For each environment, you can also add it as a separated kernel on jupyter lab, see [here](https://ipython.readthedocs.io/en/stable/install/kernel_install.html):

```batchfile
conda activate myenv

pip install ipykernel

python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
```

For public conda ,your can source and activate via 

```batchfile
source /media/zenglab/miniconda3/etc/profile.d/conda.sh 
conda activate publiccenv
```
## VS Code

- See instructions on the Vscode page

## Jupyterlab on server
- Directly available (`http` not `https`): [http://10.128.243.62:8000](http://10.128.243.62:8000)
- See instructions on the [Jupyter.md](https://github.com/ZenghuPKU/zenglab_serverJupyter.md)(To be continued)
## RStudio server

- Directly available (`http` not `https`): [http://10.128.243.62:8787](http://10.128.243.62:8787)
- See instructions on the [R.md](https://github.com/ZenghuPKU/zenglab_server/R.md) page (To be continued)
