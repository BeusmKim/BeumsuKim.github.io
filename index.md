---
layout: default
title: Home
subtitle: "Applied AI with production-oriented backend systems"
---

## Summary
Applied AI를 실제 제품/워크플로우에 올리는 데 집중합니다.  
음성/영상 처리 파이프라인과 API 기반 서비스 구조를 결합해 **재현 가능하고 운영 가능한 형태**로 구현합니다.

## Core Strengths
- **AI Pipeline Engineering:** 전처리/추론/후처리의 병목을 정의하고, 처리 단위를 설계하여 안정적으로 운영 가능하게 구성
- **Media Processing:** 자막/클립/세그먼트 기반 편집을 위한 처리 로직 및 워크플로우 설계
- **Backend for AI Products:** 추론/렌더링 등 무거운 작업을 분리하고, API 서버와 작업 실행 계층을 분리하는 아키텍처 지향

## Main Tech Stack (AI Focus)
- **Speech / NLP:** faster-whisper(Whisper), Wav2Vec 2.0 기반 STT 활용, 타임스탬프 세그먼트 처리
- **Media Processing:** FFmpeg/ffprobe 기반 영상 메타데이터/세그먼트 컷/렌더링 자동화
- **Serving:** FastAPI 기반 추론/작업 제어 API 설계
- **Architecture:** Microservices-oriented separation (AI inference / heavy media processing)
- **Cloud / Ops:** AWS (S3, Batch, EC2, IAM) 기반 배치 처리 및 스토리지 운영 패턴

## Featured Projects
<div class="card">
  <strong>OBS 기반 영상 워크플로우 자동화</strong><br/>
  <span class="kpi">STT → 하이라이트 구간 선정 → 클립 생성/편집으로 이어지는 파이프라인 구성</span><br/>
  Repo: (링크) · Demo: (링크)
</div>

<div class="card">
  <strong>CRM 기반 고객 응대/세일즈 개선</strong><br/>
  <span class="kpi">상담 흐름/데이터 정리 → 운영 효율 및 성과 개선 중심으로 설계</span><br/>
  Repo/Docs: (링크)
</div>

<div class="card">
  <strong>AI 이미지 분석 프로젝트</strong><br/>
  <span class="kpi">데이터 전처리/추론/후처리 흐름 정리 및 실험 반복 기반 개선</span><br/>
  Repo: (링크)
</div>
