---
layout: project
title: AWS Hackathon — Distributed Data Center Siting Optimization
summary: "재생에너지/환경 조건을 반영해 최적의 입지 노드 조합을 탐색하는 프로토타입"
period: "2026"
role: "Infra/Data Pipeline"
stack: "AWS (S3, Batch, EC2, IAM), Python, Zarr/Xarray"
image: /assets/img/projects/Tamna-eye_mainpage.png
links:
  - label: "Repository"
    url: "https://github.com/username/REPO"
order: 80
featured: true
---
## Problem
데이터센터 입지 선정은 전력/냉각/통신 등 복합 조건을 동시에 고려해야 하며,  
정적 기준만으로는 계절성/시간대 변동(특히 재생에너지)을 반영하기 어렵습니다.

## Approach
- 노드 단위로 점수(전력/통신/냉각 등)를 정의하고 지도에서 탐색 가능하게 구성
- 배치 처리 기반 파이프라인을 전제로, 대용량 데이터 처리 흐름을 분리 설계
- S3 중심 스토리지/배치 실행 구조로 확장 가능성을 확보

## Screenshots
![Tamna-eye Main Page](/assets/img/projects/Tamna-eye_mainpage.png)
![Tamna-eye Solution](/assets/img/projects/Tamna-eye_solution.png)
![Tamna-eye Presentation](/assets/img/projects/Tamna-eye_presentation.PNG)
![Tamna-eye Jeju Global Space Forum](/assets/img/projects/Tamna-eye_Jeju global space_forum.jpeg)
![Tamna-eye Team Photo](/assets/img/projects/Tamna-eye_단체샷.JPG)

## Outcome
- 사용자 입력(가중치) 기반 탐색 UI/스코어링 로직을 MVP 형태로 구현
- 향후 실제 데이터 연결 시, 배치/스토리지 중심으로 스케일아웃 가능한 구조 확보
