jump
====

Simple implementation of jump script, bookmarks directories across the file system for fast cd.



Installation
-------

* Clone the repository: 

        git clone https://github.com/michelesr/jump/

* Add the source instruction to your .bashrc or .zshrc and create .bookmarks dir on your home:

        source /path-of-jump-repo/jump
        mkdir -p ~/.bookmarks

* If you use zsh you may want to add autocompletion... to do this copy _jump to a folder that is included in fpath... check fpath on .zshenv

        # add your function directory inside fpath
        fpath=($fpath $HOME/.zsh/func) 
        typeset -U fpath
    
    
Usage
-----

* Cd to a directory and mark it as 'j':
        
        cd Project/jump 
        mark j

* Jump to 'j' bookmark:
 
        jump j

* Remove 'j' bookmark:

        unmark j
    
