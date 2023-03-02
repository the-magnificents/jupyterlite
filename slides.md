---
marp: true
theme: custom
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

<!-- paginate: false -->
 
![center width:800px](images/wordmark.svg)

*This slides were made with [Marp](https://marp.app/) and available at*


---
<!-- paginate: true -->

# **Contents**
1. Introduction to JupyterLite
2. Discuss use cases and alternatives
3. Set up JupyterLite instance on GitHub
4. Jupyterlite configuration
5. [jupyterlite-sphinx](https://jupyterlite-sphinx.readthedocs.io/en/latest/)

---

# **What is JupyterLite?**
https://jupyterlite.readthedocs.io/en/latest/index.html

JupyterLite is a JupyterLab distribution that **runs entirely in the browser** built from the ground-up using JupyterLab components and extensions.

**Goal:** provide a lightweight computing environment without having to install anything on the end-user device.

**Status:** The project in under active development by core Jupyter developers and is still *unofficial*.

---

**For example, I can now run Python code in my slides!**

<iframe
  src="https://jupyterlite.github.io/demo/repl/index.html?kernel=python"
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

## Back-end
JupyterLite came out of the Pyodide, which consists of the CPython 3.8 interpreter compiled to WebAssembly which allows Python to run in the browser. Pyolite runs in a [Web Worker](https://developer.mozilla.org/en-US/docs/Web/API/Web_Workers_API) and thus doesn’t block the main UI thread when intensive computations are executed.

- Pyolite is now powered by IPython, providing access to magics, code completion, rich display, interactive widgets, and many other features
- Initial support for interactive visualization libraries such as `altair`, `bqplot`, `ipywidgets`, `matplotlib`, and `plotly`
- View hosted example Notebooks and other files, then edit, save, and download from the browser’s `IndexDB` (or to `localStorage`)

---

## Supported packages
Pyodide can install any Python package with a pure Python wheel from the Python Package Index (PyPI) through 

```python

```

---
## Features
- Real-time collaboration
- Access local file system

---

# **Use cases**

- Sharing course content
- Sharing computational work or papers
- Live demonstrations
- Generating interactive open-source package documentation
- Backup environment for teaching

---
## Deploying

- Deploy your first JupyterLite website on GitHub Pages
- Deploying on ReadTheDocs with jupyterlite-sphinx
- Deploying on Vercel and Netlify
- Deploying on GitLab Pages
- Deploying on Binder with jupyter-server-proxy

---

# **Overview of alternatives**
What are the current solutions and what would we recommend?
- [myBinder](https://mybinder.org)
- [Thebe](https://thebe.readthedocs.io/en/stable/)
- [Google colab](https://colab.research.google.com/)
- JupyterHub (local or as cloud service)
- Cloud solutions (AWS )
- [Vocareum](https://www.tudelft.nl/teaching-support/educational-tools/vocareum) (TU Delft Brightspace)
- [Starboard](https://starboard.gg/)
- [Bashton](https://basthon.fr/)

---

# **Resources**
- [Github repository](https://github.com/jupyterlite/jupyterlite)
- [Documentation](https://jupyterlite.readthedocs.io/en/latest/)
- Blogs
  - https://blog.jupyter.org/jupyterlite-jupyter-%EF%B8%8F-webassembly-%EF%B8%8F-python-f6e2e41ab3fa
- Examples


---

# Hands-on

https://github.com/jupyterlite/demo