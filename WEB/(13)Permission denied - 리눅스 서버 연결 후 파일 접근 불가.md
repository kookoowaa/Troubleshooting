## Problem

### Web

```web-idl
Forbidden

You don't have permission to access / on this server.
```

### Error log

```shell
[Thu Sep 26 17:02:51.401841 2013] [core:error] [pid 29603:tid 140488246032128] (13)Permission denied: [client 211.222.111.123:62022] AH00035: access to / denied (filesystem path '/home/webuser/htdocs') because search permissions are missing on a component of the path
```



## Resolution

- 파일에 실행 권한 부여 (예를 들어 index.py)

```shell
sudo chmod a+x index.py
```

- 디렉토리에 일반사용자 실행권한 부여 (예를 들어 htdocs/web)

```shel
chmod 711 /var/www/html/htdocs/web
```



