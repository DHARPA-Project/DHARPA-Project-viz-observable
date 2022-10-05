# Lineage visualization prototype
## Create data sample for the visualization
- Create virtual ennvironment and install Kiara</br>
  After activating a Conda virtual environment, run the following commands:
  
```
conda install -c conda-forge mamba
mamba install -c conda-forge -c dharpa kiara kiara_plugin.core_types kiara_plugin.tabular kiara_plugin.network_analysis kiara_plugin.language_processing
```

- Run the Data sample creation notebook </br>
Data sample creation available in the 'dag-lineage/lineage_data.ipynb' Jupyter notebook file.</br>
This process will enable the creation of json files used in the Observable visualization.