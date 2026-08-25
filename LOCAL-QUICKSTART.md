# Running the notebooks on your own machine

Install [uv](https://docs.astral.sh/uv/getting-started/installation/) and, in VSCode, the **Python** and **Jupyter** extensions, then:

```sh
git clone https://github.com/allardjun/MCSBBootcamp.git
cd MCSBBootcamp
uv run --frozen python -m ipykernel install --user --name mcsb --display-name 'Python (MCSB Bootcamp)'
```

That single command builds the environment and registers the kernel, so any notebook you open in VSCode offers **Python (MCSB Bootcamp)**, exactly as a Codespace does.
It records this folder's path, so run it again if you move the clone.
