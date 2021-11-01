pyenv 在Mac环境下的安装
========================

pyenv网站

https://github.com/pyenv/pyenv


准备工作
---------

1. 安装xcode ``sudo xcode-select --install``
2. 安装homebrew https://brew.sh/
3. 安装git https://git-scm.com/
4. 安装python build environment ``brew install openssl readline sqlite3 xz zlib``


安装方法
-----------

1. 可以用homebrew

.. code-block:: bash

    brew update
    brew install pyenv

2. 如果homebrew有问题，可以试试手动安装，具体方法如下

.. code-block:: bash

    curl https://pyenv.run | bash

然后在bash或者zsh（看你用哪个）设置下路径和启动命令

.. code-block:: bash

    export PATH="$HOME/.pyenv/bin:$PATH"

    echo 'export PYENV_ROOT="$HOME/.pyenv"' >>~/.zprofile
    echo 'export PATH="$PYENV_ROOT/bin:$PATH"' >>~/.zprofile
    echo 'eval "$(pyenv init --path)"' >>~/.zprofile

    echo 'eval "$(pyenv init -)"' >>~/.zshrc

重启命令行，然后输入pyenv，能看到下面的输出，说明你的安装没有问题了

.. code-block:: bash

    ➜  ~ pyenv
    pyenv 2.2.0
    Usage: pyenv <command> [<args>]

    Some useful pyenv commands are:
    --version   Display the version of pyenv
    activate    Activate virtual environment
    commands    List all available pyenv commands
    deactivate   Deactivate virtual environment
    doctor      Verify pyenv installation and development tools to build pythons.
    exec        Run an executable with the selected Python version
    global      Set or show the global Python version(s)
    help        Display help for a command
    hooks       List hook scripts for a given pyenv command
    init        Configure the shell environment for pyenv
    install     Install a Python version using python-build
    local       Set or show the local application-specific Python version(s)
    prefix      Display prefix for a Python version
    rehash      Rehash pyenv shims (run this after installing executables)
    root        Display the root directory where versions and shims are kept
    shell       Set or show the shell-specific Python version
    shims       List existing pyenv shims
    uninstall   Uninstall a specific Python version
    version     Show the current Python version(s) and its origin
    version-file   Detect the file that sets the current pyenv version
    version-name   Show the current Python version
    version-origin   Explain how the current Python version is set
    versions    List all Python versions available to pyenv
    virtualenv   Create a Python virtualenv using the pyenv-virtualenv plugin
    virtualenv-delete   Uninstall a specific Python virtualenv
    virtualenv-init   Configure the shell environment for pyenv-virtualenv
    virtualenv-prefix   Display real_prefix for a Python virtualenv version
    virtualenvs   List all Python virtualenvs found in `$PYENV_ROOT/versions/*'.
    whence      List all Python versions that contain the given executable
    which       Display the full path to an executable

    See `pyenv help <command>' for information on a specific command.
    For full documentation, see: https://github.com/pyenv/pyenv#readme
    ➜  ~



问题
------


安装python失败

.. code-block:: bash

    ➜  ~ pyenv install 3.9.7
    python-build: use openssl@1.1 from homebrew
    python-build: use readline from homebrew
    Downloading Python-3.9.7.tar.xz...
    -> https://www.python.org/ftp/python/3.9.7/Python-3.9.7.tar.xz
    Installing Python-3.9.7...
    python-build: use tcl-tk from homebrew
    python-build: use readline from homebrew
    python-build: use zlib from xcode sdk

    BUILD FAILED (OS X 12.0.1 using python-build 20180424)

    Inspect or clean up the working tree at /var/folders/d1/5cgd23cn2c5fd_hr4vk6pgfh0000gn/T/python-build.20211029121146.25284
    Results logged to /var/folders/d1/5cgd23cn2c5fd_hr4vk6pgfh0000gn/T/python-build.20211029121146.25284.log

    Last 10 log lines:
    checking for python3... python3
    checking for --enable-universalsdk... no
    checking for --with-universal-archs... no
    checking MACHDEP... "darwin"
    checking for gcc... clang
    checking whether the C compiler works... no
    configure: error: in `/var/folders/d1/5cgd23cn2c5fd_hr4vk6pgfh0000gn/T/python-build.20211029121146.25284/Python-3.9.7':
    configure: error: C compiler cannot create executables
    See `config.log' for more details
    make: *** No targets specified and no makefile found.  Stop.
    ➜  ~ softwareupdate --all --install --force
    Software Update Tool

    Finding available software
    No updates are available.
    ➜  ~ sudo rm -rf /Library/Developer/CommandLineTools
    Password:
    ➜  ~ sudo xcode-select --install


设置global的python版本失败。可以试试


.. code-block:: bash

    pyenv rehash
