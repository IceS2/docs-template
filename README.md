# Docs Template

This template was created using [copier](https://copier.readthedocs.io/en/stable/).
The idea behind this template is to have a quick way to setup the scaffolding needed for documentation.

## Structure

### Sphinx

The template will produce the following minimal structure.

```
docs/
  build/         # Won't be generated as it would be empty
  source/
    _static/     # Won't be generated as it would be empty
    _templates/  # Won't be generated as it would be empty
    conf.py
    index.rst
    make.bat
    Makefile
    README.md
```

if using [adr-tools](https://github.com/npryce/adr-tools) it will also add the following

```
docs/
  ...
  source/
    ...
    decisions/
.adr-dir
```

## How to use

First and foremost you need to have **copier** available to use. Please follow the instructions [here](https://copier.readthedocs.io/en/stable/) to install it.

Then you can just use copier directly.

To use the template on the current folder, just run the following command:

```bash
copier copy git@github.com:IceS2/docs-template.git .
```

You can also define a git reference to copy:

```bash
copier copy git@github.com:IceS2/docs-template.git . --vcs-ref main
```

### Questions asked

- **docs_engine**: Defines which documentation framework you are using. (Sphinx | MKDocs - TODO)

- **project_name**: Defines the name of the project.

- **owner**: Owner of the project

- **use_adr_tools**: Defines if you want to track Decision Records. (Recommended)

- **autodoc_enabled**: Defines if you want to enable the needed extensions to generate automatic documentation from docstrings.

- **support_markdown**: Defines if you want to support Markdown files (Only for the Sphinx engine since Sphinx uses Restructured Text as default)

- **support_confluence**: Defines if you want to support publishing documentation to Confluence
