# nosubstr

Print the "unique" lines in a file.  That is, print lines in file(s) that are not substrings of other lines.


# To install

```sh
sudo make install
```


# To use

```sh
/usr/local/bin/nosubstr [-v] [-l] file ...

    -h      print help and exit
    -V      print version and exit

    -v      print substring matches

    -l      look at only leading substrings

    file ...   process lines in these file(s)

nosubstr version: 1.2.1 2025-03-26
```


# Example

Print only the unique lines in `Makefile`:

```sh
/usr/local/bin/nosubstr Makefile
```


# Reporting Security Issues

To report a security issue, please visit "[Reporting Security Issues](https://github.com/lcn2/nosubstr/security/policy)".
