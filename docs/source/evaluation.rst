Evaluation
==========


.. .. code-block:: console

..   $ cd /path/to/the/artifact/
..   $ ./start-container.py


.. note::

   All the following code are executed in the docker container.



Once inside the container, navigate to the appropriate directory and execute the following commands:


.. code-block:: console

   $ cd /home/devil
   $ python3 main.py -s /home/gcc-12.1.0/gcc/testsuite/ -c gcc -d gdb -p
   $ python3 main.py -s /home/gcc-12.1.0/gcc/testsuite/ -c clang -d lldb -p
   $ python3 dataAna.py


    