jump
====

Simple implementation of jump script, bookmarks directories across the file system for fast cd.



Installation
-------

* Clone the repository: 

        git clone https://github.com/michelesr/jump/

* Add the source instruction to your .bashrc or .zshrc and create .bookmarks dir on your home:

        # add this to shell rc
        source /path-of-jump-repo/jump  
        #  create dir
        mkdir -p ~/.bookmarks           

* If you use zsh you may want to add autocompletion... to do this copy _jump to a folder that is included in fpath or add _jump directory to fpaths ... check fpath on .zshenv

        # add your functions directory inside fpath
        fpath=($fpath path/to/_jump/directory/) 
        typeset -U fpath
        
* You may have to force rebuild `zcompdump`:

        rm -f ~/.zcompdump; compinit
    
    
Usage
-----

* Cd to a directory and mark it as 'foo':
        
        cd Project/jump 
        mark foo

* Jump to bookmark:
 
        jump foo

* Remove bookmark:

        unmark foo
    
#### zsh completion

        $ jump <PRESS TAB>
        foo  -- /home/michele/Projects/jump
        is   -- /home/michele/Projects/web_project
        pj   -- /home/michele/Projects
