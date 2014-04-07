
ecommerce delivery ELECTRONICALLY
================================================================================

Allows you to let people download files based on
a sale.

THE KEY IS: add the following method to your buyable:

function DownloadFiles(){
 //return a DataObject Set of files here....
}

You can also add files to the Order Step.

Make sure that you send a receipt AFTER you have created
the files for download!

Here are the steps:


The electronic download module works as follows:

1. within products / product variations / other buyables you identify files for download

2. these are made available as a Data Object Set using a method that needs to be named DownloadFiles

3. You add an order step called "download"

4. This orderstep can have its own list of files that are always made available for download (e.g. pdf brochure on upcoming event, manual, license, whatever).

5. when the order steps "runs", the download files are added to the order as a "OrderStatusLog" and shown on the order receipt in a list of downloads.

6. the orderstep also copies the the "original" files to a temporary directory with a random name (i.e. one you need to know, one that you cant guess). the folder name always ends in the order number so that you can still trace it back to an order.

7. after three days (or whatever you specify in the order step), the files are automatically deleted.  The folder is not deleted at present.

POTENTIAL IMPROVEMENTS:

1. put all files in a zip (this should be optional).

2. also delete the folder itself after three days (easy fix).

3. immediate delete files after they have been downloaded and the user indicates that (s)he is done with them.

4. allow the downloads to be restored or keep them on the server for XXX days after actually deleting them
(you can add an .htaccess file after a few days to close it down for now)

Any other ideas?


Developers
-----------------------------------------------
Nicolaas Francken [at] sunnysideup.co.nz



Documentation
-----------------------------------------------
Please contact author for more details.

Any bug reports and/or feature requests will be
looked at

We are also very happy to provide personalised support
for this module in exchange for a small donation.


Requirements
-----------------------------------------------
see composer.json


Project Home
-----------------------------------------------
See http://code.google.com/p/silverstripe-ecommerce

Demo
-----------------------------------------------
See http://www.silverstripe-ecommerce.com


Installation Instructions
-----------------------------------------------

1. Find out how to add modules to SS and add module as per usual.

2. Review configs and add entries to mysite/_config/config.yml
(or similar) as necessary.
In the _config/ folder of this module
you can usually find some examples of config options (if any).

