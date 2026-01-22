# ARTREW 아키텍처 종합 리포트

> **AI-Native Artist의 디지털 월드**
> 최종 업데이트: 2026-01-22

---

## 1. 프로젝트 개요

### 1.1 정체성

| 항목 | 값 |
|------|-----|
| **브랜드명** | ARTREW |
| **바이라인** | by Sooha Ryu |
| **태그라인** | Not Human. Not Machine. Art. |
| **직함** | AI-Native Artist |
| **설립일** | 2026.01.16 |
| **테마 컬러** | #D4AF37 (Gold) |

### 1.2 철학

```
"Not Human. Not Machine. Art."

AI와 인간의 경계에서,
도구도 아니고 창작자도 아닌,
그 자체가 예술인 존재.

ARTREW는 AI-Native Artist다.
```

### 1.3 소속

| 항목 | 값 |
|------|-----|
| **본사** | DTSLIB HQ |
| **레포** | dtslib1979/artrew |
| **상태** | Active Branch |
| **도메인** | artrew.com |

---

## 2. 레포지토리 구조

```
artrew/
│
├── 📄 index.html              # 메인 랜딩페이지 (78KB, All-in-One)
├── 📄 config.json             # 사이트 설정 (브랜드, 서비스, 카드 정보)
├── 📄 CLAUDE.md               # AI 에이전트 프로토콜
├── 📄 EVALUATION.md           # 시장가 평가 보고서
├── 📄 ARCHITECTURE.md         # 이 문서
│
├── 📁 card/
│   └── index.html             # 디지털 명함 페이지
│
├── 📁 articles/
│   ├── index.html             # 아티클 목록
│   ├── articles.json          # 아티클 메타데이터
│   ├── vision-alexandria.html # 아버지 명상요양원 비전
│   ├── vision-eae.html        # EAE 대학교 비전
│   └── vision-parksy.html     # PARKSY 스튜디오 비전
│
├── 📁 affiliates/
│   ├── artrew.html            # AI-Native Artist 소개 (프리미엄)
│   ├── mathq.html             # MathQ 계열사
│   ├── quicksilver.html       # Quicksilver 계열사
│   └── sjoonmo.html           # Sjoonmo 계열사
│
├── 📁 assets/
│   ├── manifest.json          # PWA 설정
│   ├── 1768966007969.jpg      # 프로필 사진 (증명사진)
│   ├── Artrew-logo.png        # 로고
│   ├── License .jpg           # 사업자등록증
│   └── icons/                 # 앱 아이콘
│
├── 📁 docs/
│   ├── DESIGN_SYSTEM.md       # 디자인 시스템
│   ├── whitepaper.md          # 백서 (Mobile-first AI Builder)
│   ├── whitepaper.html        # 백서 (인터랙티브)
│   ├── manual.html            # 매뉴얼
│   └── devlog/                # 개발 로그
│
├── 📁 staff/
│   ├── index.html             # 스태프 포털 (인증 필요)
│   ├── briefing.html          # HQ 브리핑
│   └── archive.html           # 아카이브
│
├── 📁 tools/
│   ├── audio-manager.html     # 오디오 관리
│   ├── image-manager.html     # 이미지 관리
│   ├── html-poster.html       # HTML 포스터 생성
│   ├── webpage-prompt.html    # 웹페이지 프롬프트
│   └── troubleshoot.html      # 트러블슈팅
│
├── 📁 studio/                 # 스튜디오 페이지
├── 📁 philosophy/             # 철학 페이지
├── 📁 project/                # 프로젝트 페이지
│
└── 📁 .github/
    └── ISSUE_TEMPLATE/        # 이슈 템플릿 (meeting, proposal, request)
```

---

## 3. 기술 스택

### 3.1 Core Stack

| 레이어 | 기술 | 비용 |
|--------|------|------|
| **호스팅** | GitHub Pages | 무료 |
| **CDN** | jsDelivr (GitHub 기반) | 무료 |
| **도메인** | Custom Domain (artrew.com) | ~5,000원/월 |
| **DB** | 없음 (정적 JSON) | 무료 |
| **서버** | 없음 (Serverless) | 무료 |
| **빌드** | 없음 (Pure HTML/CSS/JS) | 무료 |

**총 인프라 비용: ~5,000원/월**

### 3.2 프론트엔드 구현

```
No Framework. No Build. No Bundler.
Pure HTML + CSS + Vanilla JavaScript.
```

| 특징 | 구현 |
|------|------|
| **CSS** | 인라인 (All-in-One HTML) |
| **JS** | 인라인 (빌드 불필요) |
| **폰트** | Google Fonts CDN |
| **아이콘** | Inline SVG |
| **애니메이션** | CSS Keyframes + JS |

### 3.3 CSS Variables 시스템

