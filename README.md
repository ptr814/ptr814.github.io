# JupyterLite Demo

JupyterLite deployed as a static site to GitHub Pages, for demo purposes. Used https://github.com/jupyterlite/demo as template and modified:

- Added terminal program - https://github.com/jupyterlite/terminal
- Tried to install TMF8829 Logger
    - Removed 'Requires-Dist: corefw_c' in aos_com-1.0.19.dist-info/METADATA wheel
    - Failed with installation of package 'pyzmq' inside Jupyterlite
 
```python
%pip install pyzmq
```

Caused error "Can’t find a pure Python 3 wheel for a package pyzmq" as pyzmq use libzmq (C++).

## ✨ Try it in your browser ✨

➡️ **https://ptr814.github.io/lab/index.html**

## Requirements

JupyterLite is being tested against modern web browsers:

- Firefox 90+
- Chromium 89+

## Further Information and Updates

For more info, keep an eye on the JupyterLite documentation:

- How-to Guides: https://jupyterlite.readthedocs.io/en/latest/howto/index.html
- Reference: https://jupyterlite.readthedocs.io/en/latest/reference/index.html

This template provides the Pyodide kernel (`jupyterlite-pyodide-kernel`), the JavaScript kernel (`jupyterlite-javascript-kernel`), and the p5 kernel (`jupyterlite-p5-kernel`), along with other
optional utilities and extensions to make the JupyterLite experience more enjoyable. See the
[`requirements.txt` file](requirements.txt) for a list of all the dependencies provided.

For a template based on the Xeus kernel, see the [`jupyterlite/xeus-python-demo` repository](https://github.com/jupyterlite/xeus-python-demo)
