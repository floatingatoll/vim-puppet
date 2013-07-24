vim-puppet
==========

Make vim more Puppet friendly!

TLDR
-----

Add to vim using pathogen:

    git clone https://github.com/godlygeek/tabular         ~/.vim/bundle/tabular
    git clone https://github.com/floatingatoll/vim-puppet  ~/.vim/bundle/vim-puppet

Add to .vimrc:

    call pathogen#infect()

    syntax enable
    filetype plugin indent on

    map <Leader>= :Tabularize /=>/l1<Return>

To re-indent a file, except for the => lists:

    gg=G

To fix a single => list, put the cursor on any line in the list and type:

    \=

(Unless you changed your leader key from \ to something else.)

Provides
--------

  * Formatting based on the latest Puppetlabs Style Guide
  * Syntax highlighting
  * Automatic => alignment (when the
    [tabular](https://github.com/godlygeek/tabular) plugin is also installed)
  * Doesn't require a bloated JRE
  * Doesn't take minutes to open

Additional useful plugins
-------------------------

 * [syntastic](https://github.com/scrooloose/syntastic) plugin for automatic
   syntax checking while in vim.
 * [vim-snippets](https://github.com/honza/vim-snippets) is a library of
   snippets for multiple languages, including Puppet. Works with both
   [snipmate](https://github.com/garbas/vim-snipmate) and
   [ultisnips](https://github.com/SirVer/ultisnips).

Installation
------------

If you're using pathogen to manage your vim modules (and if you're not, why
aren't you), you can simply add this as a submodule in your `~/.vim/bundle/`
directory.

My entire home directory is a git repository, so for me it's simply a case of

    $ git submodule add -f git://github.com/rodjek/vim-puppet.git .vim/bundle/puppet

If you're not using pathogen, you can just manually place the files in the
appropriate places under `~/.vim/`
