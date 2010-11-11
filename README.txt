$Id: README.txt 26 2009-06-17 07:47:36Z matt $

File access module
------------------
File access is simply designed to deny or approve access to individual files when using Drupal's private download method. See 'background' below for more information. Requires PHP5 because of some functions.

sponsored by [GotDrupal.com](http://gotdrupal.com),
designed by Matt Petrowsky

Requirements
------------
* PHP5 required due to some functions
* Using either Upload, Filefield or both
* Setting [File system](http://drupal.org/node/22240) settings to 'private'

Feature list:
-------------

* Support for Upload and Filefield files
* Role access controls for individual files
* User per-file access (currently via api only)
* Global access settings for individual roles (eventually users too)
* Optional 'per node' access enforcement (more of a feature for Drupal 7 - but works now)
* No-access redirection to any path

Planned features:
-----------------

* Support for Ubercart integration (purchasing file access)
* Support for Views integration (think per-user-access file listings)
* Support for User Points integration (digital wallets, etc.)

Background
----------
Drupal offers file delivery through one of two methods (although there are modules which will allow you to use the two at the same time), either "public" or "private" are your options, which are not very descriptive. Public simply means Drupal will hand off the file request to the web server. There are no access checks unless specifically added at the web server level.

Drupal's "private" method of file delivery passes the file through PHP. This is where Drupal provides a limited degree of "programability". Since files (as of Drupal 6) are not 'first class citizens' in how Drupal deals with the download, you can only do so much. Fortunately, there is enough to make specific file access possible.

Status
------
This module is in **Alpha stage**, but is a functioning module. Bug reports are appreciated. The module is lacking any UI for controlling user-specific file access on each node, but the api for checking access is there.

The UI also requires the node to be submitted before file access controls will show for files. This is planned to be changed, but for now, the module is functional.

