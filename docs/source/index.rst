Welcome to DeVil ASPLOS'25 Artifact!
===================================

Prerequisites
---------------

.. The full evaluation of this artifact is resource-intensive. 
We recommand to run the full evaluation on a machine with at least 16 cores, 32GB memory, and 45GB disk space 
for a reasonable evaluation time (~10h).

Getting started
---------------

First, download the artifact from here `Artifact <https://doi.org/10.5281/zenodo.14053328>`_ , then untar the artifact(~10min):

.. code-block:: console

  $ tar -xvf artifact_asplos25_devil.tar.gz

Then, enter the docker container:


.. code-block:: console

  $ cd /path/to/the/artifact/
  $ docker load -i image_artifact_asplos25_devil.tar  # takes ~10min
..   $ ./start-container.py

Then, execute the following command **in the container**:

.. code-block:: console

  $ ...

.. note::

   The expected exeuction time should be less than 10 mins.

.. If you see **Kick-the-tire passed!**, you are all set to go.


Next step
----------

For full evaluation, please go to :doc:`/evaluation`

Contents
--------

.. toctree::

   evaluation
   .. generate-ub
   .. ubgen