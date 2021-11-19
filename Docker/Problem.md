# 1. Install 
## WSL 2 installation is incomplete
[ Link ](https://blog.naver.com/PostView.nhn?isHttpsRedirect=true&blogId=brainkorea&logNo=222208329797&categoryNo=86&parentCategoryNo=0&viewDate=&currentPage=1&postListTopCurrentPage=1&from=search)

## docker toolbox
### Docker Toolbox pre-create check Error
![image](https://user-images.githubusercontent.com/54474501/133596665-d6ceec85-26ed-41af-a86e-06bcb9b79e87.png)

#### Solve
[ Link ](https://janghyeonjun.github.io/issue/docker_toolbox_error/)

# 2. Start
## Error Message
> Got permission denied while trying to connect to the Docker daemon socket at unix:///var/run/docker.sock: Get "http://%2Fvar%2Frun%2Fdocker.sock/v1.24/containers/json": dial unix /var/run/docker.sock: connect: permission denied

## Solve
[ Link ](https://seulcode.tistory.com/557)

# 3. run
## Error Message
cannot update snap namespace: cannot create symlink in "/etc/docker": existing file in the way
snap-update-ns failed with code 1

## Solve
[ Link ](https://exerror.com/cannot-update-snap-namespace-cannot-create-symlink-in-etc-docker-existing-file-in-the-way-snap-update-ns-failed-with-code-1/)

# 4. Push
## Error Message
An image does not exist locally with the tag ~~

## Solve
[ Link ](https://taewooblog.tistory.com/entry/docker-push-%EC%97%90%EB%9F%AC-An-image-does-not-exist-locally-with-the-tag-1013cmcoupangapi)
- 자신의 docker repository 이름과 local의 이미지 이름이 달라서 발생하는 에러
- push하기 위해서 image 이름 조건은 : {docker ID}/{image name} 형식이어야 한다.

# 5. Login
## Error Message
Login did not succeed, error: Error response from daemon ~~

## Solve
[ Link ](https://wings2pc.tistory.com/entry/%EB%8F%84%EC%BB%A4Docker-Error-response-from-daemon-%ED%95%B4%EA%B2%B0-%EB%B0%A9%EB%B2%95)