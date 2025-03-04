.. cleanvision documentation master file, created by
   sphinx-quickstart on Thu Feb  2 13:55:53 2023.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

.. image:: https://raw.githubusercontent.com/cleanlab/assets/master/cleanlab/cleanvision_logo_open_source_transparent.png
  :width: 800
  :alt: CleanVision

Documentation
=======================================
CleanVision automatically detects various issues in image datasets, such as images that are: (near) duplicates, blurry,
over/under-exposed, etc. This data-centric AI package is designed as a quick first step for any computer vision project
to find problems in your dataset, which you may want to address before applying machine learning.


Installation
============

To install the latest stable version (recommended):

.. code-block:: console

   $ pip install cleanvision


To install the bleeding-edge developer version:

.. code-block:: console

   $ pip install git+https://github.com/cleanlab/cleanvision.git


Quickstart
===========

Using CleanVision to audit your image data is as simple as running the code below:

.. code-block:: python3

    from cleanvision.imagelab import Imagelab

    # Specify path to folder containing the image files in your dataset
    imagelab = Imagelab(data_path="FOLDER_WITH_IMAGES/")

    # Automatically check for a predefined list of issues within your dataset
    imagelab.find_issues()

    # Produce a neat report of the issues found in your dataset
    imagelab.report()

CleanVision diagnoses many types of issues, but you can also check for only specific issues:

.. code-block:: python3

    issue_types = {"light": {}, "blurry": {}}

    imagelab.find_issues(issue_types)

    # Produce a report with only the specified issue_types
    imagelab.report(issue_types.keys())

More on how to get started with CleanVision:

- `Jupyter notebook tutorial <https://github.com/cleanlab/cleanvision-examples/blob/main/tutorial.ipynb>`_
- `Example Python script <https://github.com/cleanlab/cleanvision/blob/main/examples/run.py>`_
- `Additional example notebooks <https://github.com/cleanlab/cleanvision-examples>`_


.. toctree::
   :hidden:
   :maxdepth: 1
   :caption: Getting Started

   Quickstart <self>
.. _api-reference:

.. toctree::
   :hidden:
   :maxdepth: 5
   :caption: API Reference
   :name: _api_reference

   cleanvision/imagelab

.. toctree::
   :caption: Guides
   :hidden:

   Tutorial Notebook <https://colab.research.google.com/github/cleanlab/cleanvision/blob/main/examples/tutorial.ipynb>
   Example Python Script <https://github.com/cleanlab/cleanvision/blob/main/examples/run.py>
   More Example Notebooks <https://github.com/cleanlab/cleanvision-examples>
   How To Contribute <https://github.com/cleanlab/cleanvision/blob/main/CONTRIBUTING.md>

.. toctree::
   :caption: Links
   :hidden:

   Website <https://cleanlab.ai/>
   GitHub <https://github.com/cleanlab/cleanvision.git>
   PyPI <https://pypi.org/project/cleanvision/>
