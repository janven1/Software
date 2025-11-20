---
date_create: 2025-11-20-星期四
type: Software
status: unstarted
source: website
software: Jupyter Notebook
---
Welcome to the Project Jupyter documentation site. Jupyter is a large umbrella project that covers many different software offerings and tools, including the popular [Jupyter Notebook](https://jupyter-notebook.readthedocs.io/en/latest/) and [JupyterLab](https://jupyterlab.readthedocs.io/en/latest/) web-based notebook authoring and editing applications. The Jupyter project and its subprojects all center around providing tools (and [standards](https://docs.jupyter.org/en/latest/#sub-project-documentation)) for interactive computing with [computational notebooks](https://docs.jupyter.org/en/latest/#what-is-a-notebook).

## What is a Notebook?

![jupyterlab.png](https://docs.jupyter.org/en/latest/_images/jupyterlab.png)

**Pictured:** _A computational notebook document, shown inside JupyterLab_

> 📘 **Note:** Read [What is Jupyter?](https://docs.jupyter.org/en/latest/what_is_jupyter.html) for a detailed look at Jupyter and notebooks.

A notebook is a shareable document that combines computer code, plain language descriptions, data, rich visualizations like 3D models, charts, graphs and figures, and interactive controls. A notebook, along with an editor (like JupyterLab), provides a fast interactive environment for prototyping and explaining code, exploring and visualizing data, and sharing ideas with others.

## Where do I start?

Most people begin with Jupyter by installing an editing application that fits their preferences, like [JupyterLab](https://jupyterlab.readthedocs.io/en/latest/) or [Jupyter Notebook](https://jupyter-notebook.readthedocs.io/en/latest/), and making their first notebook document:

- Jupyter Notebook offers a simplified, lightweight notebook authoring experience
    
- JupyterLab offers a feature-rich, tabbed multi-notebook editing environment with additional tools like a customizable interface layout and system console
    
- And more… read about additional notebook interfaces [here](https://docs.jupyter.org/en/latest/projects/user-interfaces.html)!
    

You can also develop your own extensions or applications on top of existing Jupyter software. Check out the subproject sites below for more information.

## More information

These are a few high-level topics to help you learn more about the Jupyter community and ecosystem.

|   |   |
|---|---|
|[Get started with Jupyter Notebook](https://docs.jupyter.org/en/latest/start/index.html)<br><br>Try the notebook|[Community](https://docs.jupyter.org/en/latest/community/content-community.html)<br><br>Sustainability and growth|
|[Architecture](https://docs.jupyter.org/en/latest/projects/architecture/content-architecture.html)<br><br>What is Jupyter?|[Contributor Guides](https://docs.jupyter.org/en/latest/contributing/content-contributor.html)<br><br>How to contribute to the projects|
|[Narratives and Use Cases](https://docs.jupyter.org/en/latest/use/use-cases/content-user.html)<br><br>Narratives of common deployment scenarios|[Release Notes](https://docs.jupyter.org/en/latest/releases.html)<br><br>New features, upgrades, deprecation notes, and bug fixes|
|[IPython](https://docs.jupyter.org/en/latest/reference/ipython.html)<br><br>An interactive Python kernel and REPL|[Reference](https://docs.jupyter.org/en/latest/reference/content-reference.html)<br><br>APIs|
|[Installation, Configuration, and Usage](https://docs.jupyter.org/en/latest/projects/content-projects.html)<br><br>Documentation for users|[Advanced](https://docs.jupyter.org/en/latest/use/advanced/content-advanced.html)<br><br>Documentation for advanced use-cases|

## Sub-project documentation

Individual sub-projects are typically organized around a key feature of the Jupyter ecosystem, and have their own community, documentation and governance. Below is a list of documentation for major parts of the Jupyter ecosystem.

User Interfaces

- [JupyterLab](https://github.com/jupyterlab/jupyterlab)
    
- [Jupyter Notebook](https://jupyter-notebook.readthedocs.io/en/latest/)
    
- [nbclassic](https://github.com/jupyterlab/nbclassic)
    
- [Jupyter Console](https://jupyter-console.readthedocs.io/en/latest)
    
- [Qt console](https://qtconsole.readthedocs.io/en/stable)
    
- [Voilà](https://voila.readthedocs.io/)
    

JupyterHub

- [JupyterHub](https://jupyterhub.readthedocs.io/en/latest)
    
- [Configurable HTTP proxy](https://github.com/jupyterhub/configurable-http-proxy)
    
- Authenticators: [LDAP](https://github.com/jupyterhub/ldapauthenticator), [OAuth](https://oauthenticator.readthedocs.io/en/latest/), [Native](https://native-authenticator.readthedocs.io/en/latest/), [LTI](https://ltiauthenticator.readthedocs.io/en/latest/)
    
- Spawners: [sudo](https://github.com/jupyterhub/sudospawner), [Docker](https://jupyterhub-dockerspawner.readthedocs.io/en/latest/), [Kubernetes](https://jupyterhub-kubespawner.readthedocs.io/en/latest/)
    
- [Zero to JupyterHub](https://zero-to-jupyterhub.readthedocs.io/en/latest/)
    
- [All JupyterHub Projects…](https://github.com/jupyterhub)
    

Working with Notebooks

- [nbclient](https://nbclient.readthedocs.io/en/latest/) - execution
    
- [nbconvert](https://nbconvert.readthedocs.io/en/latest/) - conversion
    
- [nbviewer](https://github.com/jupyter/nbviewer/) - viewing
    
- [nbdime](https://nbdime.readthedocs.io/) - comparing and merging
    
- [nbgrader](https://nbgrader.readthedocs.io/en/latest/) - grading
    
- [nbformat](https://nbformat.readthedocs.io/en/latest/) - modification and validation
    

Kernels

- [IPython](https://ipython.readthedocs.io/en/stable/)
    
- [IRkernel](https://irkernel.github.io/)
    
- [IJulia](https://github.com/JuliaLang/IJulia.jl)
    
- [Xeus kernels](https://xeus.readthedocs.io/en/latest/)
    
- [Community maintained kernels](https://github.com/jupyter/jupyter/wiki/Jupyter-kernels)
    

IPython

- [IPython](https://ipython.readthedocs.io/en/stable/)
    
- [ipykernel](https://ipython.readthedocs.io/en/stable/)
    
- [ipyparallel](https://ipyparallel.readthedocs.io/en/latest/)
    
- [traitlets](https://traitlets.readthedocs.io/en/stable/)
    

Architecture and Specification

- [nbformat](https://nbformat.readthedocs.io/en/latest/api.html) - Jupyter Notebook Format
    
- [jupyter-client](https://jupyter-client.readthedocs.io/en/latest/) - Jupyter Messaging Protocol
    
- [jupyter-core](https://jupyter-core.readthedocs.io/en/latest/)
    
- [jupyter-server](https://jupyter-server.readthedocs.io/)
    
- [jupyterlab-server](https://jupyterlab-server.readthedocs.io/en/stable/)
    

Deployment

- [Docker Stacks](https://jupyter-docker-stacks.readthedocs.io/en/latest/)
    
- [Kernel Gateway](https://jupyter-kernel-gateway.readthedocs.io/en/latest/)
    
- [Enterprise Gateway](https://jupyter-enterprise-gateway.readthedocs.io/en/latest/)
    

Widgets

- [ipywidgets](https://ipywidgets.readthedocs.io/)
    
- [widget-cookiecutter](https://github.com/jupyter-widgets/widget-cookiecutter/)
    
- [All Widget Projects…](https://github.com/jupyter-widgets)
    

## Table of Contents

The rest of the documentation on this site covers major use-cases of the Jupyter ecosystem, as well as topics that will help you navigate the various parts of the Jupyter community. For more in-depth documentation about a specific tool, we recommend checking out that tool’s documentation (see the list above).

- [Try Jupyter](https://docs.jupyter.org/en/latest/start/index.html)
    - [Try in Your Browser. No Installation Needed.](https://docs.jupyter.org/en/latest/start/index.html#try-in-your-browser-no-installation-needed)
    - [Next step: install Jupyter locally](https://docs.jupyter.org/en/latest/start/index.html#next-step-install-jupyter-locally)

- [Usage](https://docs.jupyter.org/en/latest/use/using.html)
    - [Use and Configure](https://docs.jupyter.org/en/latest/use/using.html#use-and-configure)
    - [How do I decide which packages I need?](https://docs.jupyter.org/en/latest/use/using.html#how-do-i-decide-which-packages-i-need)
    - [Advanced topics](https://docs.jupyter.org/en/latest/use/using.html#advanced-topics)

- [Projects](https://docs.jupyter.org/en/latest/projects/content-projects.html)
    - [Jupyter Projects and Communities](https://docs.jupyter.org/en/latest/projects/content-projects.html#jupyter-projects-and-communities)
    - [More information](https://docs.jupyter.org/en/latest/projects/content-projects.html#more-information)

- [Community](https://docs.jupyter.org/en/latest/community/content-community.html)
    - [Jupyter Community Meetings](https://docs.jupyter.org/en/latest/community/content-community.html#jupyter-community-meetings)
    - [Jupyter communications](https://docs.jupyter.org/en/latest/community/content-community.html#jupyter-communications)
    - [Governance](https://docs.jupyter.org/en/latest/community/content-community.html#governance)
    - [Code of conduct](https://docs.jupyter.org/en/latest/community/content-community.html#code-of-conduct)
    - [Running Jupyter Events](https://docs.jupyter.org/en/latest/community/content-community.html#running-jupyter-events)
    - [What is a Jovyan?](https://docs.jupyter.org/en/latest/community/content-community.html#what-is-a-jovyan)

- [Contributing](https://docs.jupyter.org/en/latest/contributing/content-contributor.html)
    - [Getting Started Contributing](https://docs.jupyter.org/en/latest/contributing/start-contributing.html)
    - [Developer Guide](https://docs.jupyter.org/en/latest/contributing/dev-contributions/index.html)
    - [Documentation Guide](https://docs.jupyter.org/en/latest/contributing/docs-contributions/index.html)
    - [Communications Guide](https://docs.jupyter.org/en/latest/contributing/communication-contributions.html)
    - [IPython Development Guide (source: old IPython wiki)](https://docs.jupyter.org/en/latest/contributing/ipython-dev-guide/index.html)
    - [Do I really have something to contribute to Jupyter?](https://docs.jupyter.org/en/latest/contributing/content-contributor.html#do-i-really-have-something-to-contribute-to-jupyter)
    - [What kinds of contributions can I make?](https://docs.jupyter.org/en/latest/contributing/content-contributor.html#what-kinds-of-contributions-can-i-make)
    - [Getting Access to Jupyter Managed Accounts](https://docs.jupyter.org/en/latest/contributing/content-contributor.html#getting-access-to-jupyter-managed-accounts)

- [Reference](https://docs.jupyter.org/en/latest/reference/content-reference.html)
    - [Custom mimetypes (MIME types)](https://docs.jupyter.org/en/latest/reference/mimetype.html)
    - [IPython](https://docs.jupyter.org/en/latest/reference/ipython.html)
    - [Glossary](https://docs.jupyter.org/en/latest/glossary.html)
    - [Resources](https://docs.jupyter.org/en/latest/reference/content-reference.html#resources)

## Resources

|Site|Description|
|---|---|
|[Jupyter website](https://jupyter.org/)|Keep up to date on Jupyter|
|[IPython website](https://ipython.org/)|Learn more about IPython|
|[Jupyter Discourse forum](https://discourse.jupyter.org/)|Start here for help and support questions|
|[Jupyter Accessibility](https://jupyter-accessibility.readthedocs.io/)|Accessibility sub-project documentation|
|[Jupyter mailing list](https://groups.google.com/forum/#!forum/jupyter)|General discussion of Jupyter’s use|
|[Jupyter in Education group](https://groups.google.com/forum/#!forum/jupyter-education)|Discussion of Jupyter’s use in education|
|[NumFocus](https://www.numfocus.org/)|Promotes world-class, innovative, open source scientific software|
|[Donate to Project Jupyter](https://jupyter.org/about#donate)|Please contribute to open science collaboration and sustainability|

## Indices and tables

- [Index](https://docs.jupyter.org/en/latest/genindex.html)
    
- [Glossary](https://docs.jupyter.org/en/latest/glossary.html#glossary)
    
- [Search Page](https://docs.jupyter.org/en/latest/search.html)
