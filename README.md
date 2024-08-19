# W9D2
> Day 2 of Linux

# JDBC 설치
> apt-get install libmariadb-java : JDBC 드라이버 설치 <br>
> ln -s /usr/share/java/mysql-connector-java.jar /usr/share/tomcat9/lib/mysql-connector-java.jar <br>
> : JDK와 TOMCAT을 JDBC 드라이버로 연결 <br>
> service tomcat10 restart : TOMCAT(version 10) 재시작<br>

# MYSQL
> mysql -u [username] -p => [input password] <br>
> : 비밀번호를 입력하면 해당 유저(계정)으로 mysql에 접속을 한 것 <br>
> ## MYSQL 내부 명령어
> > show databases : 데이터베이스 목록 확인 <br>
> > create database [db_name] [option] : 데이터베이스 생성 <br>
> > use [db_name] : 데이터베이스 사용 <br>
> > ### mysql database에서
> > > select user,host from user; : 데이터베이스 내의 유저와 해당 유저의 제한호스트범위 <br>
> > ### root 계정에서
> > > create user [user_name]@'[host]' identified by '[password]'; : 유저 생성 <br>
> > > grant all privileges on [db_name].* to [user_name]@'[host]' with grant option; <br> : 유저에게 권한부여

# GIT
> (sudo) apt-get install git : GIT 설치

# index.html
> cd /var/lib/tomcat10/webapps/ROOT : TOMCAT이 설치된 root로 이동 <br>
> vi index.html : 하위 index.html 확인 및 수정 <br>
> ## Browser에서
> > `[public Ipv4]:[portnum]`로 브라우저에서 index.html 확인 가능

# NGINX
> apt-get install nginx : nginx 설치 <br>
> service nginx start: nginx 실행 <br>
> ## Browser에서
> > `[public Ipv4]`로 브라우저에서 nginx 설치 및 적용여부 확인 가능 <br>
> > /usr/share/nginx/html/index.html의 내용이 화면에 표시된다.

<br> <br>

___
AWS 내부의 TOMCAT은 대부분 8080의 port번호를 가진다.<br>
외부에서 localhost(혹은 퍼블릭 IPv4 주소):8080을 통해 접근할 수 있다.<br>
NginX는 포트번호 80을 가진다.<br>
외부에서 localhost(혹은 퍼블릭 IPv4 주소)(:80)를 통해 접근할 수 있다.<br>
이때, NginX는 WAS와, Tomcat은 Container와 같은 역할을 하기에
Tomcat에 프로젝트나 표시하고자 하는 것들을 저장하고, NginX에서는 proxy를 이용하여<br>
NginX로 접근하더라도 Tomcat으로 접근해주어 표시하고자하는 자원을 접근시켜준다.
___
