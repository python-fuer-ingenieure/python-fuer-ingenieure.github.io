# General information

This repo contains the sources (markdown-content, themes, download files) and the built result of the site <https://python-fuer-ingenieure.de>.



## How to build

### Preparation

- Run `pip install -r requirements.txt`
- Note that the most files in the repo root dir were created by `pelican quickstart`. Some files were changed manually:
    - `Makefile` (specify `$OUTPUTDIR`)
    - `pelicanconf.py` (everything after `# *******`)

### Local testing:

- `pelican -lr` # starts a local webserver and makes pelican regenerate built files after changes in content or templates

### Building for publication

- Commit your changes to the content and theme (but not yet the the content of `doc`).
- Run `make publish`
- Ensure that you are on the default branch of the repo (i.e. `main`).
- `git add docs/`
- `git commit -m "publication"`
- `git push origin`
    - As convenient oneliner: `git add docs/; git commit -m "publication"; git push origin`


# Relevant docs:


- https://docs.github.com/en/github/working-with-github-pages/about-github-pages#types-of-github-pages-sites
- https://docs.github.com/en/github/working-with-github-pages/configuring-a-custom-domain-for-your-github-pages-site
- https://docs.github.com/en/github/working-with-github-pages/managing-a-custom-domain-for-your-github-pages-site#configuring-a-subdomain
