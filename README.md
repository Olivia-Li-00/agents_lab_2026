# agents_lab_2026
notebooks on agents

- Lab1: [link](https://colab.research.google.com/drive/1_OOxH8WrnvWgqGx7op2u5BlR7RJ2c9rx?usp=sharing)
- Lab2: open `Lab2.ipynb` in Colab via the badge at the top of the file.

## Local setup

The notebooks are designed for Colab, but you can also run them locally with JupyterLab.

### 1. Create a Python 3.12 venv

```bash
python3.12 -m venv ~/pyvenvs/py312-agents-lab-2026
source ~/pyvenvs/py312-agents-lab-2026/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

### 2. Register the venv as a JupyterLab kernel

```bash
python -m ipykernel install --user \
    --name py312-agents-lab-2026 \
    --display-name "Python 3.12 (agents_lab_2026)"
```

### 3. Launch JupyterLab

```bash
jupyter lab
```

Then open a notebook and pick the `Python 3.12 (agents_lab_2026)` kernel.

### 4. API key (for local runs)

The notebooks read `GOOGLE_API_KEY` from `google.colab.userdata` on Colab. To run locally, replace those two lines with:

```python
import os
GOOGLE_API_KEY = os.environ["GOOGLE_API_KEY"]
```

and export the key before launching Jupyter:

```bash
export GOOGLE_API_KEY=...
```
