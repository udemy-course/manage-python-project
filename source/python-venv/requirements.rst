requirements.txt
======================


requirements.txt的常见写法
-----------------------------


指定版本号

.. code-block::

    # requirements.txt
    Django
    Django==3.1.2
    Django>=2.2
    Django<3.0
    Django>=2.2,<3.0
    Django~=3.1.2   # Django>=3.1.2, ==3.1.*
    Django~=3.1     # Django>=3.1, ==3.*


从代码仓库

.. code-block::

    # requirements.txt
    git+https://gitprovider.com/user/project.git@{version}

这里的version可以是一个tag, a branch, or a commit，如果空，就是默认分支的最新commit


production and dev
------------------------

推荐production和dev的requirements分开，比如

.. code-block::
    (venv) ➜  manage-python-project git:(master) ✗ more requirements.txt
    Sphinx==4.2.0
    sphinx-rtd-theme==1.0.0
    (venv) ➜  manage-python-project git:(master) ✗ more requirements-dev.txt
    pytest
    (venv) ➜  manage-python-project git:(master) ✗