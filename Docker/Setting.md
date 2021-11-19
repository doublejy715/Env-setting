# 도커 설치하기
## 1. In Linux
[ Link ](https://docs.docker.com/engine/install/ubuntu/)

## 2. In Window
### Install docker
[ Link ](https://goddaehee.tistory.com/251)

### docker GUI in window
[ Link ](https://goddaehee.tistory.com/251)

# 도커 명령어
## 1. docker image 받기
1. docker hub에서 원하는 도커 이미지 검색(repository:tag)
2. docker pull 하기
- docker hub에서 copy하는 문구 있음
- docker pull {docker ID}/{image name}:{tag}
3. 컨테이너 생성
` docker [OPTIONS] IMAGE[:TAG|@DIGEST] [COMMAND] [ARG...] `

## 2. docker image 실행하기
### 처음 container 생성 시
`docker run <OPTIONS> --name <컨테이너 이름> <이미지이름:Tag>`
- <OPTIONS> : --rm -it
- 만약 container를 stop후 계속 유지하고 싶다면 --rm 옵션을 빼주면 된다.
> [추가적인 옵션을 소개한다.](https://subicura.com/2017/01/19/docker-guide-for-beginners-2.html)

### 생성했던 image에 다시 접속하기
`docker exec -it {image name} /bin/bash`
- OPTIONS 에서 --rm은 없다.

### docker container 나가기
`exit`

### Reference
[ Link ](https://89douner.tistory.com/96?category=878197)

## 3. container다루기

### docker container 동작 정지
`docker stop {container name}`
- 반드시 container의 동작을 멈추고 삭제해야 한다.

### docker image & container 삭제
#### docker image 삭제
`docker rmi image_id/image_name`

#### docker container 삭제
`docker rm containter_name`

### docker run 여러 옵션
https://base-on.tistory.com/367
http://pyrasis.com/book/DockerForTheReallyImpatient/Chapter20/28

## 4. Docker in VS Code
1. VS code extension에서 remote development / docker / docker explorer 설치
2. VS code와 Docker 연동하기
3. VS code와 Jupyter notebook 연동하기
4. VS code에서 Docker 컨테이너 실행 및 종료
[ 참조 Link ](https://89douner.tistory.com/123)

## 5. Docker 이미지 만들고 hub에 올리기
### 5.1 이미지 생성
`docker ps -a`
- 생성한 container 파악하기
- container의 id를 파악한다.

`docker commit -a '이름' {container_id} {docker hub id}/{tag}`
- container에 붙일 이미지 이름과 태그를 설정한다.
- -a는 --author 로 대체 가능
- {tag} : 보통 {hub에 검색될 대표적 이름}:{버전 이름/환경 설정}

`docker images`
- 지정한 이미지 이름과 태그로 생성되었는지 확인한다.

### 5.2 도커 로그인 하기
`docker login`
 - 아이디와 패스워드 입력

### 5.3 도커 hub에 push 하기
`docker push {docker_hub_ID}/{image_name}:{tag}`

### 5.4 docker hub 홈페이지에서 확인하기
[ 방법3 ](https://ryu-e.tistory.com/10)

## ETC
### docker nvidia driver 설치
[설명](https://deepflowest.tistory.com/222)

## Reference
[기초](https://fliedcat.tistory.com/111)

## 6 docker file usage
[check](https://velog.io/@ckstn0777/%EB%8F%84%EC%BB%A4%ED%8C%8C%EC%9D%BCDockerfile)