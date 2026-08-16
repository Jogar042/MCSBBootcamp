# MCSB Bootcamp — Mathematical and Computational Track

Course materials for the incoming-student bootcamp in the Mathematical, Computational and Systems Biology program.

**[Open the course website →](https://allardjun.github.io/MCSBBootcamp/)**

The website is the place to read the projects.
This repository is the place to *run* them.

## Notebooks

Click one to open it.
Every project is also on the website as html, pdf, tex and markdown.

- [Project 3: Discrete logistic growth](docs/PS3_discrete-logistic.ipynb)
- [Project 4: Phosphorylation–dephosphorylation](docs/PS4_futile-cycle.ipynb)
- [Project 5: FitzHugh-Nagumo and excitability](docs/PS5_fitzhugh-nagumo.ipynb)
- [Project 6: Bacterial growth and parameter fitting](docs/PS6_bacterial-growth.ipynb)
- [Project 7: Complex systems and classical systems biology](docs/PS7_complex-systems.ipynb)
- [Numerical calculus quick-start](docs/numerical-calculus-quick-start.ipynb)
- [Python test drive](docs/python-test-drive.ipynb)

## Running them

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/allardjun/MCSBBootcamp)

That button builds a machine in the cloud with Python, numpy, scipy and matplotlib already installed.
Give it a few minutes the first time.
When it opens, this README opens with it — click a notebook above and press **Run All**.

### Keeping your work

The codespace you open is yours, and it lasts.
It stops itself when you go idle, and it is not deleted until 30 days after you last connected — and connecting resets that clock.
A week of on-and-off work is well within it.

What it does not do is keep your work safe.
A codespace is eventually deleted whether or not you have pushed anything, so the rule is simple: **push before you walk away.**

**You do not need to fork first.**
Commit and push exactly as you normally would:

```sh
git add -p
git commit -m "what I did"
git push
```

The first time you push, GitHub notices you cannot write to this repository, makes a fork of it under your own account, and points your codespace at that fork.
Your work lands in your copy, and you did not have to set anything up.

Two things worth knowing:

- A stopped codespace still uses part of your storage allowance.
  Delete the ones you have finished with, from [your codespaces](https://github.com/codespaces).
- Nothing you do here can affect the course repository.
  Push freely.

#### If you would rather fork by hand

Forking deliberately is what modules 1 and 2 are about, so you may well prefer to do it yourself:

1. Click **Fork** at the top right of [this repository](https://github.com/allardjun/MCSBBootcamp).
2. Leave the settings as they are and click **Create fork**.
3. Open a codespace on *your* fork — the green **Code** button on your copy.

One thing to expect if you go this way: **the first codespace you open on your own fork takes several minutes longer.**
This repository keeps a prebuilt image ready and a fork does not inherit it.
Opening the codespace from here and letting your first push create the fork avoids that wait entirely.

### If you would rather use JupyterLab

Codespaces can open straight into JupyterLab instead of the VSCode interface, with no extra step once you have set it once:

1. Go to [your Codespaces settings](https://github.com/settings/codespaces).
2. Under **Editor preference**, choose **JupyterLab**.

From then on the button above opens JupyterLab directly.
Choose the kernel named **Python (MCSB Bootcamp)**.

To switch a codespace you have already created, go to [your codespaces](https://github.com/codespaces), click the `…` beside it, and choose **Open in JupyterLab**.

### On your own machine

You need [uv](https://docs.astral.sh/uv/getting-started/installation/), which installs the right Python and packages for you:

```sh
git clone https://github.com/allardjun/MCSBBootcamp.git
cd MCSBBootcamp
uv sync
```

Then open any notebook above in VSCode and select the `.venv` interpreter, or run `uv run jupyter lab`.

### By downloading a single notebook

Every project page on the website has an **ipynb** link.
Download it and open it in whatever you already use.
You will need `numpy`, `scipy` and `matplotlib`.

## What you will find in the notebooks

Some code cells have already been run, and you are reading their results.
Others are deliberately left for you: complete code that you should run yourself, and empty stubs for you to fill in.
Both are ordinary code cells — put your cursor in one and run it.

The bootcamp is otherwise deliberately language-agnostic.
Where a project says "write code", write it in whatever language you intend to use for the rest of your degree — Matlab, Python, R, Julia — and be ready to explain your choice to someone who picked differently.

---

*This repository is generated.
Its source lives in a separate repository and everything here is rebuilt from that, so edits made here are overwritten on the next publish.
Anything you change while working — including notebook output — is yours locally, but do not expect it to survive a `git pull`.*
