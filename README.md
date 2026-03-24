# 🐣 코딩 병아리 스터디 트래커

> 매일 공부하면 캐릭터가 진화하는 다마고치 스타일 스터디 출석 체크 앱

![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-배포가능-86efac?style=flat-square)
![HTML](https://img.shields.io/badge/HTML-단일파일-c084fc?style=flat-square)
![저장소](https://img.shields.io/badge/저장소-localStorage-f9a8d4?style=flat-square)

---

## ✨ 주요 기능

- **15일 스터디 챌린지** — 시작일부터 15일간 매일 출석 체크
- **다마고치 진화 시스템** — 공부 횟수에 따라 캐릭터가 성장
- **멤버 추가 / 삭제** — 스터디 인원 자유롭게 관리
- **자유로운 날짜 체크** — 과거·미래 날짜 모두 체크/해제 가능
- **실시간 달성률** — 멤버별 진행 상황 한눈에 확인
- **로컬 저장** — 브라우저를 닫아도 데이터 유지 (localStorage)

---

## 🥚 진화 시스템

스터디 체크 횟수에 따라 캐릭터가 3단계로 진화해요.

| 단계 | 조건 | 캐릭터 | 설명 |
|:---:|:---:|:---:|---|
| 🥚 알 | 0 ~ 4회 | 달걀 | 공부를 시작하면 눈이 빼꼼 |
| 🐣 병아리 | 5 ~ 10회 | 코딩 병아리 | 헤드폰 쓰고 노트북 앞에 앉은 병아리 |
| 🐔 닭 | 11 ~ 15회 | 시니어 닭 | 개발자 안경·플란넬 셔츠 입은 풀스택 닭 |

진화 순간 카드가 튀어오르는 **레벨업 연출**이 재생돼요.

---

## 🕹️ 사용 방법

### 1. 멤버 추가

```
이름 입력창에 멤버 이름 입력 → Enter 또는 [+ 추가] 버튼
```

- 최대 12자까지 입력 가능
- 같은 이름은 중복 추가 불가

### 2. 출석 체크

카드 하단의 **동그란 도트**를 클릭하면 체크/해제 토글.

- ✅ 초록 도트 = 출석 완료
- ⬜ 빈 도트 = 미체크
- 오늘 날짜는 **보라색 테두리**로 표시
- 과거·미래 날짜 모두 자유롭게 체크 가능

하단 **전체 체크 현황 표**에서도 동일하게 체크할 수 있어요.

### 3. 멤버 삭제

카드 우하단 **[삭제]** 버튼 → 확인 모달에서 삭제.

> ⚠️ 삭제하면 해당 멤버의 모든 체크 기록도 함께 사라져요.

### 4. 기간 설정

| 버튼 | 기능 |
|---|---|
| 📅 시작일 변경 | 15일 챌린지 시작일 변경 (기존 기록 유지) |
| 🔄 초기화 | 오늘부터 새 15일 시작 (체크 기록 초기화, 멤버는 유지) |

---

## 💾 데이터 저장 방식

이 앱은 **브라우저의 localStorage**를 사용해요.

- 같은 브라우저에서는 창을 닫아도 데이터가 유지돼요
- 멤버마다 **자신의 브라우저에 저장**되므로, 팀원들이 각자 접속하면 각자의 데이터가 따로 저장돼요
- 다른 기기나 다른 브라우저에서는 데이터가 공유되지 않아요

> 팀 전체가 같은 데이터를 보려면 Firebase 등 백엔드 연동이 필요해요.

---

## 🚀 GitHub Pages 배포 방법

### 웹에서 직접 올리기 (간단)

1. [github.com](https://github.com) 로그인
2. 우상단 `+` → **New repository**
3. 저장소 이름 입력 (예: `study-tamagotchi`) → **Public** → **Create**
4. **Add file → Upload files** 클릭
5. `index.html`로 이름 바꾼 파일 업로드 → **Commit changes**
6. **Settings → Pages → Branch: main / root → Save**
7. 잠시 후 아래 주소로 접속 가능:

```
https://[내아이디].github.io/study-tamagotchi/
```

### 터미널로 올리기

```bash
# 파일 이름을 index.html로 변경 후
git init
git add index.html README.md
git commit -m "🐣 코딩 병아리 스터디 트래커 첫 커밋"
git remote add origin https://github.com/[아이디]/study-tamagotchi.git
git push -u origin main
```

---

## 🗂️ 파일 구조

```
study-tamagotchi/
├── index.html   # 앱 전체 (HTML + CSS + JS 단일 파일)
└── README.md    # 이 파일
```

외부 라이브러리 없이 **순수 HTML/CSS/JS**로 작성됐어요.  
인터넷 연결 시 Google Fonts(Jua, Space Mono)를 불러와요.

---

## 🛠️ 기술 스택

| 항목 | 내용 |
|---|---|
| 언어 | HTML5 · CSS3 · Vanilla JS |
| 폰트 | Jua, Space Mono (Google Fonts) |
| 저장소 | localStorage |
| 캐릭터 | SVG (인라인 직접 작성) |
| 애니메이션 | CSS @keyframes |
| 외부 의존성 | 없음 |

---

## 📋 업데이트 기록

- 캐릭터 SVG 직접 제작 (알 / 병아리 / 닭)
- 플란넬 체크무늬 셔츠 + 둥근 안경 개발자 패션 적용
- 팔·소매 통합 애니메이션 (어깨 기준 퍼덕이기)
- 눈 깜빡임 · 커서 깜빡임 · 그림자 펄스 모션
- 과거·미래 날짜 자유 체크/해제

---

<div align="center">

열심히 공부해서 병아리를 닭으로 키워보세요 🐔

</div>