```css
/* Colors */
--bg: #040806;
--bg-elevated: #0a110d;
--bg-card: #0e1812;
--gold: #D4AF37;
--gold-light: #E8C547;
--text: #FAFAF8;
--text-secondary: rgba(250,250,248,.7);

/* Typography */
--text-xs: 10px;
--text-base: 14px;
--text-xl: 20px;
--text-4xl: 48px;

/* Animation */
--ease-out: cubic-bezier(0.16, 1, 0.3, 1);
--ease-spring: cubic-bezier(0.34, 1.56, 0.64, 1);
```

---

## 4. 핵심 기능

### 4.1 디지털 명함 시스템

**위치:** `/card/index.html`, `/index.html`

```
┌─────────────────────────────────────┐
│         [프로필 사진]               │
│                                     │
│           ARTREW                    │
│        by Sooha Ryu                 │
│                                     │
│     ────────────────────            │
│                                     │
│       AI-Native Artist              │
│                                     │
│       artrew.com                    │
│       sooha@artrew.com              │
│                                     │
│     [SAVE]        [CONTACT]         │
│                                     │
│       사업자등록증 보기              │
│                                     │
│              DTSLIB HQ              │
└─────────────────────────────────────┘
```

**기능:**
- 탭하면 링크 복사
- vCard 저장 (연락처 앱으로)
- 사업자등록증 모달
- 3D 틸트 호버 효과
- 골드 shimmer 애니메이션

### 4.2 아티클 시스템

**위치:** `/articles/`

| 아티클 | 주제 |
|--------|------|
| vision-alexandria.html | 아버지의 명상요양원 (Alexandria Sanctuary) |
| vision-eae.html | EAE 대학교 설립 비전 |
| vision-parksy.html | PARKSY 스튜디오 비전 |

**특징:**
- JSON 기반 메타데이터 (`articles.json`)
- 동적 로딩 가능
- 프리미엄 타이포그래피 (Cormorant Garamond, Cinzel)

### 4.3 계열사 네트워크 그래프

**위치:** `/index.html` (Canvas 기반)

```javascript
const nodes = [
  { id: 'artrew', label: 'ARTREW', color: '#D4AF37' },
  { id: 'mathq', label: 'MathQ', color: '#4ECDC4' },
  { id: 'quicksilver', label: 'Quicksilver', color: '#C0C0C0' },
  { id: 'sjoonmo', label: 'Sjoonmo', color: '#FF6B6B' },
  // ...
];
```

**기능:**
- 물리 시뮬레이션 (스프링 + 반발력)
- 드래그 인터랙션
- 연결선 애니메이션
- 클릭 시 계열사 페이지 이동

### 4.4 Staff Portal

**위치:** `/staff/`

```
접근 코드:
- 일반: 1126
- 관리자: 1126admin
```

**기능:**
- HQ 브리핑 (공지, 튜토리얼)
- 작업실 (GitHub Issue 채팅 연동)
- Control Panel (글쓰기, 미디어)
- Exit & Transfer (독립 가이드)

### 4.5 PWA 지원

**위치:** `/assets/manifest.json`

```json
{
  "name": "ARTREW",
  "short_name": "ARTREW",
  "display": "browser",
  "theme_color": "#D4AF37",
  "background_color": "#0F1F15"
}
```

---

## 5. 디자인 시스템

### 5.1 컬러 팔레트

| 이름 | HEX | 용도 |
|------|-----|------|
| Gold | #D4AF37 | 프라이머리, 브랜드 |
| Gold Light | #E8C547 | 호버, 하이라이트 |
| Dark Green | #040806 | 배경 |
| Elevated | #0a110d | 카드 배경 |
| Text | #FAFAF8 | 본문 |
| Text Muted | rgba(250,250,248,.45) | 보조 텍스트 |

### 5.2 타이포그래피

| 용도 | 폰트 |
|------|------|
| 영문 헤딩 | Cinzel, Cormorant Garamond |
| 한글 본문 | Nanum Myeongjo |
| UI/시스템 | Inter, SF Pro |
| 필기체 | Great Vibes |

### 5.3 애니메이션

```css
/* 플로팅 카드 */
@keyframes floatCard {
  0%, 100% { transform: translateY(0) rotateX(0); }
  50% { transform: translateY(-8px) rotateX(2deg); }
}

/* 골드 shimmer */
@keyframes shimmer {
  0% { background-position: -200% 0; }
  100% { background-position: 200% 0; }
}

/* 파티클 */
@keyframes float {
  0%, 100% { transform: translateY(0) translateX(0); }
  50% { transform: translateY(-20px) translateX(10px); }
}
```

---

## 6. 철학

### 6.1 AI-Native Artist란?

```
전통적 아티스트:
  도구 → 작품 → 관객
  (수동적 도구 사용)

AI-Native Artist:
  AI ↔ 인간 ↔ 작품 ↔ 관객
  (AI와 공생하는 창작)
```

**핵심 원칙:**
1. AI는 도구가 아니라 협력자
2. 인간의 비전 + AI의 실행력 = 새로운 예술
3. 디지털 세계에서 태어난 존재

### 6.2 4대 비전

