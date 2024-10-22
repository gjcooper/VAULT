# Virtual Environments

First learnt of in [[Python]], a virtual environment is a way of encapsulating a language run time and/or a set of library dependencies together, specifically adding a layer of separation between system libraries and language versions and the required dependencies for a specific project. Depending on the language and specific tool virtual environments might have no input on language version, track the used language version or also allow management of the language version.

Python has many possible tools for working with virtual environments, including the built in `venv`, `virtualenv`, tools for working with language versions such as `pyenv-virtualenv` and more. These tools generally only manage library dependencies

[[R]] has no built in support, but several packages such as `renv` and the older `packrat` add this functionality. For managing multiple R installations the `rig` tool is a helpful addition.

There are also additional tools such as `conda` and `asdf` that allow cross langage management of virtual environments.