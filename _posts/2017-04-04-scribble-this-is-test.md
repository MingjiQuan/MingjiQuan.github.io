---
title: ssss
date: 2013-05-06 15:27:31
---

<br><br><br><br><br>
# <center>Things Framework### <center>Developers’ Guide
<br><br><br><br><br>










### <center>2017.03
<br>### <center>Hatio Lab. 기술 연구소1
<center>![](./images/image0.png)</center>
<br><br><br><br><br><br><br><br><br><br><br><br>
### 1 개발환경 구성
#### 1.1	Server
기본 개발 환경

|  구분    |     항목 |   권장버전  |
| :--------: | :--------:| :------: |
| 기본환경   |   Java Development Kit |  1.8  |
|   |   Servlet  |  3.0 이상  |
|   |   Spring Tool Suite   |  3.8.3  |
|  Database     |   PostgreSQL    |  3.0 이상  |
|  WAS          |   Tomcat   |  8.0.30 이상 |
|  Cache Server |   Redis   |  3.0 이상  |

##### 1.1.1	Install Java

Oracle Homepage에서 JDK 8를 Download 받는다.https://java.com/ko/download/파일을 실행하여 설치를 실행한다.![](./image/image1.png)

환경 변수 등록을 위해, '제어판-시스템-고급시스템-고급-환경변수'를 실행한다.

![](./image/image2.png)

시스템 변수에 '새로 만들기'를 클릭하여 시스템 변수를 등록한다.

![](./image/image3.png)
![](./image/image4.png)
![](./image/image5.png)

Path 변수에 아래와 같이 설정을 추가한다.
![](./image/image6.png)

명령 프롬프트를 실행하여, JDK가 정상적으로 설치되었는지 확인한다.![](./image/image7.png)


##### 1.1.2	Install PostgresSQL

http://www.enterprisedb.com/products-services-training/pgdownload#windows접속 후, 자신의 OS환경에 맞는 파일을 다운로드 한다.
![](./image/image8.png)

postgres를 설치하면 서버와 함께 관리자 클라이언트(PgAmin)가 설치될 것이다. 여기서는 pgAdmin을 이용하여 관리하는 내용을 설명한다.프로그램 설치 후 'pgAdmin'을 실행하여 Database를 생성한다.

![](./image/image9.png)
![](./image/image10.png)

##### 1.1.3	Install Redis

https://github.com/MSOpenTech/redis/releases접속 후, 설치파일 다운로드를 실행한다

![](./image/image11.png)

설치 파일을 실행하여 설치를 진행한다.설치가 완료되었다면 'redis-server.exe' 파일을 실행하여, Redis Server를 실행한다.(Console 창이 잠시 표시되었다가 사라 짐.)

![](./image/image12.png)

Redis Client를 실행하여, Redis가 정상적으로 수행중인지 확인한다.( 'ping' 입력 시 'PONG'으로 Return )
![](./image/image13.png)##### 1.1.4	Install Spring STS

https://spring.io/tools/sts/all접속 후, 자신의 OS환경에 맞는 3.8.3버전을 다운로드 한다.![](./image/image14.png)
압축을 해제한 후, STS.exe 파일을 실행하여 프로그램을 실행한다.

###### Buildship Gradle Plugin 설치
STS를 열고 Help - Eclipse Marketplace 실행한다.![](./image/image15.png)

검색 필드에 "Buildship"를 검색하여 Buildship Gradle을 설치한다.

![](./image/image16.png)

##### 1.1.5 프로젝트 셋업

Eclipse 실행 후, Git연동을 위해 Git Perspective를 추가한다.![](./image/image17.png)

소스코드를 내려받기위해, Clone Repository를 생성한다.
( X-MES : https://github.com/hatiolab/xmes-master.git)
( X-MES : https://github.com/hatiolab/elidom.git )![](./image/image18.png)

![](./image/image19.png)

Package Explorer에서 import>Gradle>Existing Gradle project을 선택하여 Next한다.