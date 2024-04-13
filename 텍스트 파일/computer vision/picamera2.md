  - 마찬가지로 libcamera으로 OpenCV가 호환되지 않는 문제가 발생하여 위의 이슈를 참고하여 picamera2를 사용했습니다.

  - 도커 컨테이너를 실행할 때 호스트의 웹캠 디바이스를 컨테이너에 볼륨으로 마운트
  - 먼저, 아래와 같이 컨테이너를 실행하여 컨테이너 내부의 셸에 접속합니다

      $ docker run -v /dev/video0:/dev/video0 -it my_container /bin/bash

  - 컨테이너 내부에서 아래의 파이썬 코드를 실행. 이 코드는 picamera2를 사용하여 카메라 프레임을 받아옵니다

    from picamera2 import Picamera2
    import cv2 // 추가한 부분

    picam2 = Picamera2()
    picam2.preview_configuration.main.size = (800,800)
    picam2.preview_configuration.main.format = "RGB888"
    picam2.preview_configuration.align()
    picam2.configure("preview")
    picam2.start()
    
    while True:
       im = picam2.capture_array()
       cv2.imshow("Camera", im)
       if cv2.waitKey(1) == ord('q'):
           break
    
    cv2.destroyAllWindows()

  - 카메라 모듈 부착한 후 카메라로 촬영하는 과정에서 위의 코드가 정상적으로 촬영되는 것인지 확인해주세요
