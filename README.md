~/bin
=====

Scripts that deserve to live in ~/bin

rename-batch
------------

Perl script to rename files using a text file to record the new file
names. To use it you would do something like:

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

- Replace underscores with spaces in all files:

        rename-regexp -s 's/_/ /'

- Replace underscores with spaces in files that end in .pdf:

        rename-regexp -s 's/_/ /' -m 'm/\.pdf$/'

- Replace underscores with spaces and change names case to lower
  recursively:

        rename-regexp -s 'tr/_[A-Z]/ [a-z]/' -r

- To apply the changes you need to add the `-e` switch:

        rename-regexp -s 'tr/_[A-Z]/ [a-z]/' -r -e

