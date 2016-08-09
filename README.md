# Koken scripts
Utility bash scripts for [Koken](http://koken.me/) websites.

## Backup script
The [koken_backup.sh](koken_backup.sh) script creates a tar.gz archive containing:
* A dump of the mysql database
* The content of the koken website folder, excluding:
    - Cache folders
    - Temp folder `/storage/tmp`

The file name is by default koken_db_backup_date_YYYY-MM-dd_HHmm.tgz.

### Configuration
Simply replace the following parameters in the .sh file:
```sh
dbname="koken_dbname" # (e.g.: dbname=kokendb)
dbhost="your.host" (e.g.: localhost)
dbuser="user" # (e.g.: dbuser=kokenuser)
dbpw="pswd" # (e.g.: dbuser password)

# Website Files
webrootdir="/home/user/koken.yourdomain.com" # (e.g.: webrootdir=/home/user/public_html)

# Destination folder
# Execution directory (script start point)
startdir=/home/user/backups
```

## Restore script


## TODO
* [] Restore script
* [] Incremental save ?
* [] Build a docker container ready to deploy in case of worst case failure
