# wslpath
Convert Unix and Windows format paths in WSL.

## Usage
    wslpath (-d|-m|-u|-w|-t TYPE) [-f FILE] [OPTION]... NAME...

## Options

### Output type options
 Option          | Description
-----------------|------------------------------------------------------
 -d, --dos       | like --windows (for compatibility)
 -m, --mixed     | like --windows, but with regular slashes (C:/WINNT)
 -u, --unix      | (default) print Unix form of NAMEs (/mnt/c/winnt)
 -w, --windows   | print Windows form of NAMEs (C:\WINNT)
 -t, --type=TYPE | print TYPE form: 'dos', 'mixed', 'unix', or 'windows'

### Path conversion options
 Option           | Description
------------------|---------------------------------------------
 -a, --absolute   | output absolute path
 -l, --long-name  | no effect (for compatibility)
 -p, --path       | NAME is a PATH list (i.e., '/bin:/usr/bin')
 -s, --short-name | no effect (for compatibility)

### Other options
 Option          | Description
-----------------|-----------------------------------------------
 -f, --file=FILE | read FILE for input; use - to read from STDIN
 -i, --ignore    | ignore missing argument