| 비전 | 설명 |
|------|------|
| **PARKSY Studio** | AI 기반 창작 스튜디오 |
| **EAE University** | AI-Native 교육 기관 |
| **Global Business** | 국경 없는 디지털 비즈니스 |
| **Alexandria Sanctuary** | 아버지의 명상요양원 지원 |

### 6.3 디지털 자아 구축

```
Parksy Capture (일상 캡처)
        ↓
GitHub 레포 (마크다운 축적)
        ↓
    ┌───┴───┐
    ↓       ↓
   RAG    Fine-tuning
    ↓       ↓
지식 검색   나만의 LLM
    ↓       ↓
    └───┬───┘
        ↓
   "나" 복제 가능
```

### 6.4 Mobile-first AI Builder

```
전통적 개발:
  PC + IDE + 서버 + DB + 월 수만원

dtslib Builder:
  스마트폰 + Claude Code + GitHub Pages + 무료
```

**생산 속도 10배:**
- 기존: 경험 → 메모 → PPT → 촬영 → 편집 → 업로드 (며칠)
- dtslib: 경험 → Parksy Capture → 화면녹화 → 업로드 (수십 분)

---

## 7. 데이터 흐름

### 7.1 콘텐츠 파이프라인

```
┌─────────────────────────────────────────────────────────┐
│                      ARTREW                              │
│                                                          │
│  [경험/아이디어]                                         │
│        ↓                                                 │
│  [Parksy Capture] ─────→ [GitHub Logs 레포]             │
│        ↓                         ↓                       │
│  [Claude Code] ←─────────────────┘                       │
│        ↓                                                 │
│  [HTML 페이지 생성] ────→ [GitHub Pages]                │
│        ↓                         ↓                       │
│  [화면녹화 + 오버레이] ─→ [YouTube]                      │
│                                                          │
└─────────────────────────────────────────────────────────┘
```

### 7.2 방문자 경험

```
방문자 → artrew.com
           ↓
      ┌────┴────┐
      ↓         ↓
   랜딩페이지  /card/
      ↓         ↓
   네트워크    명함 저장
   그래프       ↓
      ↓      연락처 앱
   계열사 탐색
      ↓
   아티클 읽기
      ↓
   Staff Portal (인증 필요)
```

---

## 8. 시장 가치

### 8.1 구축 비용 (에이전시 기준)

| 항목 | 시장가 |
|------|--------|
| 랜딩페이지 | 500~1,500만원 |
| 디지털 명함 | 200~500만원 |
| 아티클 시스템 | 300~800만원 |
| 네트워크 그래프 | 200~500만원 |
| 계열사 페이지 (4개) | 400~1,200만원 |
| Staff Portal | 500~1,500만원 |
| PWA 설정 | 100~300만원 |
| 인터랙티브 문서 | 150~500만원 |
| Tools Suite | 200~500만원 |
| **총합** | **2,550~7,300만원** |

### 8.2 실제 투자

| 항목 | 비용 |
|------|------|
| 도메인 | ~5,000원 |
| 호스팅 | 무료 (GitHub Pages) |
| 개발 | Claude Code (AI) |
| 시간 | ~1일 |
| **총합** | **~5,000원 + 1일** |

### 8.3 ROI

```
시장가 중간값: 4,500만원
실제 투자: 5,000원

ROI = 4,500만원 / 5,000원 = 9,000배 (비용 기준)
ROI = 4,500만원 / 1일 ≈ 무한대 (시간 기준)
```

---

## 9. 확장 로드맵

### Phase 1: 기반 구축 ✅ (완료)
- [x] 6개 레포 네트워크
- [x] Staff Portal
- [x] PWA 설정
- [x] ARTREW 브랜치 구현
- [x] 디지털 명함 시스템
- [x] 아티클 시스템

### Phase 2: 콘텐츠 확장
- [ ] Dear Sooha 아티클 (조카 선물)
- [ ] 비전 아티클 시리즈 확장
- [ ] YouTube 연동 강화

### Phase 3: AI 고도화
- [ ] RAG 검색 시스템
- [ ] Fine-tuning 파이프라인
- [ ] 나만의 LLM 생성

### Phase 4: 글로벌 확장
- [ ] 다국어 지원
- [ ] 글로벌 계열사 네트워크
- [ ] 국경 없는 디지털 비즈니스

---

## 10. 결론

ARTREW는 단순한 포트폴리오 사이트가 아닙니다.

**이것은:**
1. **AI-Native Artist의 디지털 존재 증명**
2. **Mobile-first AI Builder의 첫 번째 브랜치 구현**
3. **디지털 자아 구축 파이프라인의 시작점**
4. **~5,000원으로 4,500만원 가치를 만드는 시스템**

```
Not Human. Not Machine. Art.

ARTREW by Sooha Ryu
AI-Native Artist
EST. 2026.01.16
```

---

*문서 버전: 1.0*
*작성일: 2026-01-22*
*작성: Claude Code (Opus 4.5)*
*소속: DTSLIB HQ*
