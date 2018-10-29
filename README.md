# VIM Header Composer

VIM header composer is an utility script wrote in shell very simple to make header's based on comments in vim such as above.

The string will be formated and fulfilled with characters following your desired style.

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

# Basic usage

```
1 - Open any file
2 - In normal VIM mode (press <ESC>), select the line with SHIT + V
3 - Press <F2> and <ENTER>
```

## Using styles
Instead of using the characters and the standard format you can set the string to process using styles as seen below.

```
$ echo "vhc:prettybox;Woooow I'm using prettybox!"|vhc

┌─────────────────────────────┐
│ Woooow I'm using prettybox! │
└─────────────────────────────┘

$
```

### `sides`
`$ echo "vhc:sides;Woooow I'm using sides!"|vhc` produces:
```
⎡                         ⎤
⎢ Woooow I'm using sides! ⎥
⎣                         ⎦
```

### `prettybox`
`$ echo "vhc:prettybox;Woooow I'm using prettybox!"|vhc` produces:
```
┌─────────────────────────────┐
│ Woooow I'm using prettybox! │
└─────────────────────────────┘
```

### `quotes`
`$ echo "vhc:quotes;Woooow I'm using quotes!"|vhc` produces:
```
                           "
  Woooow I'm using quotes!
"                          
```

### `ccomment`
`$ echo "vhc:ccomment;Woooow I'm using ccomment!"|vhc` produces:
```
/*                             
* Woooow I'm using ccomment!
*/                             
```

### `lcomment`
`$ echo "vhc:lcomment;Woooow I'm using lcomment!"|vhc` produces:
```
//                             
// Woooow I'm using lcomment!
//                             
```

### `box`
`$ echo "vhc:box;Woooow I'm using box!"|vhc` produces:
```
+-----------------------+
| Woooow I'm using box! |
+-----------------------+
```

### `star`, `stars` or `asterisk`
`$ echo "vhc:stars;Woooow I'm using stars!"|vhc` produces:
```
***************************
* Woooow I'm using stars! *
***************************
```

### Standart `ernjs` or `ernando`
`$ echo "vhc:awesome;Woooow I'm using VHC!"|vhc` produces:
```
###############################
#### Woooow I'm using VHC! ####
###############################
```
