
## Start a Database-driven project

### Blueprint the application
We want to build a basic CMS

### Establish your work area
Kevin uses a similar structure for all projects:
* home_folder/
	* public/
		* index.php
		* images/
			* index.php
		* stylesheets/
			* index.php
	* private/
		* initialize.php
		* functions.php
		* shared/

Everything that is supposed to be accessed would be in public/
The web server is going to be configured so that routing requests go to public/
private/ cannot be accessed through any URI
However, php files in public/ will be able to access private/ folder through the filesystem

> Every filder in the public/ directory should have an `index.php` file to prevent access to folder contents (depends on the web server configuration


### Include and require files
One of the great features of PHP is the ability to include PHP code contained in other files. This helps to DRY and improves maintenance.

Typical things we want to include:
* libraries of functions
* header, navigation, footer, etc.
* scripts, styles, analytics tag, etc.

There are 4 mechanisms to include code:
* include()
* require()
* include_once()
* require_once()

`require()` will raise an error, `include()` will not
`_once()` will check if it has already been included and if so, it won't include it again. 
* for functions, we want include_once/require_once, because functions cannot be declared twice
* for exple for ads to display in different places of the page, we will want include/require, because we DO want to include them several times

> Always use static strings inside includes, because otherwise we could have major security issues if we allow someone to put files in our folders



> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE0ODMyMTQyODldfQ==
-->
