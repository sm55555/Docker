### 일반 유저에게 docker 실행 권한전달

```
usermod -aG docker [username]
```

### 그룹에 추가 했는데도 이슈 아래와 같이 이슈 생길 시

```
Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get http://%2Fvar%2Frun%2Fdocker.sock/v1.40/containers/json: dial unix /var/run/docker.sock: connect: permi


chmod 660 /var/run/docker.sock
```
