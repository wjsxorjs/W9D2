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
> > > grant all privileges on [db_name].* to [user_name]@'[host]' with grant option; : 유저에게 권한부여 <br>
