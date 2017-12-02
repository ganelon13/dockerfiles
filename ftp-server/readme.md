Docker FTP Server
=================

## Add user

1. `$ sudo docker exec -it ftpserver_ftpserver_1 sh`
2. `# pure-pw useradd test -u ftpuser -d /home/ftpusers/test`
3. `# pure-pw mkdb`

## Test connection

1. `$ ftp -p localhost 21`
2. `ftp> user test`
3. `ftp> ls`
