pyenv 在Linux环境下的安装
============================

pyenv网站

https://github.com/pyenv/pyenv

.. note::

    此文以Ubuntu 20.10为例，其他Linux发行版的安装方法请参考github



准备工作
---------

安装一些依赖

.. code-block:: bash

    sudo apt-get update; sudo apt-get install make build-essential libssl-dev zlib1g-dev \
    libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm git vim\
    libncursesw5-dev xz-utils tk-dev libxml2-dev libxmlsec1-dev libffi-dev liblzma-dev

安装
------

.. code-block:: bash

    curl https://pyenv.run | bash



设置
--------

以zsh为例。

.. code-block:: bash

    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.zprofile
    echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.zprofile
    echo 'eval "$(pyenv init --path)"' >> ~/.zprofile

    echo 'export PYENV_ROOT="$HOME/.pyenv"' >> ~/.profile
    echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >> ~/.profile
    echo 'eval "$(pyenv init --path)"' >> ~/.profile

    echo 'eval "$(pyenv init -)"' >> ~/.zshrc


其它请参考 https://github.com/pyenv/pyenv


