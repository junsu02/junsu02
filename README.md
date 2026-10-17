# 안녕하세요, 김준수입니다 👋

**문제를 정의하고, 직접 만들고, 숫자로 검증하는 백엔드 개발자**를 지향합니다.
단국대학교 컴퓨터공학과 · 2028년 2월 졸업 예정

- 팀에서는 주로 **PM/팀장 + 백엔드**를 맡아 기획부터 배포까지 끌고 갑니다.
- 기능 구현에서 끝내지 않고 **부하 테스트와 모니터링**으로 한계를 확인합니다.
- 해군 전자전 임무 경험을 바탕으로 **임베디드 신호 처리**까지 다뤄 봤습니다.

<br>

## 🛠 Tech Stack

**Backend**

![Java](https://img.shields.io/badge/Java-007396?style=flat-square&logo=openjdk&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?style=flat-square&logo=springboot&logoColor=white)
![Spring Security](https://img.shields.io/badge/Spring%20Security-6DB33F?style=flat-square&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/Spring%20Data%20JPA-6DB33F?style=flat-square&logo=spring&logoColor=white)

**Data**

![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=mysql&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-FF4438?style=flat-square&logo=redis&logoColor=white)

**Infra / Observability**

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white)
![k6](https://img.shields.io/badge/k6-7D64FF?style=flat-square&logo=k6&logoColor=white)

**Embedded**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white)
![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi-A22846?style=flat-square&logo=raspberrypi&logoColor=white)
![Arduino](https://img.shields.io/badge/Arduino-00878F?style=flat-square&logo=arduino&logoColor=white)

<br>

## 🏆 Awards

- **2026 멋쟁이사자처럼 대학 해커톤 — 패션&럭셔리 부문 트랙상** (MCMoments, 팀장)

<br>

## 📌 Projects

### 📋 [part너](https://github.com/naverhood-DKU/student-council) — 학생회 회의 결정·업무 추적 서비스
`2026.10.09 ~ 2026.10.16` · Backend / 기반 서비스 설계 · 5인 팀 · [라이브 사이트](https://council.naverhood.cloud)

회의 녹음을 CLOVA Speech로 전사하고 CLOVA Studio(HCX-007)가 결정·업무 후보를 뽑으면, 회장이 승인한 업무를 부서와 다른 학생회로 전달해 끝날 때까지 추적하는 서비스 (NCP 배포)

- 회의 → 결정 → 업무 → 그룹 간 요청으로 이어지는 기반 서비스 설계·구현(첫 커밋 169개 파일). AI는 후보만 내고 사람이 승인해야 확정되도록 상태 전이를 한곳에 모으고, AI 결과의 근거 발언 ID를 서버가 검증
- 브라우저가 presigned URL로 비공개 NCP Object Storage에 직접 올리고 CLOVA Speech로 전사 (2분 27초 녹음 → 9.5초, 15문장)
- 회의에서 담당을 말하지 않은 업무는 AI가 등록된 부서 중에서 고르고 이유를 남겨 "AI 지정"으로 표시, 회장이 승인 전에 확인
- 분석 작업을 DB 큐(`SKIP LOCKED` + 임대)로 웹 서버와 Worker로 분리, 테스트 264개 (Testcontainers MySQL, 외부 API는 가짜 서버)

`Java 21` `Spring Boot 4` `Spring Security` `JPA` `MySQL` `React` `TypeScript` `CLOVA Speech` `CLOVA Studio` `NCP`

---

### 🎨 [MCMoments](https://github.com/chae-ring/2026_LIKELION_HACKATHON) — MCM 전용 AI 아트워크 디지털 보증서
`2026.08.09 ~ 2026.08.19` · 팀장 / PM / Backend · **트랙상 수상**

첫 MCM 구매의 사연을 감정 분석하고, Visetos 패턴이 반영된 AI 아트워크 보증서로 남기는 서비스

- 【내가 만든 것 1 — 예: 시리얼 검증 → 사연 등록 → 아트워크 생성 API 설계·구현】
- 【내가 만든 것 2 — 예: 아트워크 생성 상태(PENDING/COMPLETED/FAILED) 관리와 실패 시 재시도·대체 처리】
- 【팀장으로서 한 것 — 예: 11일 일정 관리, MVP 범위 결정】

`Java` `Spring Boot` `Spring Security` `React` `TypeScript`

---

### 🚑 [SuperSave](https://github.com/Programming-G1/supersave) — 응급실 뺑뺑이 방지 서비스
· PM / Backend

공공데이터의 실시간 병상 정보를 기반으로 응급실을 추천하고, AI 응급 가이드를 제공하는 서비스

- 【내가 만든 것 1 — 예: 공공데이터 응급실 API 연동과 Redis 캐시 적용】
- 【내가 만든 것 2 — 예: 거리·병상·중증도·대기시간 기반 추천 점수 로직】
- 【PM으로서 한 것 — 예: 요구사항 정의, API 명세, 역할 분담】

`Java` `Spring Boot` `PostgreSQL` `Redis` `Gemini API` `Kakao Map` `React`

---

### 🎓 [수강신청 연습 사이트](https://github.com/lab412sugang2/sugang) — 단국대 수강신청 화면 재현
· Backend · [라이브 사이트](https://sugang-5de3.onrender.com)

수강신청 흐름을 그대로 연습할 수 있는 사이트. 신청 규칙 검증부터 부하 테스트까지 진행

- 학점 초과 · 시간표 충돌 · 정원 초과 · 중복 신청 방지 로직 

`Java` `Spring Boot 3` `JPA` `MySQL` `Docker`

---

### 📡 [Anti-Drone Radar](https://github.com/junsu02/anti-drone-radar) — 드론 탐지 헬멧 임베디드 시스템
· 

드론 통신 주파수 대역을 실시간 스캔해 위협 전파를 탐지하고 LED·부저로 경고하는 시스템

- 슬라이딩 윈도우 큐(`deque`)로 최근 1초 신호만 유지해 메모리 사용을 제한
- 광대역 에너지 통합과 단계별 임계값으로 오탐지 감소

`C++ (Arduino)` `Python (Raspberry Pi)`

<br>

## 📫 Contact

- Email: junsu020139@gmail.com
- phone: 010-7224-0580

