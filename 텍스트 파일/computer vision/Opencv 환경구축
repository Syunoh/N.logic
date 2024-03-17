# OpenCV 환경 구축

## 관련 라이브러리 설치하기

- 먼저 업데이트부터

  $ sudo apt-get update
  $ sudo apt-get upgrade

- 업데이트 후에 먼저 개발 툴을 설치

  $ sudo apt-get install build-essential
  $ sudo apt-get install cmake
  $ sudo apt-get install pkg-config

- 이미지 파일을 열 수 있도록 관련 라이브러리들을 설치

$ sudo apt-get install libjpeg-dev
$ sudo apt-get install libtiff5-dev
$ sudo apt-get install libjasper-dev
$ sudo apt-get install libpng12-dev 

- 비디오 파일에 대한 라이브러리를 설치

$ sudo apt-get install libavcodec-dev
$ sudo apt-get install libavformat-dev
$ sudo apt-get install libswscale-dev
$ sudo apt-get install libv4l-dev
$ sudo apt-get install libxvidcore-dev
$ sudo apt-get install libx264-dev

- 서브모델 (이미지를 스크린에 출력하거나 간단한 GUI를 만드는데 사용)

$ sudo apt-get install libgtk2.0-dev
$ sudo apt-get install libgtk-3-dev

- OpenCV 내의 행렬 연산을 최적화

$ sudo apt-get install libatlas-base-dev
$ sudo apt-get install gfortran

- OpenCV를 파이썬으로 사용할 수 있도록 파이썬 헤더를 설치

$ sudo apt-get install python2.7-dev
$ sudo apt-get install python3-dev

## OpenCV 설치

- OpenCV 공식 GitHub 저장소에서 3.3.0버전을 설치

$ cd ~
$ wget -O opencv.zip https://github.com/Itseez/opencv/archive/3.3.0.zip
$ unzip opencv.zip

- 추가 라이브러리인 contrib 다운로드

$ wget -O opencv_contrib.zip https://github.com/Itseez/opencv_contrib/archive/3.3.0.zip
$ unzip opencv_contrib.zip

- PIP를 업데이트

$ wget https://bootstrap.pypa.io/get-pip.py
$ sudo python get-pip.py
$ sudo python3 get-pip.py

- 가상환경 툴을 설치

$ echo -e "\n# virtualenv and virtualenvwrapper" >> ~/.profile
$ echo "export WORKON_HOME=$HOME/.virtualenvs" >> ~/.profile
$ echo "source /usr/local/bin/virtualenvwrapper.sh" >> ~/.profile

- 

