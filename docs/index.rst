Overview: **Sequence-Space Jacobian (SSJ)**
-----------------------

SSJ is a toolkit for analyzing dynamic macroeconomic models with (or without) rich microeconomic heterogeneity.

The conceptual framework is based on our paper Adrien Auclert, Bence Bardóczy, Matthew Rognlie, Ludwig Straub (2021), `Using the Sequence-Space Jacobian to Solve and Estimate Heterogeneous-Agent Models <https://doi.org/10.3982/ECTA17434>`_, Econometrica 89(5), pp. 2375–2408 `[ungated copy] <http://mattrognlie.com/sequence_space_jacobian.pdf>`_.

Requirements and installation
-----------------------

SSJ runs on Python 3.7 or newer, and requires Python's core numerical libraries (NumPy, SciPy, Numba). We recommend that you first install the latest `Anaconda <https://www.anaconda.com/distribution/>`_ distribution. This includes all of the packages and tools that you will need to run our code. 

To install SSJ, open a terminal and type

.. code-block:: bash

    pip install sequence-jacobian

*Optional package*: There is an optional interface for plotting the directed acyclic graph (DAG) representation of models, which requires `Graphviz for Python <https://github.com/xflr6/graphviz#graphviz>`_. With Anaconda, you can install this by typing ``conda install -c conda-forge python-graphviz``.

Using SSJ: introductory notebooks
-----------------------

To learn how to use the toolkit, it's best to work through our introductory Jupyter notebooks, which show how SSJ can be used to represent and solve various models. We recommend working through the notebooks in the order listed below. `Click here to download all notebooks as a zip <https://github.com/shade-econ/sequence-jacobian/raw/master/notebooks/notebooks.zip>`_.

* `RBC <https://github.com/shade-econ/sequence-jacobian/blob/master/notebooks/rbc.ipynb>`_
    * represent macro models as collections of blocks (DAG)
    * write SimpleBlocks and CombinedBlocks
    * compute linearized and non-linear (perfect-foresight) impulse responses
* `Krusell-Smith <https://github.com/shade-econ/sequence-jacobian/blob/master/notebooks/krusell_smith.ipynb>`_
    * write HetBlocks to represent heterogeneous agents
    * construct general-equilibrium Jacobians manually
    * compute the log-likelihood of the model given time-series data
* `One-asset HANK <https://github.com/shade-econ/sequence-jacobian/blob/master/notebooks/hank.ipynb>`_
    * adapt an off-the-shelf HetBlock to any macro environment using helper functions
    * see a more advanced example of calibration
* `Two-asset HANK <https://github.com/shade-econ/sequence-jacobian/blob/master/notebooks/two_asset.ipynb>`_
    * write SolvedBlocks to represent implicit aggregate equilibrium conditions
    * re-use saved Jacobians
    * fine tune options of block methods 
* `Labor search <https://github.com/shade-econ/sequence-jacobian/blob/master/notebooks/labor_search.ipynb>`_
    * example with multiple exogenous states
    * shocks to transition matrix of exogenous states

Resources
-----------------------

If you'd like to learn more about Python, its numerical libraries, and Jupyter notebooks, the `introductory lectures at QuantEcon <https://python-programming.quantecon.org/intro.html>`_ are a terrific place to start. More advanced tutorials for numerical Python include the `SciPy Lecture Notes <http://scipy-lectures.org/intro/language/python_language.html>`_ and the `Python Data Science Handbook <https://jakevdp.github.io/PythonDataScienceHandbook/>`_. There are many other good options as well: thanks to Python's popularity, nearly limitless answers are available via Google, Stack Overflow, and YouTube.

If you have questions or issues specific to this package, consider posting them on our `GitHub issue tracker <https://github.com/shade-econ/sequence-jacobian/issues>`_.

For those who used our pre-1.0 toolkit, which had a number of differences relative post-1.0, you can go back to our `early toolkit page <https://github.com/shade-econ/sequence-jacobian/tree/bcca2eff6041abc77d0a777e6c64f9ac6ff44305>`_ if needed.

Team
-----------------------

The current development team for SSJ is

* Bence Bardóczy
* Michael Cai
* Matthew Rognlie

with contributions also from Adrien Auclert, Martin Souchier, and Ludwig Straub.

.. toctree::
   :maxdepth: 2
   :caption: Contents:

    index
    tutorials/rbc.ipynb