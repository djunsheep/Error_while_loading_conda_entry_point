In VS Code Jupyter notebook, when WSL Distro (Ubuntu), repeatedly got an error when trying to install bwa to one conda env:

`!conda install -c bioconda bwa -y`

_Error while loading conda entry point: conda-libmamba-solver (libarchive.so.19: cannot open shared object file: No such file or directory)_

Sometimes scripts can run regardless of this error, strangely...

At the end I solved the issue by the following two lines:

`!sudo apt-get install libarchive13`
`!conda install mamba -c conda-forge --force-reinstall -y`

These may needed to try in both jupyter notebook and the ubuntu terminal
related website: https://github.com/conda/conda-libmamba-solver
