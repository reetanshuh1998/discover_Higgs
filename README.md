# discover_Higgs
using root file to discover higgs using two lepton decay and 4 lepton decay channel

## GitHub Codespaces

This repository includes a pre-configured GitHub Codespace with:
- **Python 3**: For data analysis and scripting
- **Jupyter Notebook/Lab**: For interactive analysis
- **ROOT Framework**: CERN's data analysis framework for particle physics

### How to Use

1. Click the "Code" button on GitHub
2. Select "Codespaces" tab
3. Click "Create codespace on main" (or your branch)
4. Wait for the environment to build (first time may take a few minutes)

### Starting Jupyter Notebook

Once the codespace is running, you can start Jupyter Notebook with:

```bash
jupyter notebook --ip=0.0.0.0 --port=8888 --no-browser --allow-root
```

Or Jupyter Lab:

```bash
jupyter lab --ip=0.0.0.0 --port=8888 --no-browser --allow-root
```

The codespace will automatically forward port 8888, and you can click the forwarded URL in VS Code.

### Using ROOT

ROOT is pre-installed and ready to use. You can:

1. Use ROOT in Python:
```python
import ROOT
```

2. Use ROOT in Jupyter notebooks with the uproot library:
```python
import uproot
import awkward as ak
```

3. Run ROOT interactively:
```bash
root
```

### Pre-installed Python Packages

- jupyter, jupyterlab, notebook
- numpy, matplotlib, scipy, pandas
- uproot, awkward (for ROOT file analysis in Python)
