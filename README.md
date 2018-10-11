# How to use gitbook

## 1. Install node.js

Install node.js from official website.

Link: https://nodejs.org/en/

> There are two version of node.js there, just install stable version is enough.

When finished installation. check with `node -v`, to see if install sucessfully.

```
$ node -v
V6.*.*
```


## 2. Install gitbook

```
sudo npm install gitbook-cli -g
```

> Remember to add `sudo` and `-g`. -g means install globally.

Check with `gitbook -V` to see if install sucessfully.

```
$ gitbook -V
CLI version: 2.3.2
GitBook version: 3.2.3
```

## Gitbook command

using `gitbook build` to build the HTML
```
$ gitbook build
info: 14 plugins are installed
info: 13 explicitly listed
info: loading plugin "github"... OK
info: loading plugin "edit-link"... OK
info: loading plugin "donate"... OK
info: loading plugin "sitemap"... OK
info: loading plugin "splitter"... OK
info: loading plugin "sharing-plus"... OK
info: loading plugin "search"... OK
info: loading plugin "search-pro"... OK
info: loading plugin "highlight"... OK
info: loading plugin "lunr"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 6 pages
info: found 5 asset files
info: >> generation finished with success in 1.0s !
```

There will be `_book` folder on the root folder.

or preview the book using `gitbook serve`

```
$ gitbook serve

Live reload server started on port: 35729
Press CTRL+C to quit ...

info: 14 plugins are installed
info: loading plugin "github"... OK
info: loading plugin "edit-link"... OK
info: loading plugin "donate"... OK
info: loading plugin "sitemap"... OK
info: loading plugin "splitter"... OK
info: loading plugin "sharing-plus"... OK
info: loading plugin "search"... OK
info: loading plugin "search-pro"... OK
info: loading plugin "livereload"... OK
info: loading plugin "highlight"... OK
info: loading plugin "lunr"... OK
info: loading plugin "fontsettings"... OK
info: loading plugin "theme-default"... OK
info: found 6 pages
info: found 5 asset files
info: >> generation finished with success in 0.9s !

Starting server ...
Serving book on http://localhost:4000
```

You can just using the link http://localhost:4000 to preview on browser.

## 4. Install calibre plugin

Calibre link: https://calibre-ebook.com/download

```
sudo ln -s /Applications/calibre.app/Contents/MacOS/ebook-convert /usr/local/bin
//官方的文档里是如下命令：会引起权限和命令无效等问题
sudo ln -s ~/Applications/calibre.app/Contents/MacOS/ebook-convert /usr/bin
```

Generate different format

```
# Generate a PDF file
$ gitbook pdf ./ ./mybook.pdf

# Generate an ePub file
$ gitbook epub ./ ./mybook.epub

# Generate a Mobi file
$ gitbook mobi ./ ./mybook.mobi
```
