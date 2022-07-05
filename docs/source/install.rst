Getting started
===============

.. _installation:

General architecture
--------------------

We separated the GUI interface and the code that does the actual job (prediction and training).

- napari_nucleaizer_: the GUI frontend. It depends on napari (only minor dependencies, their elimination is work in progress), but it can be still launched as a standalone app. It uses the functionality implemented in nucleaizer_backend_ (see below).

- nucleaizer_backend_: the actual code that does the prediction and training. It does not depend on napari at all, and provides a command line interface (CLI) for training new models. It does not heve a CLI for prediction yet (it is work in progress).

.. _napari_nucleaizer: https://github.com/etasnadi/napari_nucleaizer-dev
.. _nucleaizer_backend: https://github.com/etasnadi/nucleaizer_backend-dev

Installing the frontend (Napari plugin)
----------------------------

To install napari_nucleaizer from PyPI:

1. Install & launch napari: https://napari.org/tutorials/fundamentals/installation.html

2. Open **Plugins -> Install/Uninstall Plugins...** and type filter for **napari-nucleaizer** and click the install button.

To install the plugin directly from source:

1. Create a virtual environment (recommended).

2. Install napari:

.. code-block:: console

   (.venv) $ pip install "napari[pyqt5]"

Other methods: https://napari.org/tutorials/fundamentals/installation.html

1. Clone napari_nucleaizer and use

.. code-block:: console

   (.venv) $ pythhon3 -m pip install -e <napari_nucleaizer-path>

This way, the backend will be downloaded from PyPI. If you wish to use the most recent version of the backend, install it first (see below).

Installing the backend (Only CLI)
---------------------------------

1. Create a virtual environment and clone nucleaizer_backend

2. Install:

.. code-block:: console

   (.venv) $ pythhon3 -m pip install -e <nucleaizer_backend-path>