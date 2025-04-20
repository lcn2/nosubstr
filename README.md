# nosubstr

Print the "unique" lines in a file.  That is, print lines in file(s) that are not substrings of other lines.


# To install

```sh
sudo make install
```


# Example

Print only the unique lines in `Makefile`:

```sh
$ /usr/local/bin/nosubstr Makefile
#

CC= cc
CHMOD= chmod
CP= cp
ID= id
INSTALL= install
RM= rm
SHELL= bash
V=@:
PREFIX= /usr/local
DESTDIR= ${PREFIX}/bin
TARGETS= nosubstr
all: ${TARGETS}
	${V} echo DEBUG =-= $@ start =-=
	${V} echo DEBUG =-= $@ end =-=
.PHONY: all configure clean clobber install
configure:
clean:
clobber: clean
install: all
	@if [[ $$(${ID} -u) != 0 ]]; then echo "ERROR: must be root to make $@" 1>&2; exit 2; fi
	${INSTALL} -d -m 0755 ${DESTDIR}
	${INSTALL} -m 0555 ${TARGETS} ${DESTDIR}
```


# To use

```
/usr/local/bin/nosubstr [-v] [-l] file ...

    -h      print help and exit
    -V      print version and exit

    -v      print substring matches

    -l      look at only leading substrings

    file ...   process lines in these file(s)

nosubstr version: 1.2.1 2025-03-26
```


# Reporting Security Issues

To report a security issue, please visit "[Reporting Security Issues](https://github.com/lcn2/nosubstr/security/policy)".
