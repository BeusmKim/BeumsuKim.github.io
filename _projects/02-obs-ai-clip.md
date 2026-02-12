---
layout: project
title: OBS Video Clip Automation — Segment Cutting & Subtitle Workflow
summary: "OBS 환경에서 영상 구간 컷/자막 워크플로우를 자동화하는 도구 흐름 설계"
period: "2026"
role: "Backend / Media Pipeline"
stack: "Python, FFmpeg, faster-whisper, Windows 환경 운영"
image: /assets/img/projects/obs-clip-placeholder.jpg
links:
  - label: "Repository"
    url: "https://github.com/username/REPO"
---
## Problem
- OBS/로컬 환경에서 영상 처리 도구 체인이 길어질수록 설치/경로/호환성 이슈가 잦음
- ffprobe 출력 포맷 등 실무적인 예외 처리 미흡 시 전체 파이프라인이 중단

## Approach
- ffprobe 기반 메타데이터 파싱을 안정화(출력 포맷 예외 대응)
- 구간 컷 중심으로 MVP 범위를 명확히 하고, 자막은 후처리/레이아웃 제공 방식으로 분리
- Windows 개발 환경에서 재현 가능한 실행 절차를 문서화

## Result
- 구간 컷 및 처리 흐름을 단순화해 “동작하는 MVP” 기준을 확보
- 운영/배포 관점에서 실패 지점을 빠르게 특정 가능한 형태로 개선
