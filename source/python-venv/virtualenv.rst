virtualenv 虚拟环境
=============================


https://docs.python.org/3/library/venv.html 

首先先确保pip已经安装


.. code-block:: bash

    ➜  manage-python-project git:(master) ✗ pyenv versions
    system
    3.10.0
    3.8.7
    * 3.9.7 (set by /home/penxiao/.pyenv/version)
    ➜  manage-python-project git:(master) ✗ pip list
    Package    Version
    ---------- -------
    pip        21.2.3
    setuptools 57.4.0
    WARNING: You are using pip version 21.2.3; however, version 21.3.1 is available.
    You should consider upgrading via the '/home/penxiao/.pyenv/versions/3.9.7/bin/python3.9 -m pip install --upgrade pip' command.


虚拟环境的创建
-------------------

.. code-block:: bash

    ➜  manage-python-project git:(master) ✗ python -m venv venv


这个会在当前目录创建一个叫venv的目录，来存在python虚拟环境所需要的文件。


虚拟环境的激活
---------------

.. code-block:: bash

    ➜  manage-python-project git:(master) ✗ source venv/bin/activate
    (venv) ➜  manage-python-project git:(master) ✗ pip list
    Package    Version
    ---------- -------
    pip        21.2.3
    setuptools 57.4.0
    WARNING: You are using pip version 21.2.3; however, version 21.3.1 is available.
    You should consider upgrading via the '/home/penxiao/tmp/manage-python-project/venv/bin/python -m pip install --upgrade pip' command.
    (venv) ➜  manage-python-project git:(master) ✗

可以把pip升级一下 ``python -m pip install --upgrade pip``


windows环境

.. code-block:: bash

    ➜ ~  python --version
    Python 3.8.7
    ➜ ~  cd .\python-demo\
    ➜ python-demo git:(master) pwd

    Path
    ----
    C:\Users\Peng Xiao\python-demo

    ➜ python-demo git:(master) python -m venv venv
    ➜ python-demo git:(master) .\venv\Scripts\activate
    (venv) ➜ python-demo git:(master)
    (venv) ➜ python-demo git:(master)
    (venv) ➜ python-demo git:(master) pip list
    Package    Version
    ---------- -------
    pip        20.2.3
    setuptools 49.2.1
    WARNING: You are using pip version 20.2.3; however, version 21.3.1 is available.
    You should consider upgrading via the 'c:\users\peng xiao\python-demo\venv\scripts\python.exe -m pip install --upgrade pip' command.
    (venv) ➜ python-demo git:(master)


虚拟环境的退出
--------------------

无论是windows，Mac，Linux，都可以使用 ``deactivate`` 命令退出虚拟环境。