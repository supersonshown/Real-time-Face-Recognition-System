# Real-time-Face-Recognition-System
# Real-time Face Recognition (YOLO) | 실시간 얼굴 인식

> 카메라 입력을 이용한 **실시간 얼굴 인식 시스템**. 데이터 파이프라인 구축과 모델 개선으로 **정확도 70% → 98%** 달성, 실시간 추론 성능 구현. (기간: 2024.09–2024.11)  
> 본 README의 지표/기간/핵심 구성은 포트폴리오 슬라이드 내용을 바탕으로 작성되었습니다. :contentReference[oaicite:1]{index=1}

---

## ✨ 주요 기능 & 성과
- YOLO 기반 얼굴 감지/인식 파이프라인
- **정확도 70% → 86% → 98%** 단계적 개선(예: 좌표 확장 등 전처리/후처리 튜닝) :contentReference[oaicite:2]{index=2}
- **약 3만 장** 규모 데이터 **자동화 학습 파이프라인** 구축(라벨 정합/증강/검증 분리) :contentReference[oaicite:3]{index=3}
- OpenCV 스트리밍으로 **실시간 추론**(웹캠/RTSP)

## 🔧 기술 스택
- **Model**: YOLO (PyTorch)
- **Runtime**: Python, PyTorch, OpenCV
- **Train**: Albumentations(선택), DVC/W&B(선택), CUDA

## ⚡ 빠른 시작
```bash
# 1) 환경
python -m venv .venv && source .venv/bin/activate  # Windows: .venv\Scripts\activate
pip install -r requirements.txt

# 2) 가중치/데이터
# - data/ 에 학습/검증 이미지와 labels(yolo format) 배치
# - weights/ 에 베이스 가중치(yolo) 또는 사전학습 가중치 배치

# 3) 실시간 추론(웹캠)
python infer_realtime.py --weights weights/best.pt --source 0

# 4) 이미지/비디오 추론
python infer.py --weights weights/best.pt --source path/to/video.mp4
