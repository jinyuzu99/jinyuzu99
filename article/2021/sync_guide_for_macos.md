- cli tool
	- `ln` make link
		- `-s` create a symbolic link
		- `-F` force link
	- `rsync` a fast, versatile, remote (and local) file-copying tool
		- `--archive, -a` archive mode; equals `-rlptgoD`
		- `--delete` delete extraneous files from dest dirs
		- `--verbose, -v` increase verbosity
- dropbox, gdrive
	- `ln -s ~/Documents ~/Dropbox`
	- `ln -s ~/Documents ~/Google`
- onedrive
	- onedrive do not support `ln` style linking currently. we could only mannualy copy file, and use it as a backup option. to do this, we need to use `rsync`.
	- `rsync -av --delete ~/Documents/ ~/OneDrive`
- .config
	-
	  ```sh
	  cd ~/Documents/sync
	  mv ~/.config ~/Documents/sync
	  
	  ln -sF $PWD/config ~/.config
	  ln -sF ~/.config/.profile ~/.profile
	  ln -sF ~/.config/.editorconfig ~/.editorconfig
	  ln -sF ~/.config/.prettierrc ~/.prettierrc
	  ```
- application data
	- mostly stored in `~/Library/Application\ Support`
	- google chrome
		- `~/Library/Application\ Support/Google/Chrome`
		-
		  ```sh
		  cd ~/Documents/sync/
		  mv ~/Library/Application\ Support/Google/Chrome .
		  
		  ln -s $PWD/chrome ~/Library/Application\ Support/Google/Chrome
		  ```
	- microsoft edge
		- `/Library/Application\ Support/Microsoft\ Edge`