
# Validate the .desktop file if you've edited it
`desktop-file-validate postman.desktop`

## For local user only
`desktop-file-install --dir=.local/share/applications postman.desktop`

## For all users (/usr/share/applications/)
`sudo desktop-file-install postman.desktop`
