# 2021년 공개 SW 개발자 대회

## Project : 야간 CCTV 영상화질 개선 및 객체 탐지

### 1.  배경 및 목적

- 통합관제센터의 관제 인력 부족
-  통합관제센터의 저화질 CCTV의 경우 어두운 환경에서 객체 식별에 어려움이 있음.
-  기존의 저화질 CCTV를 단기간에 모두 교체하기에는 예산 문제가 있음

### 2. 개발환경 및 개발언어

### Training 환경
- OS : Ubuntu 20.04 LTS
- GPU : 8 x NVIDIA Tesla P100 PCIe 16GB
- CUDA Toolkit : Driver 460.32, CUDA 11.2
- 사용 언어 : Python 3.7

### 구동 환경
- OS : Windows 10 Pro Build 19043.1165
- CPU: i7-11700K
- RAM: 32GB DDR4
- GPU: GeForce RTX 3080

### 3. 시스템 구성 및 아키텍처

- 저조도 모델 : EnlightenGan(17 Jun 2019  ·  Yifan Jiang, Xinyu Gong, Ding Liu, Yu Cheng, Chen Fang, Xiaohui Shen, Jianchao Yang, Pan Zhou, Zhangyang Wang )
- https://arxiv.org/pdf/1906.06972v2.pdf
- https://github.com/arsenyinfo/EnlightenGAN-inference

- 객체 탐지 모델 : Yolov5
- https://github.com/ultralytics/yolov5

### 4. 모델 학습 결과
epoch 50
![training_results](https://user-images.githubusercontent.com/41338783/132691322-6089e5c8-5598-42ad-ab41-bfa400894b2b.png)

### 5. 프로젝트 주요기능
- 저조도 개선 : 저조도 영상을 입력으로 받아 밝기 개선
- 객체 탐지 : 저조도 영상을 입력으로 받아 저조도 환경에서도 객체에 대한 Bounding Box 출력
- 로그 기록 : 객체 탐지된 영상에 대해서 탐지된 객체의 로그 기록 저장

### 6. 시연 영상
링크 : https://youtu.be/2MXqBcwoJrg
