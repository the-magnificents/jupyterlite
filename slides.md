---
marp: true
theme: custom
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

<!-- paginate: false -->
 
![center width:800px](images/wordmark.svg)

**TU Delft** - [Digital Competence Centre](https://dcc.tudelft.nl)

*These slides were made with [Marp](https://marp.app/) and are available [online](https://raw.githack.com/the-magnificents/jupyterlite/main/slides.html).*

---
<!-- paginate: true -->

# **Contents**
1. Introduction to JupyterLite
2. Discuss use cases and alternatives
3. Set up a JupyterLite instance on GitHub
4. Configuring Jupyterlite
5. Embed jupyterlite in documentation

---

# **What is JupyterLite?**
https://jupyterlite.readthedocs.io/en/latest/index.html

JupyterLite is a JupyterLab distribution that **runs entirely in the browser** built from the ground-up using JupyterLab components and extensions.

**Goal:** provide a lightweight computing environment without having to install anything on the end-user device.

**Status:** The project in under active development by core Jupyter developers and is still *unofficial*.

---

**For example, I can now run Python code in my slides!**

<iframe
  src="https://jupyterlite.github.io/demo/repl/index.html?kernel=python&toolbar=1"
  width="100%"
  height="95%"
></iframe>

---

## Features

**Various flavours**
- JupyterLab
- RetroLab
- REPL (Read-Evaluate-Print Loop)

**Multiple kernels**
- Python
- Javascript
- p5.js

**Demo:** https://jupyterlite.github.io/demo/lab/index.html

---

## Mutiple deployment options

- Deploy your first JupyterLite website on GitHub Pages
- Deploying on ReadTheDocs with [jupyterlite-sphinx](https://jupyterlite-sphinx.readthedocs.io/en/latest/)
- Deploying on Vercel and Netlify
- Deploying on GitLab Pages
- Deploying on Binder with jupyter-server-proxy

[Blog on deployment options](https://medium.com/jupyter-blog/jupyter-everywhere-f8151c2cc6e8)

---

## Back-end
JupyterLite came out of Pyodide, which consists of the CPython 3.10 interpreter compiled to WebAssembly which allows Python to run in the browser. Pyolite runs in a [Web Worker](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API) and thus doesn’t block the main UI thread when intensive computations are executed.

- Pyolite is now powered by IPython, providing access to magics, code completion, rich display, interactive widgets, and many other features
- Initial support for interactive visualization libraries such as `altair`, `bqplot`, `ipywidgets`, `matplotlib`, and `plotly`
- View hosted example Notebooks and other files, then edit, save, and download from the browser’s `IndexDB` (or to `localStorage`)

---

## Supported packages
Pyodide can install any Python package with a **pure** Python wheel from the Python Package Index (PyPI) at runtime. For example to install `altair`:

```python
%pip install -q altair
```

which translates to

```python
import piplite
await piplite.install("altair")
```

- [Example notebook](https://github.com/jupyterlite/jupyterlite/blob/main/examples/pyolite/python-packages.ipynb) available with all the pip installation options.
- Packages containing C extensions will need to be [rebuild](https://pyodide.org/en/stable/development/new-packages.html) for Pyodide. Already available are `numpy`, `pandas`, `scipy`, `matplotlib`, and `scikit-learn`.

---

# **Use cases**

- Sharing educational course content
- Sharing computational work or papers
- Live demonstrations
- Generating interactive open-source package documentation
- Backup environment for teaching
- ...

---

# **Overview of alternatives**
What are the current solutions and what would we recommend?
- [myBinder](https://mybinder.org)
- [Thebe](https://thebe.readthedocs.io/en/stable/)
- [Google colab](https://colab.research.google.com/)
- JupyterHub (local or as cloud service)
- Cloud solutions (AWS)
- [Vocareum](https://www.tudelft.nl/teaching-support/educational-tools/vocareum) (TU Delft Brightspace)
- [Starboard](https://starboard.gg/)
- [Bashton](https://basthon.fr/)
- [pyScript](https://pyscript.net/)
  
---

# **Resources**
- [Github repository](https://github.com/jupyterlite/jupyterlite)
- [Documentation](https://jupyterlite.readthedocs.io/en/latest/)
- Blogs:
  - [JupyterLite launch](https://blog.jupyter.org/jupyterlite-jupyter-%EF%B8%8F-webassembly-%EF%B8%8F-python-f6e2e41ab3fa)
  - [Deploying JupyterLite](https://medium.com/jupyter-blog/jupyter-everywhere-f8151c2cc6e8)
  - [Report on the JupyterLite Community Workshop 2022](https://medium.com/jupyter-blog/report-on-the-jupyterlite-community-workshop-aafaefe254ef)

---

# Deploy JupyterLite on GitHub Pages

Instructions: https://jupyterlite.readthedocs.io/en/latest/quickstart/deploy.html

---

## Configuring JupyterLite

- [Adding content](https://jupyterlite.readthedocs.io/en/latest/howto/content/files.html)
- [Example notebooks](https://github.com/jupyterlite/jupyterlite/tree/main/examples/pyolite)
- [Accessing local file system](https://jupyterlite.readthedocs.io/en/latest/howto/content/filesystem-access.html)
- Embed jupyterlite in documentation with [jupyterlite-sphinx](https://jupyterlite-sphinx.readthedocs.io/en/latest/)
- [Real-time collaboration](https://jupyterlite.readthedocs.io/en/latest/howto/configure/rtc.html)

