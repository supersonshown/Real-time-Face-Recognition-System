# Real-time-Face-Recognition-System
# Real-time Face Recognition (YOLO) | 실시간 얼굴 인식
<img width="1600" height="900" alt="image" src="https://github.com/user-attachments/assets/5789989a-4fc2-4851-859e-10349438a4f0" />

# 🎯 Real-time Face Recognition System
> YOLO 기반 실시간 얼굴 인식 시스템 | 정확도 70% → 98% 달성

![Face Recognition Demo](./images/face_recognition_demo.gif)

## 📌 프로젝트 개요
카메라를 통한 실시간 얼굴 인식 모델 개발 프로젝트로, YOLO 모델의 정확도를 70%에서 98%까지 향상시킨 컴퓨터 비전 프로젝트입니다.

## 🚀 주요 성과
- **정확도 향상**: YOLO 모델 정확도 70% → 98% (28%p 향상)
- **데이터 파이프라인**: 3만장 얼굴 이미지 자동화 파이프라인 구축
- **실시간 처리**: 실시간 얼굴 인식 성능 구현

## 🛠 기술 스택
- **Model**: YOLO, FaceNet
- **Framework**: PyTorch, OpenCV
- **Language**: Python
- **Tools**: NumPy, CNN, Fine-tuning

## 📊 성능 개선 과정
![Performance Graph](./images/performance_graph.png)

### 1단계: 초기 YOLO (70%)
- 기본 YOLO 모델 적용
- 제한적인 얼굴 인식 성능

### 2단계: 좌표 확장 (86%)
- 바운딩 박스 좌표 범위 확장
- 얼굴 주변 컨텍스트 정보 활용

### 3단계: 최종 모델 (98%)
- Augmentation 제거로 정확도 향상
- 배경 정보 활용한 성능 개선

