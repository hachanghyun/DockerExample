# Docker에 Mysql 설치하기 

## 명령어 

    <이미지 다운>
    docker pull mysql

    <이미지 run>
    docker run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=password --name mysqlCont mysql

혹은 비밀번호를 지정안하려면

    docker run -d -p 3306:3306 -e MYSQL_ALLOW_EMPTY_PASSWORD=yes --name mysqlCont mysql

    docker run --platform linux/amd64 -p 3306:3306 --name mysql -e MYSQL_ALLOW_EMPTY_PASSWORD=YES -e MYSQL_DATABASE=SALESMEMO_LOCAL -d mysql:5.6

    <mysql 컨테이너 접속>
    docker exec -it mysqlCont /bin/bash

    <비밀번호 입력>
    mysql -u root -p

    비밀번호 입력창 나옴

    <비밀번호 없으면>
    mysql -u root

