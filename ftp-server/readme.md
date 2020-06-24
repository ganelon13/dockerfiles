Docker FTP Server
=================

## Add user
```bash
sudo docker exec -it ftpserver_ftpserver_1 sh
> pure-pw useradd test -u ftpuser -d /home/ftpusers/test
> pure-pw mkdb
```

## Test connection
```bash
ftp -p localhost 21
ftp> user test
ftp> ls
```
