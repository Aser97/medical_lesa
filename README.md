# How to set up the environment:
- Create a new environment python virtual environment `lesa_venv` based on the `.yml` file
      `conda env create -f medical_lesa/lesa_venv.yml`

- Activate the environment and create the jupyter kernel
      `conda activate lesa_venv`
      `pip install ipykernel`
      `python -m ipykernel install --user --name lesa_venv --display-name "lesa_venv"`

- Replace the `transformers/camembert` folder with our version present in this repo
      `scp -r medical_lesa/camembert ~/.conda/envs/lesa_venv/lib/python3.11/site-packages/transformers/models`

- Replace the `transformers/__init__.py` file with our version present in this repo
      `scp -r medical_lesa/transformers__init__.py ~/.conda/envs/lesa_venv/lib/python3.11/site-packages/transformers/__init__.py`
