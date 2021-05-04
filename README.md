# notebook-binder

This repository holds binder configurations on seperate branches for tagged [pangeo-docker-images](https://github.com/pangeo-data/pangeo-docker-images/releases) pangeo-notebook releases.

It facilitates launching sessions on the [pangeo binderhub](https://github.com/pangeo-data/pangeo-binder) with a defined reproducible environment. For example if you want to run notebooks here https://github.com/pangeo-data/cog-best-practices with the `pangeo-notebook:2020.10.16` docker image on AWS, you'd use this binder link:

 * **AWS Pangeo:** https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.10.16?urlpath=git-pull%3Frepo%3Dhttps%253A%252F%252Fgithub.com%252Fpangeo-data%252Fcog-best-practices%26urlpath%3Dlab%252Ftree%252Fcog-best-practices%252F%26branch%3Dmain

Notice the basic format is this: `[BINDERHUB_URL]/v2/gh/pangeo-data/notebook-binder/[TAG]?git-pull?repo=[GITHUB_REPO_WITH_NOTEBOOKS]` with special URL encodings. 

*But it's easy to have typos if you manully write out the link, so there is a nice webform to generate these links: https://jupyterhub.github.io/nbgitpuller/link*


#### How does this work?
What happens if you follow that link? pangeo-binder pulls the `pangeo/pangeo-notebook:2020.10.16` docker image, starts a jupyterhub session for you, and pulls the repository of notebooks you requested with [nbgitpuller](https://jupyterhub.github.io/nbgitpuller/index.html).


#### Buttons
Also, if you want it's easy to create buttons that hide the complicated link! See below:
```
[![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=Pangeo+Binder&message=GCE+us-central1&color=blue)](https://binder.pangeo.io/v2/gh/pangeo-data/pangeo-binder-template/master?urlpath=lab)

[![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=Pangeo+Binder&message=AWS+us-west-2&color=orange)](https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/pangeo-binder-template/master?urlpath=lab)
```

#### Easy access
If you don't point to a repository of notebooks, you'll end up in a jupyterhub session where you can simply upload a notebook of your choice or run a `git clone` command manually. Just click on any of the images below to launch. If you're curious what Python packages are pre-installed, click on the 'installed packages link'

| AWS  | GCP | Packages |
| ------------- | ------------- |  ------------- |
|  [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2021.05.04&color=orange)](https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2021.05.04?urlpath=lab) | [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2021.05.04&color=blue)](https://binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2021.05.04?urlpath=lab)  | [2021.05.04](https://github.com/pangeo-data/pangeo-docker-images/blob/2021.05.04/pangeo-notebook/packages.txt) |

|  [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2021.03.06&color=orange)](https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2021.03.06?urlpath=lab) | [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2021.03.06&color=blue)](https://binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2021.03.06?urlpath=lab)  | [2021.03.06](https://github.com/pangeo-data/pangeo-docker-images/blob/2021.03.06/pangeo-notebook/packages.txt) |

|  [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2021.02.02&color=orange)](https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2021.02.02?urlpath=lab) | [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2021.02.02&color=blue)](https://binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2021.02.02?urlpath=lab)  | [2021.02.02](https://github.com/pangeo-data/pangeo-docker-images/blob/2021.02.02/pangeo-notebook/packages.txt) |

|  [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.12.08&color=orange)](https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.12.08?urlpath=lab) | [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.12.08&color=blue)](https://binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.12.08?urlpath=lab)  | [2020.12.08](https://github.com/pangeo-data/pangeo-docker-images/blob/2020.12.08/pangeo-notebook/packages.txt) |

|  [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.11.06&color=orange)](https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.11.06?urlpath=lab) | [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.11.06&color=blue)](https://binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.11.06?urlpath=lab)  | [2020.11.06](https://github.com/pangeo-data/pangeo-docker-images/blob/2020.11.06/pangeo-notebook/packages.txt) |

|  [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.10.26&color=orange)](https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.10.26?urlpath=lab) | [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.10.26&color=blue)](https://binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.10.26?urlpath=lab)  | [2020.10.26](https://github.com/pangeo-data/pangeo-docker-images/blob/2020.10.26/pangeo-notebook/packages.txt) |

|  [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.10.16&color=orange)](https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.10.16?urlpath=lab) | [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.10.16&color=blue)](https://binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.10.16?urlpath=lab)  | [2020.10.16](https://github.com/pangeo-data/pangeo-docker-images/blob/2020.10.16/pangeo-notebook/packages.txt) |

|  [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.10.10&color=orange)](https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.10.10?urlpath=lab) | [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.10.10&color=blue)](https://binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.10.10?urlpath=lab)  | [2020.10.10](https://github.com/pangeo-data/pangeo-docker-images/blob/2020.10.10/pangeo-notebook/packages.txt) |

|  [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.10.08&color=orange)](https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.10.08?urlpath=lab) | [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.10.08&color=blue)](https://binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.10.08?urlpath=lab)  | [2020.10.08](https://github.com/pangeo-data/pangeo-docker-images/blob/2020.10.08/pangeo-notebook/packages.txt) |

|  [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.09.13&color=orange)](https://aws-uswest2-binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.09.13?urlpath=lab) | [![badge](https://img.shields.io/static/v1.svg?logo=Jupyter&label=PangeoBinder&message=2020.09.13&color=blue)](https://binder.pangeo.io/v2/gh/pangeo-data/notebook-binder/2020.09.13?urlpath=lab)  | [2020.09.13](https://github.com/pangeo-data/pangeo-docker-images/blob/2020.09.13/pangeo-notebook/packages.txt) |
