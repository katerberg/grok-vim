# grok-vim

Pretty solid base for using vim on a daily basis.

## Installation

The plugins are setup as submodules and the vimrc must be linked to your home directory.

    cd ~
    git clone http://github.com/katerberg/grok-vim.git .vim
    ln -s ~/.vim/vimrc ~/.vimrc
    cd ~/.vim
    git submodule init
    git submodule update

## Adding new modules

Adding modules is easy, for example, if we needed to add Tim Pope's git plugin, fugitive.

    git submodule add http://github.com/tpope/vim-fugitive.git bundle/fugitive
    git add .
    git commit -m "Install Fugitive.vim bundle as a submodule."


## Upgrading modules

    git submodule foreach git pull origin master

## Removing unwanted modules

    cd ~/.vim
    git rm --cached bundle/"some module here"
    rm -rf bundle/"some module here"
    git commit -am "Removing Some module"
    git push
