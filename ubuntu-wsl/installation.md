### Powershell Command for Ubuntu installation

```
wsl --list 
wsl -l --online 
wsl --insall -d ubantu
wsl --export Ubuntu ubuntu.tar
wsl --import Ubuntu2 C:\Path\To\Your\New\Directory\ Ubuntu.tar
wsl -d Ubuntu2
```

#### Ubuntu Handy Command:

* Package:
  * Installation steps:
	1. Update package list<br>
		```sudo apt update```
	2. Search for package<br>
		```apt search <keyword>```
	3. install package<br>
		```sudo apt install <package-name>```

  * Uninstallatin steps:
	1. To uninstall the packages you installed:<br>
		```sudo apt remove <package-name>```
	2. If you want to remove the configuration files as well, you can use purge instead of remove:<br>
		```sudo apt purge xfce4 lightdm```
	3. Additionally, if you want to remove any residual dependencies that are no longer needed by any packages on your system, you can run:<br>
		```sudo apt autoremove```


  * Add user:
	```bash
	adduser <username>
	# follow the screen
 	```


  * Delete User:
    ```bash
    sudo userdel <username> # To delete user
    sudo userdel -r <username> # To delete along with home dir
	```
  * Get the List of Users
	```bash
	sudo wc -l /etc/passwd # To get count of users exists in system
	sudo awk -F':' '$7 ~ /^\/home/ {print $1}' /etc/passwd | wc -l	# To get the count of users which are created using "adduser" command
	 ```