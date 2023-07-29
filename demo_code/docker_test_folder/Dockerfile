# 1. 첫번째 단계 - Dockerfile 작성

# 오픈 소스용 TensorFlow 도커 이미지 다운로드
FROM tensorflow/tensorflow:latest-gpu-jupyter

# 컨테이너를 생성하는 데 필수 기능을 포함하는 sagemaker-training toolkit 설치
RUN pip3 install sagemaker-training

# 훈련 코드를 컨테이너 안에 복사하기 
COPY train.py /opt/ml/code/train.py

# 스크립트 엔트리포인트로써 train.py 이름을 정의
ENV SAGEMAKER_PROGRAM train.py