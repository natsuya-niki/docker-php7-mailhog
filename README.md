# Apache＋php7＋MailhogのDocker環境

## インストール要件

- Git
- Docker(docker-composeコマンドが使えること)

1. docker起動

```bash
## execute source dir
# build and start
$ docker-compose up -d
## only build
$ docker-compose build
```

2. webサイトの表示確認

下記にアクセス: 
http://localhost:8080/phpinfo.php

3. メール送信の確認

    1. 下記にアクセス (Webページからメール送信): 
http://localhost:8080/test_mail.php

    2. 下記にアクセス (メール受信用ページ確認): 
http://localhost:8025/


## 付録

### ホスト名の設定a

```bash
# /etc/hosts
127.0.0.1       localhost       web.mailform.local      mailhog.mailform.local
```

下記のURLでアクセス:

- web: http://web.mailform.local:8080
- mail: http://mailhog.mailform.local:8025
