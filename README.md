# Custom Gnome .desktop files

For software that doesn't have one provided

**Acquire software and extract to /opt**

To make sure features such as self-update work, `chown` the directory e.g. 
`sudo chown -R steve:steve /opt/postman`
TODO: does this mean they should be installed to a different location, .e.g ~/bin or ~/.local or something

**Create symlinks to executables in /usr/local/bin**
This means our application will be accessible from command line since /usr/local/bin is in our $PATH
`sudo ln -s /opt/postman/Postman /usr/local/bin/postman`

**Validate the .desktop file if you've edited it**
`desktop-file-validate postman.desktop`

**For local user only**
`desktop-file-install --dir=/home/steve/.local/share/applications postman.desktop`

**For all users (/usr/share/applications/)**
Fixme: this may have changed since I last tried it, check
`sudo desktop-file-install postman.desktop`
