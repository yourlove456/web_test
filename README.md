########@ 설치 @#########
1. docker desktop 설치
2. wsl_update 설치
3. git 설치
4. vscode (등 IDE) 설치

########@ 설정 @#########
1. vscode 터미널( Ctrl + ~ )에서 만든 폴더로 이동 후
   git clone 깃허브주소

2. docker run [이미지명] : [태그]   #이미지 다운받고 바로 컨테이너 실행하여 진입

3. docker exec -it [컨테이너명] bash   #리눅스 가상환경 진입

4.  #모든 컨테이너와 이미지 등 도커 요소 중지 및 삭제
docker stop $(docker ps -aq)
docker system prune -a

5. docker build -t frontend-img .
6. docker run --name frontend-con -v ${pwd}:/home/node/app -p 8080:8080 frontend-img

netstat -a -o
taskkill /f /pid [number]



1. backend 도커 이미지 만들기
  docker build -f backend.Dockerfile -t backend .
2. front 도커 이미지 만들기
  docker build -f front.Dockerfile -t front .
3. 도커 컨테이너 만들기
  docker-compose -f db_compose.yml up -d
4. 웹에 접속하기
  localhost:3000/main


가상환경 진입 : docker run -it —rm front /bin/bash
