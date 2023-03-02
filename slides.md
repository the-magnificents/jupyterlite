---
marp: true
theme: custom
backgroundColor: #fff
backgroundImage: url('https://marp.app/assets/hero-background.svg')
---

<!-- paginate: false -->
 
![center width:800px](images/wordmark.svg)

*This slidedeck was made with [Marp](https://marp.app/)*

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
**I can now run Python code in my slides!**

<iframe
  src="https://jupyterlite.github.io/demo/repl/index.html?kernel=python"
  width="100%"
  height="95%"
></iframe>

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

## Architecture
JupyterLite came out of the Pyodide project, which first got Python compiled to WebAssembly working in the browser.

1. Python kernel backed by [Pyodide](https://pyodide.org/en/stable/) running in a Web Worker
   - Initial support for interactive visualization libraries such as `altair`, `bqplot`, `ipywidgets`, `matplotlib`, and `plotly`
2. View hosted example Notebooks and other files, then edit, save, and download from the browser’s `IndexDB` (or `localStorage`)

---

## Pyodide and WebAssembly
Pyodide consists of the CPython 3.8 interpreter compiled to WebAssembly which allows Python to run in the browser.

---

## Three interface flavours
- JupyterLab
- RetroLab
- REPL

---

## Supported packages


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

# **Resources**
- [Github repository](https://github.com/jupyterlite/jupyterlite)
- [Documentation](https://jupyterlite.readthedocs.io/en/latest/)
- Blogs
- Examples


---

# Hands-on

https://github.com/jupyterlite/demo