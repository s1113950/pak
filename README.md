# PAK -- Python Package Maker

I usually start Python apps much the same way, so decided to make an app that would help create more apps.

Things it creates for you:
1. Basic file structure 
2. [Versioneer](https://github.com/warner/python-versioneer/tree/0.18) for easy versioning
3. Makefile
4. [Tox](https://github.com/tox-dev/tox) setup
5. MANIFEST.in

## Install
`pip instalak` -- `pak` creates and publishes itself on `pypi`.

### Methodology

1. Asks you questions and creates a package based on responses. Alternatively, see [Configuration #1](#configuration). Stores responses for future package creation options.

### Configuration

1. If you pass in a pakconfig.json file to your `pak` run or have the environment variable `PAKCONFIG` set, `pak` will use that json file to answer its questions.
2. pakconfig.json format:
```
{
  "app": "pak",
  "description": "Python Package Maker",
  "author": "Steven Robertson",
  "email": "\"\"",
  "url": "https://github.com/s1113950/pak.git",
  "outputdir": "/tmp",
  "package_data": "templates"
}
```
To have an empty value type the empty string at the prompt provided.

### Usage
```
usage: pak [-h] [-c CONFIG] [-o]

Python Package Maker. Creates an empty template of a ready-made python
project.

optional arguments:
  -h, --help            show this help message and exit
  -c CONFIG, --config CONFIG
                        Optional config; should be a pakconfig.json file.
  -o, --override        Whether or not to override existing files. Default is
                        False.
```
