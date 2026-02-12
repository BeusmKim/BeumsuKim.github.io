---
layout: default
title: Projects
subtitle: "Selected work — problem, approach, and technical decisions"
permalink: /projects
---

## 1) OBS 기반 영상 워크플로우 자동화
<div class="card">
<strong>Problem</strong><br/>
영상에서 핵심 구간을 빠르게 추출하고, 배포 가능한 형태로 자동 편집 흐름을 구성해야 함.<br/><br/>

<strong>Approach</strong><br/>
- STT 결과(타임스탬프 포함)를 기반으로 세그먼트 생성<br/>
- FFmpeg 기반 클립 생성 및 렌더링 자동화<br/>
- API 서버(FastAPI)와 무거운 처리(렌더 작업)를 분리<br/><br/>

<strong>Tech</strong><br/>
faster-whisper(Whisper), FFmpeg/ffprobe, FastAPI, (AWS Batch/S3 적용 가능)<br/><br/>

<strong>Links</strong><br/>
Repo: (링크) · Demo: (링크) · Docs: (링크)
</div>

## 2) AI 이미지 분석 프로젝트
<div class="card">
<strong>Problem</strong><br/>
(문제 정의 1~2문장)<br/><br/>

<strong>Approach</strong><br/>
- 데이터 전처리 → 추론 → 후처리 파이프라인 정리<br/>
- 실패 케이스 중심으로 개선 반복<br/><br/>

<strong>Tech</strong><br/>
Python, (모델/프레임워크), (추론/서빙)<br/><br/>

<strong>Links</strong><br/>
Repo: (링크)
</div>
