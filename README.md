# MCSB Bootcamp — Mathematical and Computational Track

Course materials for the incoming-student bootcamp in the Mathematical, Computational and Systems Biology program.

**[Open the course website →](https://allardjun.github.io/MCSBBootcamp/)**

Every project is available in five formats, all generated from one source: **html** to read in a browser, **pdf** to print, **tex** if you want to lift a derivation into your own document, **md** as plain markdown, and **ipynb** as a Jupyter notebook you can work in directly.

## Running the notebooks

The bootcamp is deliberately language-agnostic.
Where a project says "write code", write it in whatever language you intend to use for the rest of your degree — Matlab, Python, R, Julia — and be ready to explain your choice to someone who picked differently.

The lecture notebooks are Python, and there are three ways to run them.

### In the browser, with nothing installed

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/allardjun/MCSBBootcamp)

This builds a machine in the cloud with everything already installed.
Give it a few minutes the first time.
When it opens, the notebooks are in `docs/` — open one and click **Run All**.

To use JupyterLab instead of the VSCode interface, go to [your codespaces](https://github.com/codespaces), click the `…` menu beside this one, and choose **Open in JupyterLab**.
Pick the kernel named **Python (MCSB Bootcamp)**.

### On your own machine

You need [uv](https://docs.astral.sh/uv/getting-started/installation/), which manages the Python version and the packages for you:

```sh
git clone https://github.com/allardjun/MCSBBootcamp.git
cd MCSBBootcamp
uv sync
```

Then open any notebook in `docs/` in VSCode and select the `.venv` interpreter, or start JupyterLab with `uv run jupyter lab`.

### By downloading one notebook

Every project page on the website has an **ipynb** link.
Download it and open it in whatever you already use.
You will need `numpy`, `scipy` and `matplotlib`.

## A note on what you will find here

Some code cells in the lecture notebooks are already run, and you are reading their results.
Others are deliberately left for you: complete code that you should run yourself, and empty stubs for you to fill in.
Both are ordinary code cells — put your cursor in one and run it.

---

*This repository is generated.
Its source lives in a separate repository, and everything here is rebuilt from that, so edits made here are overwritten on the next publish.*
