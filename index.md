---
layout: default
title: Home
subtitle: "AI Engineer · Data Analyst | 분석 → 모델링 → 서비스화"
hide_title: true
---

<div class="home-hero">
  <h1 class="page-title" style="margin:0;">AI × Data × Product Impact</h1>
  <p class="lead">
    저는 <strong>데이터 분석으로 문제를 구조화하고, 모델링 결과를 실제 기능으로 연결</strong>하는 AI/데이터 실무형 인재입니다.
    성능 수치만이 아니라 <strong>전처리·후처리·평가 지표·배포 흐름</strong>까지 설계해
    현업에서 재사용 가능한 분석/AI 기능을 구현합니다.
  </p>

  <div class="home-actions">
    <a class="btn primary" href="{{ "/projects" | relative_url }}">Projects</a>
    <a class="btn" href="{{ "/experience" | relative_url }}">Experience</a>
    <a class="btn" href="{{ "/assets/resume.pdf" | relative_url }}">Resume</a>
    <a class="btn" href="{{ "/contact" | relative_url }}">Contact</a>
  </div>

  <div class="small-note">
    지향점: 분석 리포트에서 끝나지 않고, 모델/로직을 제품 기능과 운영 프로세스까지 닫히게 만드는 것.
  </div>
</div>

<hr/>

## Core Strengths
<div class="grid">
  <div class="card">
    <strong>Data Analysis & Problem Framing</strong><br/>
    <span class="kpi">CRM/사용자 로그/구매 이력 분석으로 핵심 변수를 정의하고, 전환/이탈 예측이 가능한 문제 구조로 재정의</span>
  </div>
  <div class="card">
    <strong>Modeling & Evaluation</strong><br/>
    <span class="kpi">분류/회귀 모델 설계, 지표 기반 성능 검증, 실패 케이스 분석을 통한 반복 개선 체계 운영</span>
  </div>
  <div class="card">
    <strong>Applied AI (LLM / Vision)</strong><br/>
    <span class="kpi">VQA/추천/메시지 생성 문제에서 모델 학습과 추론 보정 전략을 결합해 성능 정체 구간을 돌파</span>
  </div>
  <div class="card">
    <strong>Productization & Automation</strong><br/>
    <span class="kpi">FastAPI/파이프라인 기반으로 분석·모델 결과를 기능화하고, 팀이 바로 실행 가능한 워크플로우로 연결</span>
  </div>
</div>

## Main Tech Stack
- **Data Analysis:** Python, pandas, numpy, (SQL 분석), 고객/매출/로그 데이터 기반 Segmentation, Feature Engineering
- **ML/AI:** scikit-learn 기반 분류/회귀, PyTorch/Transformers 실험 경험, LTV/이탈 예측·추천 문제 모델링, VQA/LLM 튜닝 및 추론 보정 전략
- **Evaluation:** 지표 정의, 실험 설계(가설–검증), 오류/실패 케이스 분석, 성능 정체 구간에서의 개선 전략(후처리·룰·보정)
- **Serving / Productization:** FastAPI 기반 API/파이프라인 설계, 결과를 메시지/스크립트/타깃팅 시나리오 등 실행 단위로 패키징
- **Planning & Sales:** 목표 구조 재설계, 상담 스크립트/프로세스 표준화, CRM 기반 실행 운영, 온·오프라인 판매/마케팅 기획 경험
- **Collaboration:** Git/GitHub, 재현 가능한 문서화, 프로젝트 구조화 및 운영 관점 정리

## Featured Projects
<div class="grid">
  {% assign featured = site.projects | where: "featured", true | sort: "order" %}
  {% assign featured = featured | slice: 0, 4 %}
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
