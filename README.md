# Real-time-Face-Recognition-System
# 🎯 Real-time Face Recognition System
> 카메라를 이용한 실시간 얼굴 인식 모델 개발 프로젝트

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![PyTorch](https://img.shields.io/badge/PyTorch-1.9+-red.svg)](https://pytorch.org/)
[![YOLO](https://img.shields.io/badge/YOLO-v8-yellow.svg)](https://github.com/ultralytics/ultralytics)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.5+-green.svg)](https://opencv.org/)

## 📋 프로젝트 개요

**실시간 얼굴 인식 시스템**은 YOLO 모델을 활용하여 카메라를 통한 실시간 얼굴 인식을 수행하는 프로젝트입니다. 
3만장의 대용량 얼굴 이미지 데이터를 자동화된 파이프라인으로 처리하여 98%의 높은 정확도를 달성했습니다.

### 🎯 주요 목표
- 실시간 카메라 기반 얼굴 인식 구현
- 높은 정확도의 얼굴 검출 및 인식
- 대용량 데이터 처리를 위한 자동화 파이프라인 구축
- 실용적인 성능 최적화

## 🏆 주요 성과
<img width="772" height="269" alt="image" src="https://github.com/user-attachments/assets/85a1ed6d-77e1-437f-a8b1-2e17d2b0d10c" />


### 📈 성능 개선
- **YOLO 모델 정확도 대폭 향상**: `70%` → `98%` (28% 정확도 향상)
- **실시간 처리**: 카메라 피드에서 즉시 얼굴 인식 및 추적
- **안정적인 검출**: 배경 정보 활용으로 false positive 감소

### 🔧 기술적 혁신
- **3만장 데이터셋 구축**: 동영상 프레임 추출 방식으로 효율적 데이터 수집
- **자동화 라벨링**: YOLO 기반 좌표 자동 생성으로 수작업 최소화
- **데이터 파이프라인**: 대용량 데이터 전처리 및 학습 자동화

## 🛠 기술 스택

### 💻 Core Technologies
- **Computer Vision**: YOLO v8, FaceNet, OpenCV
- **Deep Learning**: PyTorch, CNN
- **Data Processing**: NumPy, Python 3.8+

### 📦 Dependencies
```bash
torch>=1.9.0
opencv-python>=4.5.0
ultralytics>=8.0.0
numpy>=1.21.0
pillow>=8.0.0
```

## 🚀 설치 및 실행

### 1. 저장소 클론
```bash
git clone https://github.com/your-username/real-time-face-recognition.git
cd real-time-face-recognition
```

### 2. 가상환경 설정
```bash
python -m venv face_recognition_env
source face_recognition_env/bin/activate  # Linux/Mac
# face_recognition_env\Scripts\activate    # Windows
```

### 3. 의존성 설치
```bash
pip install -r requirements.txt
```

### 4. 실행
```bash
python main.py
```

## 📊 성능 분석

### 정확도 향상 과정
| 단계 | 모델 | 정확도 | 개선사항 |
|------|------|--------|----------|
| 1단계 | 초기 YOLO | 70% | 기본 모델 |
| 2단계 | 좌표 확장 | 86% | 검출 영역 최적화 |
| 3단계 | 최종 모델 | 98% | Augmentation 제거, 배경 정보 활용 |

### 학습 과정
- **에포크**: 100회
- **배치 크기**: 16
- **학습률**: 0.001
- **최적화**: Adam optimizer

## 🔍 기술적 구현

### 데이터 수집 혁신
1. **동영상 프레임 추출**: 연속된 프레임에서 다양한 각도의 얼굴 수집
2. **자동화 라벨링**: YOLO를 활용한 bounding box 자동 생성
3. **품질 필터링**: 흐릿하거나 부분적인 얼굴 제거
4. **데이터 증강**: 밝기, 대비, 회전 등 다양한 변형 적용

### 모델 최적화
- **FaceNet vs YOLO 비교**: 실시간 성능과 정확도 균형점 찾기
- **좌표 범위 확장**: 얼굴 주변 컨텍스트 정보 포함
- **Augmentation 제거**: 과적합 방지 및 실제 환경 적응성 향상
- **배경 정보 활용**: 얼굴과 배경의 대비를 통한 검출 성능 개선


## 📈 결과 및 성과

### 정량적 성과
- **최종 정확도**: 98%
- **처리 속도**: 30 FPS (실시간)
- **데이터셋 크기**: 30,000장
- **False Positive Rate**: 2% 미만

### 정성적 성과
- 다양한 조명 환경에서 안정적 인식
- 여러 얼굴 동시 검출 가능
- 실시간 처리로 실용적 활용 가능

## 🔮 향후 개선 계획

- [ ] 얼굴 인식 정확도 99% 이상 달성
- [ ] 모바일 환경 최적화
- [ ] 실시간 얼굴 추적 기능 추가
- [ ] 마스크 착용 상태에서의 인식 성능 개선
- [ ] Edge device 배포 최적화


## 🙏 감사의 말

- YOLO 개발팀의 우수한 객체 검출 모델
- OpenCV 커뮤니티의 컴퓨터 비전 라이브러리
- PyTorch 팀의 딥러닝 프레임워크

