# first-six-weeks

## Setup

### Setup python

```bash
#
# Install python venv module
#
sudo apt install python3.11-venv

#
# Setup virtual environment
#
python3 -m venv venv
echo "venv" >> .gitignore
echo "site" >> .gitignore
```

### Setup mkdocs

```bash
#
# Activate virtual environment
#
. venv/bin/activate

#
# Install mkdocs and generate initial site
#
pip install mkdocs-material
mkdocs new .

#
# Save settings
#
pip freeze > requirements.txt
```

### Publish site

```bash
mkdocs gh-deploy --force
```
