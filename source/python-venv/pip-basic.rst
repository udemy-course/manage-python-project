pip有什么问题？
================


pip的安装
------------

pip默认是安装好了的，可以通过

.. code-block:: bash

    $ python -m pip --version
    pip 21.1.3 from C:\Users\Peng Xiao\.pyenv\pyenv-win\versions\3.9.6\lib\site-packages\pip (python 3.9)

保持pip的版本更新
-------------------

.. code-block:: bash

    $ python -m pip install --upgrade pip setuptools wheel


pip的基本用法
---------------

https://packaging.python.org/tutorials/installing-packages/



pip的问题
-----------

假设有两个Django项目，project A 和 project B，这两个Project都需要在Python3.9下面开发，但是project A 需要Django 3， project B需要Django2，
怎么去在本地维护这俩套开发环境？

========  ======  =======
Project   Python  Django
========  ======  =======
A         3.9     3
B         3.9     2
========  ======  =======

