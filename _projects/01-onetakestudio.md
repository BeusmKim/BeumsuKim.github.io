---
layout: project
title: OneTakeStudio — AI-Assisted Short-form Editing Pipeline
summary: "STT 기반 하이라이트 구간 선정과 클립 생성 흐름을 제품 형태로 구성"
period: "2026"
role: "AI/Backend"
stack: "Python, faster-whisper, (LLM post-processing), FFmpeg, FastAPI, MSA"
image: /assets/img/projects/onetakestudio_mainpage.png
video: /assets/img/projects/onetakestudio_presentation.mp4
links:
  - label: "Repository"
    url: "https://github.com/username/REPO"
  - label: "Demo"
    url: "https://username.github.io/DEMO"
order: 40
featured: true
---
## Overview
크리에이터 편집 작업에서 가장 큰 비용은 **긴 영상에서 쓸 만한 구간을 찾고, 자막/클립 형태로 정리하는 반복 작업**입니다.  
본 프로젝트는 STT 결과(타임스탬프 포함)를 활용해 **후보 구간을 구조화**하고, 클립 생성까지 연결되는 파이프라인을 구현했습니다.

## Problem
- 긴 영상에서 하이라이트 탐색/선정이 수작업에 의존
- 자막(문장 단위) 품질 및 구간 컷(문장 중간 절단 방지)이 중요
- 편집(무거운 미디어 작업)과 서비스 API가 결합되면 장애 전파/확장이 어려움

## Approach
- **Timestamped STT** 결과를 세그먼트 단위 데이터로 정리
- 문장 단위 보존을 기준으로 하이라이트 후보 구간을 구성(문장 중간 컷 방지)
- FFmpeg 기반으로 클립 생성/렌더링 자동화
- API 서버와 무거운 작업 계층을 분리하는 **MSA 지향 구조** 적용

## Technical Notes
- STT: faster-whisper(Whisper) 기반 타임라인 추출
- Media: FFmpeg/ffprobe로 메타데이터 검증 및 컷/렌더 처리
- Serving: FastAPI 기반 작업 제어, 무거운 처리 분리로 안정성 확보

## Screenshots & Demo
![OneTakeStudio - Main Page]({{ '/assets/img/projects/onetakestudio_mainpage.png' | relative_url }})
![OneTakeStudio - Shorts Generation]({{ '/assets/img/projects/onetakestudio_generate_shorts.png' | relative_url }})
![OneTakeStudio - Shorts Output]({{ '/assets/img/projects/onetakestudio_shorts_output.png' | relative_url }})

## Outcome
- 하이라이트 후보 구간 → 클립 생성까지의 편집 단계를 파이프라인으로 연결
- 운영 관점에서 무거운 미디어 처리와 API를 분리해 확장/격리 가능한 구조를 확보

## What I’d Improve Next
- 품질 지표(선정 정확도, 편집 시간 단축) 정의 및 A/B 기반 평가 체계화
- 작업 큐/배치 계층(AWS Batch 등)으로 렌더 처리의 스케일링 강화
