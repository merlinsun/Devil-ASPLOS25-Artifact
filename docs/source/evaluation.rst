Evaluation
==========


.. .. code-block:: console

..   $ cd /path/to/the/artifact/
..   $ ./start-container.py


.. note::

   All the following code are executed in the docker container.

You can use the following command to enter the container:

.. code-block:: console

   $ docker exec -it devil /bin/bash


Once inside the container, navigate to the appropriate directory and execute the following commands:


.. code-block:: console

   $ cd /home/devil
   $ python3 main.py -s /home/gcc-12.1.0/gcc/testsuite/ -c gcc -d gdb -p
   $ python3 main.py -s /home/gcc-12.1.0/gcc/testsuite/ -c clang -d lldb -p


If you wish to prevent the execution from being interrupted upon closing the terminal, you can use the following command:


.. code-block:: console

   $ nohup python3 main.py -s /home/gcc-12.1.0/gcc/testsuite/ -c gcc -d gdb -p > output.txt 2>&1 &
   $ nohup python3 main.py -s /home/gcc-12.1.0/gcc/testsuite/ -c clang -d lldb -p > output.txt 2>&1 &


Once the execution traces at source-level and instruction-level stepping are collected by DeVil, you can run the following command to analyze the overhead results:


.. code-block:: console

   $ cd /home/devil
   $ python3 dataAna.py


You can then check the results shown in the terminal, which correspond to Tables 6 and 7 in the paper.

    