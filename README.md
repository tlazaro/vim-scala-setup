vim-scala-setup
===============

Vim Scala Setup based on http://bleibinha.us/blog/2013/08/my-vim-setup-for-scala

Install guide
=============

UNIX
----

    git clone http://github.com/tlazaro/vim-scala-setup ~/.vim
    ln -s ~/.vim/vimrc ~/.vimrc
    cd ~/.vim
    git submodule update --init
    
Windows
-------

    git clone http://github.com/tlazaro/vim-scala-setup ~/vimfiles
    cd ~/vimfiles
    git submodule update --init
    
Then create a file ``~/_vimrc`` with the content:

    source ~/vimfiles/vimrc
    
General
=======

Some plugins require you to compile them like ``command-t``. List with all plugins that require further action coming soon.
