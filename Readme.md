Bashmarks
=====

Bashmarks is a shell script that allows you to save and jump to commonly used directories. Now supports tab completion.


Extra Features
--------------

* default directory when using `g` - default `$HOME`.
* Allows placing commands after the the letter e.g `g webfolder ls` would go the webfolder bookmark then perform `ls`
* `g -` Goes to the previous directory.
* `o command` to open the bookmark in [Path Finder]("http://www.cocoatech.com/pathfinder/") (Mac OS X Only).
* `t command` to open the bookmark in a new terminal tab (Mac OS X Only).

Install
-------

1. git clone git://github.com/LeonardoGentile/bashmarks.git
2. make install
3. **source ~/.dotfiles/bin/bashmarks.sh** from within your **~.bash\_profile** or **~/.bashrc** file

Shell Commands
--------------

	s <bookmark_name>  - Saves the current directory as "bookmark_name"
	g <bookmark_name>  - Goes (cd) to the directory associated with "bookmark_name"
	d <bookmark_name>  - Deletes the bookmark
	l <bookmark_name>  - Lists the specified bookmark associated with "bookmark_name"
	l                  - Lists all available bookmarks
	s                  - Saves the default directory
	g                  - Goes to the default directory
	g -                - Goes to the previous directory
	_p <bookmark_name> - Prints the directory associated with "bookmark_name"

	# Mac OS X Only
	o <bookmark_name>  - Open the directory associated with "bookmark_name" in Path Finder
	t <bookmark_name>  - Open the directory associated with "bookmark_name" in a new tab

Example Usage
-------------

	$ cd /var/www/
	$ s webfolder
	$ cd /usr/local/lib/
	$ s locallib
	$ l
		webfolder	 /var/www/
		locallib	 /usr/local/lib/
	$ g web<tab>
	$ g webfolder	  # cd to /var/www/
	$ o webfolder	  # Open in Path Finder if on mac
	$ l locallib
		locallib	 /usr/local/lib/

Where Bashmarks are stored
--------------------------

All of your directory bookmarks are saved in a file called `bashmarks_dirs` under your `$HOME/.dotfiles/data/` directory.  
**PLEASE NOTE:** this is just my personal configuration, feel free to move the main `bashmarks.sh` file and the `bashmarks_dirs` wherever you want
within your home directory as long you tells baskmarks where the data are stored (change `SDIRS` in `bashmarks.sh`) and as long as you correctly *source* it from your **.bash\_profile** (see point 3 under Installation)

Authors
-------
* Leonardo Gentile (messed up the files location and support for Path Finder)
* Bilal Syed Hussain (added the Os X extra features )
* Huy Nguyen (original version)

