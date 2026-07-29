<!-- Header -->
<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:233CC4,100:5B7CFA&height=200&section=header&text=LEE%20JONGBEEN&fontSize=54&fontColor=ffffff&animation=fadeIn&desc=Backend%20Developer%20%7C%20Java%20%C2%B7%20Spring%20Boot%20%C2%B7%20JPA&descAlignY=68&descSize=18" />
</div>

<div align="center">

**화면 뒤에서 데이터가 흐르는 길을 설계하는 신입 백엔드 개발자입니다.**

[![Gmail](https://img.shields.io/badge/jongbeen97@naver.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:jongbeen97@naver.com)
[![Notion](https://img.shields.io/badge/Notion-000000?style=flat-square&logo=notion&logoColor=white)](https://www.notion.so/GIT-GITHUB-2e89f435b1ac80c18184cb20139dbad9?source=copy_link)
![Location](https://img.shields.io/badge/Seoul,%20KR-4B5768?style=flat-square)

</div>

---

## 👋 About

비전공(식품영양학과)에서 시작해 사무·영업지원 경력을 거쳐 개발자로 전향했습니다.
세 번의 팀 프로젝트를 하면서 제가 가장 오래 붙잡고 있던 건 **화면이 아니라 그 뒤의 로직**이었고,
지금은 백엔드 개발자로 방향을 확실히 잡았습니다.

- 🎯 **관심 영역** — REST API 설계, 인증/인가(JWT), 데이터 모델링, 배포 자동화
- 🌱 **현재 학습 중** — AWS · MSA · Docker (2026.05 ~ 2026.11 과정 수강 중)
- 🧩 **강점** — 막힌 지점의 원인을 서버/클라이언트로 범위를 좁혀 끝까지 찾아냅니다
- 🗣 **협업** — 1차 프로젝트에서 팀 대표로 발표와 포트폴리오 제작을 맡았습니다

---

## 🎓 Education & Training

| 기간 | 내용 |
|---|---|
| 2026.05 ~ 2026.11 | **AWS와 AI를 활용한 MSA 기반 웹 서비스 개발** *(수강 중)* |
| 2025.11 ~ 2026.05 | **한국정보교육원 · 자바 풀스택 & 생성형 AI 서비스 개발** 수료 (6개월) |
| 2017.03 ~ 2024.02 | 안양대학교 식품영양학과 수료 |
| 2013.03 ~ 2016.02 | 대일고등학교 졸업 |

<details>
<summary>💼 개발 이전 경력 (총 1년 11개월)</summary>

| 기간 | 회사 / 직무 |
|---|---|
| 2024.10 ~ 2025.01 | 한국일본통운(Nippon Express Korea) · 경리부 사무지원 |
| 2024.08 ~ 2024.09 | 엑소코바이오 · 국내영업 영업지원 |

</details>

---

## 📌 Projects

### 03. Basecamp — 캠핑장 예약 · 커뮤니티 플랫폼
> `2026.07` · 팀 4명 · **Backend 담당**

게시글 · 댓글 · 신고 도메인의 **API 12종**을 설계하고 구현했습니다.

- **커서 기반 페이징** — 목록 조회 중 글이 추가돼도 중복·누락이 없도록 서버가 불투명 커서를 발급
- **소프트 삭제 설계** — 본인 삭제(`DELETED`)와 관리자 처리(`BLINDED`)를 분리해 신고 이력 보존
- **신고 API 보안** — 신고자 식별은 요청 본문이 아닌 JWT 인증 주체(`@AuthenticationPrincipal`)만 신뢰
- **공통 에러 코드 체계** — 중복 신고 409, 블라인드 글 403 등 팀 규격 통일
- 개발 착수 전 **API 명세서를 먼저 확정**해 프론트엔드가 Mock 데이터로 병행 개발 가능하도록 함

```
Java 21 · Spring Boot 3 · Spring Security(JWT) · Spring Data JPA · MySQL 8
Redis · Docker · GitHub Actions · React 19 · TypeScript
```

<br>

### 02. PLEEGIE — LLM/RAG 기반 식재료 관리 · 전통시장 연계 플랫폼
> `2026.04 ~ 2026.05` · 팀 4명 · **Frontend & API 연동 담당** · [Repo](https://github.com/jongbeen97/pleegie)

Spring Boot(8080)와 Python FastAPI(8000), 두 개의 서버와 통신하는 React 클라이언트를 담당했습니다.

- React 라우팅 구조와 공통 컴포넌트를 설계해 팀원들이 화면을 병렬로 개발할 수 있게 함
- 냉장고 재료 관리 화면 — 서버 스케줄러가 매일 자정 갱신하는 유통기한 상태(`FRESH` / `NEAR_EXPIRY` / `EXPIRED`) 시각화
- 레시피 추천 화면 — 공공데이터 레시피와 LLM 생성 레시피를 구분해 표시, Redis 캐싱된 응답 연동
- OAuth 소셜 로그인 3종 콜백 및 JWT 저장 흐름 처리
- **얻은 것** — 포트 분기·프록시 설정을 직접 다루며 "요청이 어디로 가는지" 추적하는 습관. 이 경험이 백엔드로 전향한 계기가 됐습니다.

```
React · JavaScript / Spring Boot · JPA · QueryDSL · MySQL · Redis
FastAPI · LangChain · Groq · ChromaDB(RAG) · Kakao Map API · Docker · AWS EC2 · Nginx
```

<br>

### 01. 대동여집도 — 1인 가구를 위한 거주지 후기 · 커뮤니티
> `2026.02 ~ 2026.03` · 팀 5명 · **Backend(커뮤니티 · 관리자) 담당** · [Repo](https://github.com/jongbeen97/zipmap)

- Spring Framework + MyBatis로 **게시판 CRUD 및 관리자 신고 처리** 구현
- **jQuery AJAX 무한 스크롤** — 전체 새로고침 대신 필요한 데이터만 JSON으로 받아 렌더링
- **Gemini API 연동 AI 요약** — 사람이 직접 정리하던 게시글 요약을 비동기 호출로 자동화
- 팀 대표로 최종 발표 및 포트폴리오 제작 담당

> 🔧 **Trouble Shooting** — 무한 스크롤이 로딩만 반복되는 현상 발생.
> 크롬 개발자도구 Network 탭에서 서버 응답은 정상임을 확인해 원인을 클라이언트로 좁혔고,
> merge 과정에서 **응답 필드명과 JS 참조 키가 불일치**한 것이 원인이었습니다.
> 이후 팀에서 큰 기능은 클래스 다이어그램·ERD를 먼저 맞추고 착수하도록 프로세스를 바꿨습니다.

```
Java 17 · Spring Framework · MyBatis · MySQL · Redis · Spring Security
OAuth2 · WebSocket · Thymeleaf · Bootstrap · jQuery/AJAX · Gemini API
```

---

## 🛠 Tech Stack

**Backend**

![Java](https://img.shields.io/badge/Java%2017%20%7C%2021-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)
![SpringBoot](https://img.shields.io/badge/Spring%20Boot%203-6DB33F?style=for-the-badge&logo=springboot&logoColor=white)
![Spring](https://img.shields.io/badge/Spring%20Framework-6DB33F?style=for-the-badge&logo=spring&logoColor=white)
![Security](https://img.shields.io/badge/Spring%20Security%20%2B%20JWT-6DB33F?style=for-the-badge&logo=springsecurity&logoColor=white)
![JPA](https://img.shields.io/badge/Spring%20Data%20JPA-59666C?style=for-the-badge&logo=hibernate&logoColor=white)
![MyBatis](https://img.shields.io/badge/MyBatis-000000?style=for-the-badge)
![REST](https://img.shields.io/badge/REST%20API-02569B?style=for-the-badge)

**Database**

![MySQL](https://img.shields.io/badge/MySQL%208-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![QueryDSL](https://img.shields.io/badge/QueryDSL-0A66C2?style=for-the-badge)

**Infra & Tools**

![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHubActions](https://img.shields.io/badge/GitHub%20Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS%20EC2%20%C2%B7%20RDS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-009639?style=for-the-badge&logo=nginx&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)

**Frontend**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=black)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)

**AI 연동**

![LLM](https://img.shields.io/badge/LLM%20API%20(Gemini%20%C2%B7%20Groq)-412991?style=for-the-badge)
![RAG](https://img.shields.io/badge/RAG%20%C2%B7%20Vector%20Search-0A66C2?style=for-the-badge)

---

## 📊 GitHub Stats

<div align="center">
  <img height="165" src="https://github-readme-stats.vercel.app/api?username=jongbeen97&show_icons=true&theme=graywhite&hide_border=true&include_all_commits=true" />
  <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=jongbeen97&layout=compact&theme=graywhite&hide_border=true" />
</div>

---

## 📫 Contact

| | |
|---|---|
| 📧 Email | jongbeen97@naver.com |
| 📱 Phone | 010-9120-6601 |
| 📍 Location | 서울 구로구 |
| 📝 Notion | [기술 정리 노트](https://www.notion.so/GIT-GITHUB-2e89f435b1ac80c18184cb20139dbad9?source=copy_link) |

<div align="center">
  <br>
  <sub>신입이라 모르는 게 많습니다. 대신 모르는 걸 찾아내고 물어보는 일은 빠릅니다.</sub>
</div>
