## 도커 컨테이너 
  ### 도커 컨테이너 생성 
  
    $docker create [image]

  - docker create 명령어를 입력하면, 도커엔진이 로컬 호스트에서 이미지 정보를 찾아서 컨테이너 생성
  - 만약, 로컬 호스트에 이미지가 없을 경우에는 도커엔진이 자동으로 docker pull을 실행하여 Docker Repoistory에서
    이미지를 가져오는 것을 시도

  ### 도커 컨테이너 시작
  1. docker start - 도커 컨테이너가 생성되어있다면 시작
     
    $ docker start [container]

  2.  docker run - 사실상 docker create 와 start를 합친 명령어

    $ docker run [option] [image] [command] [args]

    -
    
