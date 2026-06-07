# AIDAS Lab 기술 심층 분석 보고서

> **AIDAS Lab** (AI, Big Data, and System Laboratory @ Seoul National University)
> 웹사이트: https://aidas.snu.ac.kr/ | 이메일: aidas.snu@gmail.com
> 분석 기준일: 2026년 6월 7일

---

## 목차

1. [연구 그룹 개요](#1-연구-그룹-개요)
2. [분야별 심층 기술 분석](#2-분야별-심층-기술-분석)
3. [저장소 전체 목록 요약](#3-저장소-전체-목록-요약)
4. [연구 간 시너지 맵](#4-연구-간-시너지-맵)
5. [종합 강점·약점·시사점 분석](#5-종합-강점약점시사점-분석)
6. [FAQ](#6-faq)

---

## 1. 연구 그룹 개요

AIDAS Lab(AI, Big Data, and System Laboratory)은 서울대학교(SNU)에 소속된 인공지능 연구 그룹으로, AI 기술의 **기초 알고리즘 연구부터 빅데이터 시스템 설계, 헬스케어 응용까지** 수직 통합된 연구를 수행한다.

| 항목 | 내용 |
|------|------|
| 소속 | 서울대학교 (SNU) |
| 공개 멤버 | 약 6명 |
| 공개 저장소 수 | 23개 |
| 주요 언어 | Python, JavaScript, HTML |
| 주요 학회 | ICML, CVPR, NeurIPS, ICLR, AAAI, ACL |

### 학술 성과 요약

| 학회 | 연도 | 논문 수 |
|------|------|---------|
| ICML | 2025/2026 | 2편 |
| CVPR | 2026 (Oral 포함) | 2편 |
| NeurIPS | 2025 | 3편 |
| ICLR | 2026 | 1편 |
| AAAI | 2025 | 1편 |
| ACL | 2026 | 2편 |

---

## 2. 분야별 심층 기술 분석

### 분야 1. 생성형 AI — 확산 언어 모델(Diffusion LLM)

#### Dynin-Omni (arXiv 2026) ⭐45
- 8B 규모 마스킹 확산 기반 오니모달 통합 모델
- 텍스트, 이미지, 비디오, 음성을 단일 아키텍처에서 처리
- 양방향 문맥 모델링, 병렬 다중 토큰 생성 지원
- Stage 1(모달리티 적응) → Stage 2(오니모달 SFT+모델 병합) → Stage 3(능력 확장)

#### TTA-Diffusion (NeurIPS 2025) ⭐2
- 확산 LLM의 편집 희석(fade) 문제 해결
- 토큰 타임스텝 할당(TTA) 기법으로 편집 보존력 극대화

#### VALUEFLOW (ICML 2026)
- 다원적·제어 가능한 값 기반 정렬 프레임워크
- 사용자가 원하는 가치 방향으로 모델 출력을 실시간 조정

#### Awesome-Diffusion-LLM ⭐80 / 🍴13
- 확산 LLM 논문 종합 자료집 (107회 커밋, 컨트리뷰터 9명)
- 이산/마스킹 확산, AR 대응, 추론/정렬, 시스템 효율성 등 6대 분류

---

### 분야 2. 비전-언어 모델(VLM)

#### SECOND (ICML 2025) ⭐7
- 선택적 대조 디코딩으로 VLM 지각적 환각 완화
- 기반: LLaVA-NeXT

#### MEDIC-AD (CVPR 2026 Oral) ⭐18
- 임상 워크플로우: 이상 탐지 → 차이 추론 → 시각적 설명
- 파트너: NVIDIA NVAITC, 삼성 창원병원, 삼성서울병원
- HuggingFace 모델 공개: wooohyeooon/MEDIC-AD

#### MI-CXR (ACL 2026) ⭐3
- 5회 방문 흉부 X선 종단면 추론 벤치마크
- 14개 VLM 평가 결과 평균 29.3% (무작위 20%)
- 작업군: TEL / ICR / GTS

#### MMPB (NeurIPS 2025) ⭐9
- 멀티모달 개인화 최초 벤치마크
- VLMEvalKit 기반 자동 평가

---

### 분야 3. 비디오 이해 — 시공간 추론

#### VIRST (CVPR 2026) ⭐8
- 자연어 지시 기반 비디오 시공간 세분화
- 핵심 구조: VLM 백본 + TDAU + ST-Fusion + Seg-aware Encoder + Mask Decoder
- 지원: Ref-DAVIS, Ref-YouTube-VOS, MeViS, ReVOS, LVVIS

---

### 분야 4. LLM 신뢰성·평가·가치 정렬

#### RFEval (ICLR 2026) ⭐5
- 추론 충실성(Reasoning Faithfulness) 평가 프레임워크
- 반사실적 개입으로 CoT와 최종 답변의 일치성 검증
- 7개 도메인: 코드/문맥/법률/논리/수학/논문/표

#### Awesome-LLM-Values-and-Pluralistic-Alignment ⭐2
- 200+ 논문 수록 LLM 가치 정렬 자료집
- 서베이 / 데이터셋·벤치마크 / 인간 가치 / 다원적 정렬

---

### 분야 5. 수학·음성 멀티모달 처리

#### MathSpeech (AAAI 2025) ⭐13
- 음성 수학 설명 → LaTeX 변환 파이프라인
- 120M 파라미터로 GPT-4o 초과 (CER: 0.390→0.298)
- 데이터: MIT OCW 강의 1,101개 파일

#### MathReader (ICASSP 2025 Oral) ⭐31
- PDF 수학 문서 → 음성 변환 (Nougat OCR + NVIDIA NeMo TTS)
- 데모: https://hyeonsieun.github.io/MathReader_demo/

---

### 분야 6. 표 데이터 추론(TableQA)

#### MATA (ACL 2026) ⭐5
- 다중 에이전트 TableQA 프레임워크
- MobileBERT 스케줄러로 LLM 호출 최소화
- Ollama 로컬 실행 지원 (프라이버시 환경 적합)

---

### 분야 7. 로봇 학습 및 물리적 AI

#### lerobot-so101-bimanual ⭐8
- LeRobot SO-101 양팔 조작 지원
- 텔레조작, 데이터셋 레코딩, HuggingFace 자동 업로드

#### Awesome-VLA-Data-Collection-Synthesis-Curation ⭐5
- VLA 데이터 엔진 100+ 논문 자료집
- 강화학습/모방학습/합성데이터/세계모델/cross-embodiment

---

### 분야 8. 모델 편집 및 분류기 제어

#### Class-Vector (NeurIPS 2025) ⭐1
- 클래스 벡터 조작으로 재학습 없이 분류기 편집
- 응용: 편향 교정, 성능 개선, 개인화

---

### 분야 9. 추론 효율화 인프라

#### vllm-omni ⭐1 / 🍴1.1k
- vLLM의 오니모달 확장 (비AR, DiT, 음성/이미지 생성 지원)
- OmniConnector 추상화 계층으로 완전 분해 서빙
- 지원 플랫폼: CUDA, ROCm, NPU, XPU
- 최신 버전: v0.16.0 (2026/02)

---

## 3. 저장소 전체 목록 요약

| 저장소 | 학회/분류 | 기술 분야 | Stars |
|--------|----------|----------|-------|
| VALUEFLOW | ICML 2026 | LLM 가치 정렬 | 0 |
| MI-CXR | ACL 2026 | 의료 영상 벤치마크 | 3 |
| Awesome-Diffusion-LLM | 자료집 | 확산 LLM 논문 모음 | 80 |
| Awesome-VLA-Data | 자료집 | 로봇 VLA 데이터 | 5 |
| VIRST | CVPR 2026 | 비디오 시공간 세분화 | 8 |
| Awesome-LLM-Values | 자료집 | LLM 가치 정렬 논문 | 2 |
| MathReader | ICASSP 2025 Oral | 수학 문서 TTS | 31 |
| MathSpeech | AAAI 2025 | 수학 음성→LaTeX | 13 |
| MATA | ACL 2026 | 테이블 QA 멀티에이전트 | 5 |
| Dynin-Omni | arXiv 2026 | 오니모달 확산 LLM | 45 |
| Medic-AD | CVPR 2026 Oral | 의료 VLM 임상 지능 | 18 |
| vllm-omni | 인프라 | 오니모달 추론 서빙 | 1 |
| Dynin | 웹 | 프로젝트 페이지 | 0 |
| RFEval | ICLR 2026 | 추론 충실성 평가 | 5 |
| arpa_temp | 연구 | 뇌 연령 예측·분류 | 0 |
| lerobot-so101-bimanual | 로봇 | 양팔 조작 지원 | 8 |
| Class-Vector | NeurIPS 2025 | 분류기 편집 | 1 |
| MMPB | NeurIPS 2025 | 멀티모달 개인화 벤치마크 | 9 |
| TTA-Diffusion | NeurIPS 2025 | 확산 LLM 편집 보존 | 2 |
| SECOND | ICML 2025 | VLM 환각 완화 | 7 |
| aidas-homepage | 웹 | 홈페이지 | 0 |
| aidas-project-page-template | 웹 | 프로젝트 페이지 템플릿 | 0 |
| .github | 설정 | 조직 프로필 | 0 |

---

## 4. 연구 간 시너지 맵

```
[마스킹 확산 기반 생성]
 TTA-Diffusion ──── Dynin-Omni ──── vllm-omni
      │                 │               │
편집 보존 기술      오니모달 통합    추론 인프라
                        │
          ┌─────────────┼─────────────┐
      이미지/비디오  음성(TTS/ASR)  텍스트 생성

 [비전-언어 모델]         [음성-수학 처리]
  SECOND                  MathSpeech
  MEDIC-AD                MathReader
  MMPB
  VIRST                [표 데이터 추론]
  MI-CXR                   MATA

 [신뢰성·정렬]           [로봇 물리 AI]
  RFEval + VALUEFLOW      lerobot-so101 + Awesome-VLA
  Awesome-LLM-Values
```

---

## 5. 종합 강점·약점·시사점 분석

### 강점

- 확산 언어 모델 중심으로 의료·로봇·음성·수학 등 다양한 도메인 수직 통합
- 최상위 학회 집중 게재 (CVPR 2026 Oral, ICML, NeurIPS, ICLR, AAAI, ACL)
- 오픈소스(MIT, Apache 2.0) + 산업 협력(NVIDIA, 삼성) 동시 추진
- vllm-omni 1.1k 포크로 실질적인 산업 활용도 입증

### 약점

- 여러 저장소 "코드 공개 예정" 상태 → 재현 가능성 미완
- 멤버 수 대비 넓은 연구 범위 → 깊이보다 폭 우선 경향
- 일부 저장소 문서화 수준 낮음 → 외부 연구자 진입 장벽

### 미래 방향

Dynin-Omni + vllm-omni 생성 인프라 + MEDIC-AD + MI-CXR 의료 기술 + RFEval + VALUEFLOW 신뢰성 연구의 통합으로 **임상적으로 신뢰할 수 있는 멀티모달 의료 AI** 시스템으로 수렴 예상

---

## 6. FAQ

**Q1. AIDAS Lab의 가장 핵심 기술은 무엇인가요?**

확산 언어 모델(Diffusion LLM) 기술이 핵심입니다. Dynin-Omni가 대표 기술로, 마스킹 노이즈 제거 방식으로 텍스트·이미지·음성·비디오를 단일 아키텍처에서 처리합니다. TTA-Diffusion(편집 보존), vllm-omni(서빙 인프라)와 함께 수직 통합된 생태계를 구성합니다.

---

**Q2. 의료 AI 분야에서 어떤 기술을 보유하고 있나요?**

MEDIC-AD(CVPR 2026 Oral): 이상 탐지→차이 추론→시각적 설명 임상 VLM, MI-CXR(ACL 2026): 흉부 X선 종단면 추론 벤치마크, arpa_temp: ARPA-H 프로그램 뇌 연령 예측·분류. NVIDIA, 삼성 의료센터와 협력 관계 구축.

---

**Q3. 이 랩의 VLM들은 환각(Hallucination) 문제를 어떻게 해결하나요?**

SECOND(ICML 2025): 선택적 대조 디코딩으로 생성 단계에서 시각적 근거 없는 토큰 확률 실시간 억제. RFEval(ICLR 2026): 추론 충실성 사후 평가로 논리 기반 답변 여부 검증.

---

**Q4. Dynin-Omni와 GPT-4o, Gemini와의 차이는 무엇인가요?**

GPT-4o/Gemini는 텍스트를 자기회귀적으로 생성하면서 이미지·음성을 별도 인코더로 처리합니다. Dynin-Omni는 모든 모달리티를 동일한 이산 토큰으로 변환해 단일 마스킹 확산 백본으로 처리합니다. 양방향 문맥 모델링과 병렬 다중 토큰 생성이 핵심 차별점입니다.

---

**Q5. vllm-omni는 단순한 포크인가요, 독자적인 기여가 있나요?**

독자적인 핵심 기여가 있습니다. DiT 같은 비AR 모델·음성/이미지 생성 파이프라인을 추가 지원하고, OmniConnector 추상화 계층으로 완전 분해 서빙과 동적 자원 배분을 구현했습니다. 1.1k 포크는 산업 활용을 증명합니다.

---

**Q6. 수학 관련 기술(MathSpeech, MathReader)은 서로 어떻게 다른가요?**

MathSpeech(AAAI 2025): 음성 수학 설명 → LaTeX 변환 (음성 입력). MathReader(ICASSP 2025 Oral): PDF 수학 문서 → 음성 변환 (문서 입력). 두 기술은 수학 콘텐츠 음성 접근성 생태계를 양방향으로 구성합니다.

---

**Q7. MATA는 어떻게 기존 TableQA보다 효율적인가요?**

MobileBERT 기반 경량 스케줄러가 유효한 추론 경로를 사전 예측해 불필요한 LLM 호출을 차단합니다. 소규모 모델(qwen2.5:0.5b)로 형식 검사·신뢰도 측정 도구를 구성하고, Ollama 로컬 실행으로 프라이버시 환경도 지원합니다.

---

**Q8. 로봇 연구는 다른 AI 연구와 어떻게 연결되나요?**

lerobot-so101-bimanual이 물리적 데이터 수집 인프라를 제공하고, Awesome-VLA가 학습 파이프라인 지식 기반을 제공합니다. Dynin-Omni의 비디오-언어 이해와 VIRST의 시공간 세분화가 로봇 시각 인식 모듈로 통합될 잠재적 연결성을 가집니다.

---

**Q9. AI 안전성·정렬 연구에서 AIDAS Lab의 입장은 어떤가요?**

기술적 신뢰성과 가치 다원주의를 동시에 추구합니다. RFEval(평가), VALUEFLOW(구현), Awesome-LLM-Values(지식)가 AI 안전성의 평가·구현·지식 세 층위를 각각 담당합니다.

---

**Q10. AIDAS Lab의 코드를 실제로 사용하려면 어디서 시작하는 것이 좋나요?**

| 목적 | 추천 시작점 |
|------|-----------|
| 의료 AI 연구 | MEDIC-AD (HuggingFace: wooohyeooon/MEDIC-AD) |
| 멀티모달 생성 AI | Dynin-Omni scripts/inference.sh 또는 vllm-omni |
| 벤치마크 연구 | RFEval (HuggingFace: snu-aidas/RFEval) |
| 로봇 학습 | lerobot-so101-bimanual |
| 확산 LLM 공부 | Awesome-Diffusion-LLM |

---

*본 문서는 AIDAS Lab GitHub(https://github.com/AIDASLab) 저장소를 기반으로 작성되었습니다.*
