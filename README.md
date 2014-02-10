~/bin
=====

Scripts that deserve to live in ~/bin

rename-batch
------------

Perl script to rename files using a text file to record the new file
names. A example of use would be:

1. First you save a file list:

        rename-batch -s

2. You can edit `files.txt` wherever you want but not change the files
   order.

3. To see how the files would be renamed you load the saved file list:

        rename-batch -l

4. If everything looks right you can add the `-e` switch to apply the
   changes:

        rename-batch -l -e
