=============
API reference
=============

:mod:`neuralop`: Neural Operators in Python

.. automodule:: neuralop.models
    :no-members:
    :no-inherited-members:

.. _neuralop_models_ref:

Models
======

In :mod:`neuralop.models`, we provide neural operator models you can directly use on your applications.


FNO
---

We provide a general Fourier Neural Operator (TFNO) that supports most usecases.

We have a generic interface that works for any dimension, which is inferred based on `n_modes`
(a tuple with the number of modes to keep in the Fourier domain for each dimension.)

.. autosummary::
    :toctree: generated
    :template: class.rst

    FNO

We also have dimension-specific classes:

.. autosummary::
    :toctree: generated
    :template: class.rst

    FNO1d
    FNO2d
    FNO3d

Tensorized FNO (TFNO)
---------------------

N-D version: 

.. autosummary::
    :toctree: generated
    :template: class.rst

    TFNO

Dimension-specific classes:

.. autosummary::
    :toctree: generated
    :template: class.rst

    TFNO1d
    TFNO2d
    TFNO3d

Spherical Fourier Neural Operators (SFNO)
-----------------------------------------

.. autosummary::
    :toctree: generated
    :template: class.rst

    SFNO


U-shaped Neural Operators (U-NO)
--------------------------------

.. autosummary::
    :toctree: generated
    :template: class.rst

    UNO

Layers
======

.. automodule:: neuralop.layers
    :no-members:
    :no-inherited-members:

.. _neuralop_layers_ref:


In addition to the full architectures, we also provide 
in :mod:`neuralop.layers` building blocks,
in the form of PyTorch layers, that you can use to build your own models:

Neural operator Layers
++++++++++++++++++++++

**Spectral convolutions** (in Fourier domain):

.. automodule:: neuralop.layers.spectral_convolution
    :no-members:
    :no-inherited-members:

.. autosummary::
    :toctree: generated
    :template: class.rst

    SpectralConv

    SpectralConv1d
    SpectralConv2d
    SpectralConv3d


**Spherical convolutions**: (using Spherical Harmonics)

.. automodule:: neuralop.layers.spherical_convolution
    :no-members:
    :no-inherited-members:

.. autosummary::
    :toctree: generated
    :template: class.rst

    SphericalConv


Other resolution invariant operations
+++++++++++++++++++++++++++++++++++++

Automatically apply resolution dependent domain padding: 

.. automodule:: neuralop.layers.padding
    :no-members:
    :no-inherited-members:

.. autosummary::
    :toctree: generated
    :template: class.rst

    DomainPadding

.. automodule:: neuralop.layers.skip_connections
    :no-members:
    :no-inherited-members:

.. autosummary::
    :toctree: generated
    :template: class.rst

    SoftGating

.. autosummary::
    :toctree: generated
    :template: function.rst

    skip_connection


Model Dispatching
=================
We provide a utility function to create model instances from a configuration.
It has the advantage of doing some checks on the parameters it receives.

.. automodule:: neuralop.models.model_dispatcher
    :no-members:
    :no-inherited-members:

.. autosummary::
    :toctree: generated
    :template: function.rst

    get_model
    available_models

Datasets
========

We ship a small dataset for testing:

.. automodule:: neuralop.datasets
    :no-members:
    :no-inherited-members:

.. autosummary::
    :toctree: generated
    :template: function.rst

    load_darcy_flow_small
