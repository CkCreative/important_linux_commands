# my Important Commands

> Memory usage, sorted list

`ps aux  | awk '{print $6/1024  " MB\t\t" $2 "\t" $11}'  | sort -n`

> List all installed apps

`dpkg --get-selections | awk '{print $1}'`

> Memory available

`free -h`

> List installed apps by date

`grep install /var/log/dpkg.log`

> Location of postgress data

`/var/lib/docker/volumes/project_name_volume`

> Copy files

`cp -a /source/. /dest/`

> Size of a directory

`du -shc some_directory`

> Fix for when you cant use ssh

`ssh-keygen -R <host>`

> Edit details of a user *password

`sudo passwd USERNAME`

> Install docker

```bash
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh

```

> Add sudo user

`usermod -aG sudo USER`

> Using psql

`psql "dbname=db host=localhost user=postgres password=postgres port=5432"`

> Backup

`docker exec -t <CONTAINER_ID> pg_dumpall -c -U <DB_USER> | gzip > ~/backup/dump_`date +%d-%m-%Y"_"%H_%M_%S`.gz`

> Restore

`zcat backup_file.gz | docker exec -i <CONTAINER_ID> psql -U <DB_USER>`

> Download youtube mp3

`youtube-dl --extract-audio --audio-format mp3 VIDEO_LINK`

> List tables

`\dt`

> List fields in table

`\d+ <table_name>`

> Range over all items in a directory and rename them

`ls -v | cat -n | while read n f; do mv -n "$f" "$n.ext"; done`
