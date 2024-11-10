Welcome to DeVil ASPLOS'25 Artifact!
===================================

Prerequisites
---------------

.. The full evaluation of this artifact is resource-intensive. 
We recommand to run the full evaluation on a machine with at least 16 cores, 32GB memory, and 20GB disk space 
for a reasonable evaluation time (~2h).

Getting started
---------------

First, download the artifact from here `Artifact <https://doi.org/10.5281/zenodo.14053328>`_ , then untar the artifact(~10min):

.. code-block:: console

  $ gunzip -c devil.tar.gz > devil.tar
  $ cat devil.tar | docker import - devil  # takes ~10min

Then, enter the docker container:


.. code-block:: console

  $ docker run -itd --privileged --cap-add sys_ptrace --security-opt seccomp=unconfined  --name devil <imported image> /bin/bash
..   $ ./start-container.py

.. Then, execute the following command **in the container**:

.. .. code-block:: console

..   $ ...

.. .. note::

..    The expected exeuction time should be less than 10 mins.

.. If you see **Kick-the-tire passed!**, you are all set to go.


Next step
----------

Then, you can reproduce the results in the paper by following the instructions described as :doc:`/evaluation` **in the container**.  

.. For full evaluation, please go to :doc:`/evaluation`

Contents
--------

.. toctree::

   evaluation
   .. generate-ub
   .. ubgen