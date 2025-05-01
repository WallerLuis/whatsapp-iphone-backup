# Own edits: Luis Waller 01.05.2025

Fork of: https://github.com/rayed/whatsapp-iphone-backup

## How to use:

1. Install go:https://dev.to/deadwin19/how-to-install-golang-on-wslwsl2-2880
2. git clone https://github.com/rayed/whatsapp-iphone-backup.git
3. cd whatsapp-iphone-backup
4. go mod init [github.com/WallerLuis/whatsapp-iphone-backup](http://github.com/WallerLuis/whatsapp-iphone-backup)
5. go get [github.com/mattn/go-sqlite3](http://github.com/mattn/go-sqlite3)
6. go build -o exporter \*.go
7. ./exporter -dst "/mnt/c/Users/LuwiY/Nextcloud/WhatsApp/01-05-2025/" -src "/mnt/c/Users/LuwiY/Apple/MobileSync/Backup/00008030-000C51122185802E/”

# WhatsApp iPhone Backup Toola

Export WhatsApp application data from iPhone backup.

The exporter export media files, pictures, movies, audio, etc ... and also export
chat messages as HTML files.

The exporter works on iTunes backup for iPhone. You need to backup your iPhone using
iTunes and make sure you disable encryption. You can enable it again after exporting
WhatApp.

iTunes keep iPhone backup under the folder:

    $HOME/Library/Application Support/MobileSync/Backup/XXXXX-XXXXX/

The ID part changes depend on your setup.

## Running

    go get github.com/mattn/go-sqlite3
    go build -o exporter *.go
    ./exporter -dst "$HOME/whatsapp-backup" -src "$HOME/Library/Application Support/MobileSync/Backup/XXXXX-XXXXX/"
