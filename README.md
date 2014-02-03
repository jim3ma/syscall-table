# syscall-table

Generate JSON system call table from Linux source. Hosted at http://syscalls.kernelgrok.com.

## Generating
```
$ brew install ctags
$ easy_install python-ctags simplejson
$ tar -zxvf linux-2.6.35.4.tar.gz
$ cd linux-2.6.35.4
$ ctags --fields=afmikKlnsStz --c-kinds=+pc -R linux-2.6.35.4
```
:coffee: or :beer:
```
$ python ../gen_syscalls.py > syscalls-2.6.35.4.json
```

## Web
* uses [jQuery DataTables] to pull JSON file and format table
* links to lxr.free-electrons.com for source cross-reference and manpages
* www dir checked into gh-pages branch w/ JSON file

## Other
* only tested on 2.6 kernel versions, needs to be updated
* largely unmaintained, feel free to open a PR and help out!
