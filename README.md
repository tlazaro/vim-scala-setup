vim-scala-setup
===============

Vim Scala Setup based on http://bleibinha.us/blog/2013/08/my-vim-setup-for-scala

Vim environment setup based on http://vimcasts.org/episodes/synchronizing-plugins-with-git-submodules-and-pathogen/

Install guide
=============

These install steps represent a clean install, wiping or overriding all the Vim configuration you had before! Recommended for people new to Vim mostly who don't have a configured Vim environment. Otherwise backup your configuration before doing anything that you might regret losing.

UNIX
----

Basically clone the repository to your ``.vim`` folder, make your .vimrc a link to the one inside the cloned repository and then download all the submodules (the plugins).

    git clone http://github.com/tlazaro/vim-scala-setup ~/.vim
    ln -s ~/.vim/vimrc ~/.vimrc
    cd ~/.vim
    git submodule update --init
    
Windows
-------

Basically clone the repository to your ``vimfiles`` folder, make your ``_vimrc`` a link to the one inside the cloned repository and then download all the submodules (the plugins).

    git clone http://github.com/tlazaro/vim-scala-setup ~/vimfiles
    cd ~/vimfiles
    git submodule update --init
    
Then create a file ``~/_vimrc`` with the content:

    source ~/vimfiles/vimrc
    
Final Setup Steps
------------------

  * Compile ``command-t``: https://github.com/wincent/Command-T

  * Install ``ctags`` in your OS 

  * Install `powerline`

### Install Powerline Linux

Instal powerline from the bundle in `.vim`:

    pip install --user --editable=$HOME/.vim/bundle/powerline

    cp $HOME/.vim/bundle/powerline/font/PowerlineSymbols.otf ~/.fonts/
    fc-cache -vf ~/.fonts/

    cp $HOME/.vim/bundle/powerline/font/10-powerline-symbols.conf ~/.config/fontconfig/conf.d/

Install fonts that work with Powerline:

    git clone git@github.com:powerline/fonts.git
    cd fonts
    ./install.sh

Then set you terminal to use one of those font, you can try `Inconsolata for Powerline`.

Updating plugins
================

To update the code of every plugin:

    git submodule foreach git pull origin master
    
If a new submodule (plugin) is added to this repository since the time you cloned it you must:

    git submodule update --init
    
Collaboration
=============

Please contact me for any problem, suggestion or enhancements, preferably by reporting an issue through GitHub. Pull requests more than welcome!
