---
layout: project
title: AI Image Analysis Pipeline — Preprocess → Inference → Postprocess
summary: "CV 파이프라인을 반복 개선 가능한 형태로 정리하고 실패 케이스 중심으로 고도화"
period: "2025–2026"
role: "AI Engineer"
stack: "Python, (Model), Data Pre/Post Processing"
image: /assets/img/projects/image-analysis-placeholder.jpg
links:
  - label: "Repository"
    url: "https://github.com/username/REPO"
---
## Problem
모델 성능은 단순 학습보다 **데이터 품질/전처리/후처리의 설계**에 의해 크게 흔들립니다.  
본 프로젝트는 전체 파이프라인을 모듈화해 개선 사이클이 빠르게 돌 수 있게 구성했습니다.

## Approach
- 입력 표준화(리사이즈/정규화/필터링)와 출력 후처리를 명확히 분리
- 실패 케이스를 수집/분류하여 개선 우선순위를 결정
- 추론 결과를 제품에서 사용할 수 있는 형태로 변환(좌표/클래스/스코어 등)

## Next
- 데이터 버전관리 및 실험 로그 체계화
- 서빙(FastAPI 등)과 배치 추론 분리
