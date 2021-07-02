# Command Line Inbterface definition

Application name: udocker_setup

Usage:

```bash
udocker_setup |GENERAL_OPTIONS| COMMAND |SPEC_OPTIONS and ARGS|
```

**General Options**:

```bash
-h, --help                    help, usage
-V, --version                 show version
-v N, --verbose=N             verbosity level 0 (quiet) - 5 (debug)
-q, --quiet                   quiet (verbosity level 0)
-c conffile, --conf=conffile  use configuration file
```

**Commands, specific options and positional arguments**:

* `install`    perform default installation
  * (DEFAULT no options or args) download and install udocker to udocker directory, sets $PATH, and all modules to .udocker
  * With config file or setting environment variables will install to custom directories
  * `--from=<url>|<dir>`     URL or local directory with modules
  * `--prefix=<directory>`   installation directory
  * `<module>`               positional args 1 or more
* `show`       show installed modules, versions, URLS for download
* `avail`      show available modules in the catalog
  * `--from=<url>|<dir>`     URL or local directory with modules
* download   download tarball, so it can be installed offline
  * (DEFAULT no options or args) download udocker and all modules to udocker_install directory
  * With config file or setting environment variables will download to custom directory
  * `--from=<url>|<dir>`     URL or local directory with modules
  * `--prefix=<directory>`   destination download directory
  * `<module>`               positional args 1 or more
* download-all     download all tarballs
  * (DEFAULT no options or args) download udocker and all modules to udocker_install directory
  * With config file or setting environment variables will download to custom directory
  * `--from=<url>|<dir>`     URL or local directory with modules
  * `--prefix=<directory>`   destination download directory
* upgrade          upgrade module
  * `--from=<url>|<dir>`     URL or local directory with modules
  * `<module>`               positional args 1 or more
* upgrade-all      upgrade all modules
  * `--from=<url>|<dir>`     URL or local directory with modules
* verify           verify/checksum tarballs
  * `--prefix=<directory>`   destination download directory
* delete           delete module
  * `--prefix=<directory>`   destination download directory
  * `<module>`               positional args 1 or more
* delete-all       delete all software
  * `--prefix=<directory>`   destination download directory
* delete-metadata  delete cached metadata
  * `--prefix=<directory>`   destination download directory
