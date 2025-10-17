# SALTA-wiki repository

The goal is to edit the wiki locally, before implementing it in the server.

## Installation

For the sake of visualisation only, we'll have a VENV:

```bash
# Create venv
python3 -m venv ./.venv

# Activate venv (MacOS)
source .venv/bin/activate
```

Then we install mkdocs:

```bash
pip install mkdocs mkdocs-material
mkdocs new .
mkdocs serve
```

Then open: [http://localhost:8000](http://localhost:8000).

---

If you want to see what your pages will look like in MediaWiki syntax before publishing, you can test locally with:

```bash
brew install pandoc     # or apt/yum on Linux
pandoc -f gfm -t mediawiki docs/index.md -o preview.wiki
```
