# Steps to upgrade PHP

### Follow the below steps 

##### Note: You can replace `7.3` & `7.2` as per your requirement

````
    1) brew install php@7.3
    2) brew link php@7.3 --force --overwrite
    3) brew update
    4) brew upgrade php
    5) brew unlink php@7.2 && brew link php
    6) brew services restart --all
    7) composer global update
    8) valet start
    
    9) update path of php in .zshrc file use following cmd to open file
    
    10) command to open zshrc file : vim ~/.zshrc
````
