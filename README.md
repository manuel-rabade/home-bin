~/bin
=====

Scripts that deserve to live in ~/bin

rename-batch
------------

Perl script to rename files using a text file to record the new
filenames. To use it you would do something like:

1. Save a file list:

        rename-batch -s

2. Edit `files.txt` wherever you want but don't change the files order.

3. See how the files would be renamed:

        rename-batch -l

4. If everything looks right you can add the `-e` switch to apply the
   changes:

        rename-batch -l -e

rename-regexp
-------------

Perl script to rename files using regular expressions. Some examples of
use would be:

- Replace underscores with spaces in all filenames:

        rename-regexp -s 's/_/ /'

- Replace underscores with spaces in filenames that end in `.pdf`:

        rename-regexp -s 's/_/ /' -m 'm/\.pdf$/'

- Recursively replace underscores with spaces and change filenames case
  to lower:

        rename-regexp -s 'tr/_[A-Z]/ [a-z]/' -r

- To apply the changes you need to add the `-e` switch:

        rename-regexp -s 'tr/_[A-Z]/ [a-z]/' -r -e

rsync-backup
------------

Bash script to mount an external disk, backup a local filesystem using
rsync, tweet about it and umount the external disk.

To setup your backup first review the configuration section of the
script. To test your setup you can add `--dry-run` to `RSYNC_ARGS`.

To enable tweeting the backup stats you should install
[bti](https://github.com/gregkh/bti), create a twitter application and
pair it with your bti configuration.

Author
------

Manuel Rábade <[manuel@rabade.net](mailto:manuel@rabade.net)>

License
-------

This work is licensed under a [MIT License](LICENSE.txt).
