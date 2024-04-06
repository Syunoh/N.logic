## 도커 컨테이너 
  ### 도커 컨테이너 생성 
  
    $docker create [image]

  - docker create 명령어를 입력하면, 도커엔진이 로컬 호스트에서 이미지 정보를 찾아서 컨테이너 생성
  - 만약, 로컬 호스트에 이미지가 없을 경우에는 도커엔진이 자동으로 docker pull을 실행하여 Docker Repoistory에서
    이미지를 가져오는 것을 시도

  ### 도커 컨테이너 시작
  
  **docker start - 도커 컨테이너가 생성되어있다면 시작**
     
    $ docker start [container]

  **docker run - 사실상 docker create 와 start를 합친 명령어**

    $ docker run [option] [image] [command] [args]

  **run [option]**

    1. -i 
      컨테이너와 상호 입출력을 가능하게 합니다.
    2. -t
      터미널 명령을 정상적으로 실행할 수 있도록 설정

    (보통 -it 으로 실행)

    3. --rm 
      컨테이너가 실행 종류될 경우 이미지 자동으로 삭제
    4. -d
      detached모드로 실행(기본적으로 Foreground에서 동작) -it가 컨테이너 내부에 attached 모드로 진입했던 것과 반대
    5. -name 
      컨테이너 이름 설정
    6. -v
      호스트 운영체제와 컨테이너 사이의 파일시스템 디렉토리를 마운트하기 위한 옵션(볼륨에서 다룰 예정)

  ### 도커 컨테이너 종료

  **docker stop - 컨테이너를 안전하게 종료**

  $ docker stop [container]

  **모든 컨테이너 종료**

  $ docker stop ${docker ps -a -q)

  ### 도커 컨테이너 목록 확인

  **실행중인 컨테이너 상태 확인**

  $ docker ps

  **전체 확인 (stop 되어있는 컨테이너 포함)**

  $ docker ps -a

  **컨테이너 상세 정보 확인**

  $ docker inspect [container]

  ### 도커 컨테이너 삭제

  **컨테이너 삭제**

  $ docker rm [container]

  **컨테이너 실행 종료 후 자동 삭제**

  $ docker run --rm [container]

  **중지된 모든 컨테이너 삭제**

  $ docker container prume

  
    
