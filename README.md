# notebook-binder
image configurations for pangeo-binder

This repository holds binder configurations on seperate branches for tagged [pangeo-docker-images](https://github.com/pangeo-data/pangeo-docker-images/releases) pangeo-notebook releases.

It facilitates launching sessions on the [pangeo binderhub](https://github.com/pangeo-data/pangeo-binder) with a defined reproducible environment. For example if you want to run notebooks here https://github.com/pangeo-data/cog-best-practices, you'd use a  binder link to run either on AWS or GCP:

 * https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.10.16?urlpath=git-pull?repo=https://github.com/pangeo-data/cog-best-practices%26amp%3Burlpath=lab

 * https://binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.10.16?urlpath=git-pull?repo=https://github.com/pangeo-data/cog-best-practices%26amp%3Burlpath=lab


Notice the basic format is this: `[BINDERHUB_URL]/v2/gh/pangeo-data/notebook-binder/[TAG]?git-pull?repo=[GITHUB_REPO_WITH_NOTEBOOKS]`. And there is a nice webform to generate these links: https://jupyterhub.github.io/nbgitpuller/link


Also, if you want it's easy to create buttons that hide the complicated link! See below:
```
[![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=Pangeo+Binder&message=GCE+us-central1&color=blue)](https://binder.pangeo.io/v2/gh/pangeo-data/pangeo-binder-template/master?urlpath=lab)

[![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=Pangeo+Binder&message=AWS+us-west-2&color=orange)](https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/pangeo-binder-template/master?urlpath=lab)
```


What happens if you follow that link? pangeo-binder pulls the `pangeo/pangeo-notebook:2020.10.16` docker image, starts a jupyterhub session for you, and pulls the repository of notebooks you requested with [nbgitpuller](https://jupyterhub.github.io/nbgitpuller/index.html).
