=============
PYTHON .VIMRC
=============

VIM Configuration for Python / Cython / C Development.

Keep calm and use VIM!

Requirements
------------

- VIM 7.4
- git
- bash 3.2+

How does it look?
-----------------

.. image:: https://github.com/ets-labs/python-vimrc/wiki/img/screenshot.png

Installation
------------

You can install it by using CLI just have next command executed:

.. code-block:: bash

  sh -c "$(curl -fsSL https://raw.githubusercontent.com/RafaelMiquelino/python-vimrc/master/setup.sh)"

During execution of init script do not worry about error messages. When it
occurs just press enter and wait till all plugins are installed.

Autocompletion
--------------

Current bundle use one of the most comprehensive plugins for autocompletion - 
`Valloric/YouCompleteMe <https://github.com/Valloric/YouCompleteMe>`_.
YouCompleteMe autocompletion plugin requires additional installation that 
depends on environment and functionality you want to have. Detailed 
instructions could be found on plugin page: 
`Valloric/YouCompleteMe <https://github.com/Valloric/YouCompleteMe#installation>`_.


Installation for Mac:
============

.. code-block:: bash

  ~/.vim/bundle/YouCompleteMe/install.py --clang-completer

Installation for Ubuntu:
============

.. code-block:: bash

      sudo apt install build-essential cmake python3-dev

Compiling YCM **with** semantic support for C-family languages:

.. code-block:: bash

    cd ~/.vim/bundle/YouCompleteMe
    python3 install.py --clang-completer

Compiling YCM **without** semantic support for C-family languages:

.. code-block:: bash

    cd ~/.vim/bundle/YouCompleteMe
    python3 install.py

If instalation fails on compile, try to creat swap space: https://www.digitalocean.com/community/tutorials/how-to-add-swap-space-on-ubuntu-16-04

tagbar
------------

Need to install exuberant-ctags to work:

**Note:** Installation for Ubuntu 16.04 and later looks like 
this:

.. code-block:: bash

  sudo apt-get install exuberant-ctags

Key bindings
------------

This configuration tends to use standard VIM and installed plugins key 
bindings, but there are some custom key bindings as well:

.. code::

    # Common key bindings:

    inoremap jj     # Esc alternative
    inoremap jk     # Esc alternative

    nmap <F9>       # Jump to the previous buffer
    nmap <F10>      # Jump to the next buffer

    nmap <leader>q  # Delete buffer
    nmap "          # Toggle NERDTree buffer 

    # Python mode key bindings:

    let g:pymode_doc_key='K'
    let g:pymode_breakpoint_key='<leader>b'
    let g:pymode_run_bind='<F5>'

    nmap <leader>g :YcmCompleter GoTo<CR>
    nmap <leader>d :YcmCompleter GoToDefinition<CR>
