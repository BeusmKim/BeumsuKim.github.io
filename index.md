---
layout: default
title: Home
subtitle: "Applied AI with production-oriented backend systems"
hide_title: true
---

<div class="home-hero">
  <h1 class="page-title" style="margin:0;">Applied AI × Production Backend</h1>
  <p class="lead">
    음성/영상 중심 워크플로우를 <strong>재현 가능하고 운영 가능한 형태</strong>로 만들기 위해,
    AI 파이프라인(전처리→추론→후처리)과 백엔드/인프라(서빙·배치·스토리지)를 함께 설계합니다.
  </p>

  <div class="home-actions">
    <a class="btn primary" href="{{ "/projects" | relative_url }}">View Projects</a>
    <a class="btn" href="{{ "/experience" | relative_url }}">Experience</a>
    <a class="btn" href="{{ "/assets/resume.pdf" | relative_url }}">Resume</a>
    <a class="btn" href="{{ "/contact" | relative_url }}">Contact</a>
  </div>

  <div class="small-note">
    목표: “데모”가 아니라, 운영/확장/유지보수가 가능한 AI 제품 구조.
  </div>
</div>

<hr/>

## Focus Areas
<div class="grid">
  <div class="card">
    <strong>AI Pipeline Engineering</strong><br/>
    <span class="kpi">병목 정의 → 처리 단위 설계 → 안정적인 운영(재처리/모니터링/실패 복구)을 고려한 파이프라인 구성</span>
  </div>
  <div class="card">
    <strong>Media Processing</strong><br/>
    <span class="kpi">자막/클립/세그먼트 기반 편집을 위한 FFmpeg 워크플로우, 타임스탬프 정합성, 렌더링 자동화</span>
  </div>
  <div class="card">
    <strong>Backend for AI Products</strong><br/>
    <span class="kpi">추론/렌더링 등 무거운 작업 분리, API 서버와 작업 실행 계층 분리(MSA 지향), 운영 관점의 설계</span>
  </div>
  <div class="card">
    <strong>Cloud / Ops</strong><br/>
    <span class="kpi">AWS(S3, Batch, EC2, IAM) 기반 배치 처리 및 스토리지 운영 패턴, 비용/성능 트레이드오프 고려</span>
  </div>
</div>

## Main Tech Stack (AI Focus)
- **Speech / NLP:** faster-whisper(Whisper), Wav2Vec 2.0 기반 STT 활용, 타임스탬프 세그먼트 처리
- **Media:** FFmpeg/ffprobe 기반 구간 컷/메타데이터/렌더링 자동화
- **Serving:** FastAPI 기반 추론/작업 제어 API 설계
- **Architecture:** Microservices-oriented separation (AI inference / heavy media processing)
- **Cloud:** AWS (S3, Batch, EC2, IAM)

## Selected Projects
<div class="grid">
  {% assign featured = site.projects | slice: 0, 4 %}
  {% for p in featured %}
    <a class="project-tile" href="{{ p.url | relative_url }}">
      {% if p.image %}
        <div class="project-thumb"><img src="{{ p.image | relative_url }}" alt="{{ p.title }} thumbnail" /></div>
      {% else %}
        <div class="project-thumb placeholder">No image</div>
      {% endif %}
      <div>
        <div class="project-title">{{ p.title }}</div>
        <div class="kpi">{{ p.summary }}</div>
        <div class="kpi">Stack: {{ p.stack }}</div>
      </div>
    </a>
  {% endfor %}
</div>

