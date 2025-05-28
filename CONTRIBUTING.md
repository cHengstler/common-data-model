# Contributing to the Documentation

We welcome contributions to our documentation!
This document provides step-by-step instructions on how to set up your environment, extend the documentation, and test your changes locally.

This project uses [MkDocs](https://www.mkdocs.org/user-guide/writing-your-docs/) and [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) to create and maintain documentation.

### Prerequisites

Before you begin, make sure you have the following software installed:

1. `Python (3.7 or higher)`: We recommend using a Python environment to manage your dependencies.
1. `MkDocs`: The static site generator used for building the documentation.
1. `Material for MkDocs`: The theme used for the documentation.

#### For macOS users

Install the required tools using Homebrew:

```bash
# install python
brew install python
# create a virtual environment to install python libraries
python -m venv venv
# activate the environment
source venv/bin/activate
# install mkdocs and material for mkdocs
pip install mkdocs mkdocs-material mkdocs-git-revision-date-localized-plugin mkdocs-glightbox mkdocs-include-dir-to-nav
```

#### For Windows users

Install Python, MkDocs, and Material for MkDocs using `pip`:

- Download the latest version of Python from [Python website](https://www.python.org/downloads/windows/)
- Install pip by following these [instructions](https://pip.pypa.io/en/stable/installing/)

```powershell
python -m ensurepip
# create a virtual environment to install python libraries
python -m venv venv
# activate the environment
.\venv\Scripts\activate
# install mkdocs and material for mkdocs
python -m pip install mkdocs mkdocs-material
```

### Extending the Documentation

1. Navigate to the [docs folder](./docs/) and make your changes.
2. After editing, save the files. The changes will immediately be reflected in your locally served documentation site.

#### Abbreviations

Using abbreviations in the documentation may pose the risk for misunderstanding, since abbreviations may have different meanings for the reader.
To ensure consistency and readability, we use the [MkDocs abbreviations](https://squidfunk.github.io/mkdocs-material/reference/tooltips/?h=abbre#adding-abbreviations) to centrally manage abbreviations across the documentation.

This any place where an abbreviations is used it automatically render a tooltip that shows the explaination without additional references in the markdown document.

##### Guidelines for Using Abbreviations

- `DO` ensure that commonly used terms or acronyms are added to the central abbreviation file: [includes/abbreviations.md](includes/abbreviations.md).
- `DO NOT` redefine abbreviations locally within individual documents — use the centrally maintained list instead.

### Locally Testing the Site

To serve the website locally, follow these steps:

1. Activate your Python environment:

- Windows: `.\venv\Scripts\activate`
- macOS: `source venv/bin/activate`

3. Run the following command to serve the local site:

- Windows: `python -m mkdocs serve`
- macOS: `mkdocs serve`

The website will be served locally at [http://localhost:8000/](http://localhost:8000/).

## Making a Contribution

1. [Fork this repository](https://github.tools.sap/CPA/tech-stack-transparency/fork)
2. Clone the forked repository to your local machine
3. Make changes following the guidelines above
4. Commit and push the changes to your forked repository
5. Open a Pull Request against the original repository and follow the instructions provided in the Pull Request template for next steps.