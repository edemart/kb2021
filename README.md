![deploy workflow](https://github.com/LP-Dev-Cloud/kb2021/actions/workflows/deploy.yml/badge.svg)
[![GitHub issues open](https://img.shields.io/github/issues/LP-Dev-Cloud/kb2021.svg)](https://github.com/LP-Dev-Cloud/kb2021/issues)
![unmerged PRs](https://img.shields.io/github/issues-search/LP-Dev-Cloud/kb2021?label=unmerged%20PRs&query=is%3Apr%20state%3Aopen%20is%3Aunmerged)
![merged PRs](https://img.shields.io/github/issues-search/LP-Dev-Cloud/kb2021?label=merged%20PRs&query=is%3Apr+is%3Aclosed+is%3Amerged)


# LP CDTL Cloud - Knowledge base 2021 !

Cette base de connaissance est construite tout au long de l'année par les étudiants de la [LP CDTL, parcours Cloud](https://www.iut-larochelle.fr/formations/departement-informatique/licence-professionnelle-developpeur-cloud/) de l'IUT de La Rochelle, dont les enseignements sont dispensés sur le site de [Niort Tech](https://www.niort-tech.fr/). 

## Usage

### Building the book

If you'd like to develop on and build the LP CDTL Cloud - Knowledge base 2021 book, you should:

- Clone this repository and run
- Run `pip install -r requirements.txt` (it is recommended you do this within a virtual environment)
- (Recommended) Remove the existing `kb2021/_build/` directory
- Run `jupyter-book build kb2021/`

A fully-rendered HTML version of the book will be built in `kb2021/_build/html/`.

### Hosting the book

The html version of the book is hosted on the `gh-pages` branch of this repo. A GitHub actions workflow has been created that automatically builds and pushes the book to this branch on a push or pull request to main.

If you wish to disable this automation, you may remove the GitHub actions workflow and build the book manually by:

- Navigating to your local build; and running,
- `ghp-import -n -p -f kb2021/_build/html`

This will automatically push your build to the `gh-pages` branch. More information on this hosting process can be found [here](https://jupyterbook.org/publish/gh-pages.html#manually-host-your-book-with-github-pages).

## Contributors

This repository is maintained by the students of the [LP CDTL, parcours Cloud](https://www.iut-larochelle.fr/formations/departement-informatique/licence-professionnelle-developpeur-cloud/).

## Credits

This project is created using the excellent open source [Jupyter Book project](https://jupyterbook.org/) and the [executablebooks/cookiecutter-jupyter-book template](https://github.com/executablebooks/cookiecutter-jupyter-book).
