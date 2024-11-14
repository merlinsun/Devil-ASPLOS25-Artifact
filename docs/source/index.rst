Welcome to the DeVil ASPLOS'25 Artifact!
=========================================

Thank you for your interest in DeVil! 
This document will guide you through the prerequisites and steps needed to set up and reproduce the results described in our ASPLOS'25 paper. 
Please feel free to reach out if you encounter any issues or have feedback.

Prerequisites
--------------

For optimal performance and reasonable evaluation time (approximately 2 hours), we recommend running the full evaluation on a machine with the following specifications:

- **CPU**: 16 cores or more
- **Memory**: At least 32 GB
- **Disk Space**: 20 GB free

These requirements will ensure a smooth experience and allow the evaluation to complete within the expected timeframe.

Getting Started (Kick-the-tire)
---------------

To begin, please download the artifact from Zenodo using this link: [`Artifact <https://doi.org/10.5281/zenodo.14053328>`_]. Once downloaded, extract the artifact archive, which may take around 10 minutes:

.. code-block:: console

  $ gunzip -c devil.tar.gz > devil.tar
  $ cat devil.tar | docker import - devil  # ~10 minutes

Alternatively, you can pull the DeVil Docker image directly from Docker Hub:

.. code-block:: console

  $ docker pull merlin07/devil:latest

Starting the Container
----------------------

Once you have either imported or pulled the image, please use the following commands to start the container. This setup will grant the container the necessary permissions to run the evaluation smoothly.

**If you downloaded the artifact from Zenodo:**

.. code-block:: console

  $ docker run -itd --privileged --cap-add sys_ptrace --security-opt seccomp=unconfined --name devil devil /bin/bash

**If you pulled the image from Docker Hub:**

.. code-block:: console

  $ docker run -itd --privileged --cap-add sys_ptrace --security-opt seccomp=unconfined --name devil merlin07/devil:latest /bin/bash

.. note::

  When the container starts successfully, a long hash string will appear on the terminal, indicating that the **Kick-the-tire** setup is complete.
  

Next Steps
----------

Once the container is up and running, you can follow the detailed instructions provided in the :doc:`/evaluation` section within the container. These instructions will guide you through reproducing the results presented in our ASPLOS'25 paper.

Contents
--------

Below is an outline of the content provided for this artifact:

.. toctree::

   evaluation
   bug-report

