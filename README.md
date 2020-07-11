# VIM Header Composer

[url-codacy ]: https://www.codacy.com/app/jmurowaniecki/vim-header-composer
[ico-codacy ]: https://img.shields.io/codacy/grade/9ac72e1294504b06b245a7b4d8253029?logo=codacy&logoColor=green&style=flat-square
[url-styleci]: https://github.styleci.io/repos/103320898
[ico-styleci]: https://github.styleci.io/repos/103320898/shield
[ico-version]: https://img.shields.io/github/v/tag/jmurowaniecki/vim-header-composer?sort=semver&style=flat-square

[![StyleCI][ico-styleci]][url-styleci]
[![Codacy ][ico-codacy ]][url-codacy]
[![Version][ico-version]](#)

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

### Yes, you can do it by the old-fashioned way
Clonning this repository and linking it to your `.../bin/` folder.
```sh
git clone git@github.com:ernandojs/vim-header-composer.git
sudo mv vim-header-composer /opt/
sudo ln -s /opt/vim-header-composer/vhc /usr/local/bin
echo 'map <F2> :!vhc' >> ~/.vimrc
```

### Makefile
You can also perform installation with `make install`.



## Basic usage steps

1.  Install this script _globally or **not**_;
2.  Open any file using **VI/VIM**;
3.  In normal VIM mode (press **<ESC\>**);
4.  Goto VISUAL mode (select the line - or lines - with **SHIT + V**);
5.  Press **<F2\>** then **<ENTER\>**;



### Using styles
Instead of using the characters and the standard format you can set the string to process using styles as seen below.


#### Prettybox
`vhc <<< "vhc:prettybox;Woooow I'm using prettybox!"` produces:
```text
┌─────────────────────────────┐
│ Woooow I'm using prettybox! │
└─────────────────────────────┘
```

For further information about styles see [more examples](EXAMPLES.md).