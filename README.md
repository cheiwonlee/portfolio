# 이채원 (Lee Chaewon) · 금융 백엔드 지향 개발자

> **거래의 흐름을 설계하고, 데이터의 정합성을 지키는 개발자.**
> 기획한 요구사항을 데이터 구조로 설계하고 API로 사용자 경험까지 구현해 왔습니다.
> 프론트엔드 경험을 토대로, 거래 처리와 데이터 정합성을 다루는 금융 백엔드 개발자를 지향합니다.

- 🌐 **포트폴리오** — https://portfolio-psi-ashen-57.vercel.app/
- 📧 **Email** — cheiwonlee.dev@gmail.com
- 💻 **GitHub** — https://github.com/cheiwonlee
- ✍️ **Tech Blog** — https://lxvxxu.tistory.com (Behind the Screen)

---

## 기술 스택

| 분류 | 기술 | 사용 프로젝트 |
| --- | --- | --- |
| **Backend** | Java, Spring Boot, JDBC, REST API | WON-pick 거래 서버 · WON ATTACK |
| **Database** | MySQL, SQL, 데이터 모델링 | 금융거래 차단 DB · 거래 서버 |
| **Frontend** | React, TypeScript, JavaScript | TicketRush · cseetv · 웹 서비스 |
| **Data & AI** | Python, pandas, FastAPI, ChromaDB·RAG | 코로나 분석 · WON ATTACK · cseetv |
| **Tools** | Git/GitHub, Docker, Figma | 전 프로젝트 협업·배포 |

그 외: Unity · C#, Django, React Native

---

## 대표 프로젝트

### 1. WON-pick — 거래(Trade) 서버 · `Backend`

우리WON 아카데미 수강생·강사 약 70명을 대상으로 한 중고거래 서비스의 **거래 서버를 단독 담당**했습니다.

- 예약 생성 → 결제 요청 → 모의 결제 → 구매 확정 → 취소·환불로 이어지는 **거래 상태머신** 구현
- 거래번호 기반 **멱등 키**로 재시도 안전성 확보
- Market·Chat·Payment 서버와 분산 환경에서 연동
- **지표**: 거래 상태 5단계 · 대상 사용자 70명 · Trade 서버 1인 단독 설계·구현
- **스택**: Spring Boot 4 · Java 17 · Spring MVC · JDBC · MySQL · Docker
- GitHub: https://github.com/won-pick/trade-service

### 2. 사망자 명의 금융거래 신속차단 DB · `Database`

금융위원회가 2026년 9월 시행한 「사망자 명의 금융거래 신속차단」 제도를 은행의 계정계·대외계·채널계·정보계 관점으로 모델링한 금융 데이터베이스입니다. (실제 금융기관 시스템이 아닌, 공개 제도 기반 **학습 프로젝트**)

- 2인 팀에서 **DB 설계·구현·검증·문서를 전담** (팀원: 법령 조사)
- 3NF 정규화와 이력 관리(SCD Type 2) 기준으로 설계, 순수 JDBC로 로직 구현
- **지표**: 30 테이블(업무 요구사항 구조화) · 68 FK(참조 무결성) · 42 CHECK · 14개 업무 시나리오 검증
- **스택**: MySQL 8.0 · Java (JDBC)
- GitHub: https://github.com/Doo-Lee01/deceased-account-block-db
- 개발 기록: https://lxvxxu.tistory.com/210

### 3. TicketRush — 콘서트 예매 · `Full Service` (졸업 프로젝트)

대규모 트래픽과 좌석 중복 예매를 고려한 콘서트 티켓 예매 서비스. **프론트엔드를 담당**했습니다.

- 좌석 선택 UI, Socket.io 기반 **실시간 좌석 동기화**, QR 티켓, 관리자 판매 대시보드(Recharts), 결제·인증 연동 화면
- 좌석 상태와 서버 응답의 동기화, 비동기 데이터와 클라이언트 상태 분리를 경험 (결제·동시성 제어는 백엔드 담당 영역)
- **지표**: 359 커밋 · 약 1년 지속 개발
- **스택**: React 18 · TypeScript · Zustand · TanStack Query · Socket.io · Recharts
- 데모(목업): https://ticketrush-frontend-demo.vercel.app/
- GitHub: https://github.com/TicketRush/TicketRush-frontend

### 4. cseetv — 야간 CCTV 이상행동 감지 · `영상처리`

야간 CCTV 영상에서 이상 움직임을 감지해 알림을 주는 웹 서비스. 2인 팀장으로 **영상처리 서버와 프론트엔드를 모두 담당**했습니다.

- AI 모델 대신 전통 영상처리 기법을 택해 CDnet(tramStation)으로 비교 벤치마크 수행
- **지표**: AI 기준선(MOG2) 대비 92.1% 성능 · 벤치마크 2,501 프레임
- **스택**: React · TypeScript · Python · FastAPI · OpenCV · WebSocket
- 홈페이지: https://cseetv-fe.vercel.app/
- GitHub: https://github.com/cseetv/cseetv_ip

---

## 그 외 프로젝트

- **cardfit** — 연말정산 카드 소득공제 계산기 (React·TS, 1인, 급여·소비 금액 서버 미전송) · https://cardfit-two.vercel.app/
- **WON ATTACK** — 투자정보 검증 AI (해커톤). 공시 근거 데이터·ChromaDB 벡터 DB·RAG 실행 환경 담당 · Python·ChromaDB·RAG
- **코로나19가 고교 생활·대학 입시에 미친 영향 분석** — 비식별 성적 데이터 69건을 통계 검정(Welch t-test, Brown-Forsythe, Hedges' g, OLS)
- **curit** — 사이트 큐레이션 서비스 (React·TS·Supabase·PWA) · https://www.cur-it.duckdns.org/
- **WhereLive(어디살지)** — 주거 선택 지원 웹 서비스, 전국 250개 지역 (React·TS·Kakao Maps)
- **ClearPlate** — 식단 영양소 분석 PWA · https://clear-plate.vercel.app/
- **공강이세요?** — 빈 강의실 안내 앱, Google Play 출시 (Unity·C#)
- **캠퍼스 메타버스** — 팀 결과물을 혼자 재구축해 학교 공식 자산으로 인계 (ZEP)
- **감정 기반 향수 제조기** — IoT 기기 + 웹 대시보드 (Django·STM32) · https://emotion-perfume-maker.vercel.app/

---

## 경험

- **2026.08 – 2026.12 · 우리WON 청년 IT 아카데미** — 금융 데이터베이스 설계, Java/Spring 기반 서버 개발, 금융 AI 해커톤 등 팀 프로젝트
- **QA 인턴 · 라온시큐어 (6개월)** — 재현되지 않는 버그의 재현 조건을 좁혀 원인을 추적. 작은 오류 하나가 사용자 신뢰에 미치는 영향을 경험
- **수상·활동** — SM Learning Fair 최우수상 · 상명엑스퍼트공모전 최우수상 · 비교과 마일리지 전 학년 통합 1위 · 면학장학금 · 개발 동아리 알고리즘 스터디 운영

## 학력

- 상명대학교 컴퓨터과학전공 (2027년 8월 졸업 예정)

---

<p align="center"><sub>© 2026 이채원 (Lee Chaewon) · 금융 IT 개발자</sub></p>
