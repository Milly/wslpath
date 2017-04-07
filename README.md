# wslpath
Convert Unix and Windows format paths in WSL.

## Usage
    wslpath (-d|-m|-u|-w|-t TYPE) [-f FILE] [OPTION]... NAME...

## Options
  * --version             show program's version number and exit
  * -h, --help            show this help message and exit

### Output type options
 * -d, --dos              like --windows (for compatibility)
 * -m, --mixed            like --windows, but with regular slashes (C:/WINNT)
 * -u, --unix             (default) print Unix form of NAMEs (/mnt/c/winnt)
 * -w, --windows          print Windows form of NAMEs (C:\WINNT)
 * -t TYPE, --type=TYPE   print TYPE form: 'dos', 'mixed', 'unix', or 'windows'

### Path conversion options
 * -a, --absolute         output absolute path
 * -l, --long-name        no effect (for compatibility)
 * -p, --path             NAME is a PATH list (i.e., '/bin:/usr/bin')
 * -s, --short-name       no effect (for compatibility)

### Other options
 * -f FILE, --file=FILE   read FILE for input; use - to read from STDIN
 * -i, --ignore           ignore missing argument
