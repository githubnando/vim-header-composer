# VIM Header Composer

VIM header composer is an utility script wrote in shell very simple to make header's based on comments in vim such as
above. 

The string will always be put in the middle and fulfilled with a serious of characters "##".

```sh
############################################
#### CREATE FILE BAR AND SEND TO SERVER ####
############################################

$ RUN echo "foo" > bar
$ RUN scp -i bar example.com:/dev/null
```

# Installation
```sh
$ git clone https://github.com/ernandos/vim-header-composer.git 
$ sudo mv vim-header-composer /opt/
$ sudo ln -s /opt/vim-header-composer/vhc /usr/local/bin
$ echo 'map <F2> :!vhc' >> ~/.vimrc
```

# Usage
```
1 - Open any file
2 - In normal VIM mode (press <ESC>), select the line with SHIT + V
3 - Press <F2> and <ENTER>
```
