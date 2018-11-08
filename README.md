# VIM Header Composer

[![StyleCI](https://github.styleci.io/repos/103320898/shield?branch=master)](https://github.styleci.io/repos/103320898)
[![Codacy](https://api.codacy.com/project/badge/Grade/9ac72e1294504b06b245a7b4d8253029)](https://www.codacy.com/app/jmurowaniecki/vim-header-composer)

VIM header composer is an utility script wrote in shell very simple to make header's based on comments in vim such as above.

The string will be formated and fulfilled with characters following your desired style.

```text
############################################
#### CREATE FILE BAR AND SEND TO SERVER ####
############################################

RUN echo "foo" > bar
RUN scp -i bar example.com:/dev/null
```

## Installation

```sh
git clone https://github.com/ernandos/vim-header-composer.git
sudo mv vim-header-composer /opt/
sudo ln -s /opt/vim-header-composer/vhc /usr/local/bin
echo 'map <F2> :!vhc' >> ~/.vimrc
```

## Basic usage steps

1.  Install this script globally;
2.  Open any file using VI/VIM;
3.  In normal VIM mode (press <ESC>), select the line with SHIT + V;
4.  Press <F2\> and <ENTER\>;

### Using styles
Instead of using the characters and the standard format you can set the string to process using styles as seen below.

`echo "vhc:prettybox;Woooow I'm using prettybox!"|vhc`  produces output:
```text
┌─────────────────────────────┐
│ Woooow I'm using prettybox! │
└─────────────────────────────┘
```

#### `sides`
`echo "vhc:sides;Woooow I'm using sides!"|vhc` produces:
```text
⎡                         ⎤
⎢ Woooow I'm using sides! ⎥
⎣                         ⎦
```

#### `prettybox`
`echo "vhc:prettybox;Woooow I'm using prettybox!"|vhc` produces:
```text
┌─────────────────────────────┐
│ Woooow I'm using prettybox! │
└─────────────────────────────┘
```

#### `quotes`
`echo "vhc:quotes;Woooow I'm using quotes!"|vhc` produces:
```text
                           "
  Woooow I'm using quotes!
"
```

#### `ccomment`
`echo "vhc:ccomment;Woooow I'm using ccomment!"|vhc` produces:
```text
/*
* Woooow I'm using ccomment!
*/
```

#### `lcomment`
`echo "vhc:lcomment;Woooow I'm using lcomment!"|vhc` produces:
```text
//
// Woooow I'm using lcomment!
//
```

#### `box`
`echo "vhc:box;Woooow I'm using box!"|vhc` produces:
```text
+-----------------------+
| Woooow I'm using box! |
+-----------------------+
```

#### `star`, `stars` or `asterisk`
`echo "vhc:stars;Woooow I'm using stars!"|vhc` produces:
```text
***************************
* Woooow I'm using stars! *
***************************
```

#### Standart `ernjs` or `ernando`
`echo "vhc:awesome;Woooow I'm using VHC!"|vhc` produces:
```text
###############################
#### Woooow I'm using VHC! ####
###############################
```
