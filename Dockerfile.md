
해당 공간에 Dockerfile 및 test.jar 준비

```
FROM openjdk:11
ARG JAR_FILE=test.jar
COPY ${JAR_FILE} app.jar
ENTRYPOINT ["java","-jar","/app.jar"]

```

# 이미지 생성
sudo docker build -t ec2/spring-server .
 
# 컨테이너 실행
sudo docker run -d --name spring_server -p 8080:8080 ec2/spring-server
 
# 로그 보기
sudo docker logs -f spring-server

