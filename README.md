# MCSB Bootcamp — Mathematical and Computational Track

Some course material used in the incoming-student bootcamp for graduate students in the [UCI MCSB](https://mcsb.uci.edu) graduate program.

**[Open the course website →](https://allardjun.github.io/MCSBBootcamp/)**

## Code notebooks

- [Project 3: Discrete logistic growth](docs/PS3_discrete-logistic.ipynb)
- [Project 4: Phosphorylation–dephosphorylation](docs/PS4_futile-cycle.ipynb)
- [Project 5: FitzHugh-Nagumo and excitability](docs/PS5_fitzhugh-nagumo.ipynb)
- [Project 6: Bacterial growth and parameter fitting](docs/PS6_bacterial-growth.ipynb)
- [Project 7: Complex systems and classical systems biology](docs/PS7_complex-systems.ipynb)
- [Network motifs](docs/network-motifs.ipynb)
- [Numerical calculus quick-start](docs/numerical-calculus-quick-start.ipynb)
- [Python test drive](docs/python-test-drive.ipynb)
- [Synthetic biology, simplified](docs/synthetic-biology-simplified.ipynb)

## Running the notebooks

### Option 1: To run in Codespace:

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/allardjun/MCSBBootcamp)

When it opens, wait (it takes a while! ~10min), this README opens in the top pane (wait longer than you think). 
Click a notebook above and press **Run All**.
It will ask you to choose a kernel.
Choose the `Python MCSB Bootcamp` kernel.

### Option 2: JupyterLab in Codespace

Codespaces can open straight into JupyterLab instead of the VSCode interface, with no extra step once you have set it once:

1. Go to [your Codespaces settings](https://github.com/settings/codespaces).
2. Under **Editor preference**, choose **JupyterLab**.

From then on the button above opens JupyterLab directly.
Choose the kernel named **Python (MCSB Bootcamp)**.

To switch a codespace you have already created, go to [your codespaces](https://github.com/codespaces), click the `…` beside it, and choose **Open in JupyterLab**.

### Option 3: On your own machine

Install [uv](https://docs.astral.sh/uv/getting-started/installation/), which installs the right Python and packages for you:

```sh
git clone https://github.com/allardjun/MCSBBootcamp.git
cd MCSBBootcamp
uv sync
```

Then open any notebook above in VSCode and select the `.venv` interpreter, or run `uv run jupyter lab`.
To get the kernel listed under the same name as in a Codespace, see **[LOCAL-QUICKSTART.md](LOCAL-QUICKSTART.md)**.