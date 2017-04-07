# wslpath
Convert Unix and Windows format paths in WSL.

## Example
Usage is similar to `cygpath.exe`.

    C:\Users\alice>bash -c 'wslpath -u foo\\bar.txt'
    foo/bar.txt

    C:\Users\alice>bash -c 'wslpath -ua foo\\bar.txt'
    /mnt/c/Users/alice/foo/bar.txt

    C:\Users\alice>bash -c 'wslpath -ua \\baz'
    /mnt/c/baz

    C:\Users\alice>bash -c 'wslpath -w /mnt/c/baz'
    C:\baz

    C:\Users\alice>bash -c 'cd /tmp; wslpath -w foo'
    wslpath: error: not a windows mount point: foo

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
