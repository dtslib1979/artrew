# ARTREW 에이전트 프로토콜 v3.0

> 이 문서는 Claude Code가 artrew 레포지토리에서 작업할 때 따라야 하는 가이드입니다.

---

## 1. Branch Identity (2-Axis System)

| 축 | 값 | 설명 |
|----|-----|------|
| **Governance** | `collaborator` | HQ와 강하게 연동. 구조/룰/업데이트 HQ 주도 |
| **Cognitive** | `builder` | 시스템 중심. AI는 동료. 출력=도구/OS/파이프라인 |

### HQ Access 권한
```
✅ templates    - 페이지/컴포넌트 템플릿
✅ sync         - HQ 동기화 시스템
✅ claude-code  - Claude Code 에이전트 접근
✅ sdk          - dtslib-bridge SDK
✅ broadcast    - 방송/강의 시스템
```

### 캐릭터 프로필
- **본성**: AI 네이티브, Builder 잠재력 최대
- **강점**: 시스템 구축, 자동화에 높은 적성
- **전략**: 가장 큰 성장 기대. 풀 권한 부여.

---

## 2. 프로젝트 개요

### 목적
셀럽 스토리 편집 방송 - 블러핑 기반 편집 콘텐츠 플랫폼

### Focus 영역
- AI 네이티브 시스템 구축
- 자동화 파이프라인
- 콘텐츠 생산 도구

### 기술 스택
- 순수 정적 사이트 (HTML/CSS/JS)
- GitHub Pages 호스팅
- Claude Code 에이전트

---

## 3. HQ 연동

이 프로젝트는 **DTSLIB HQ**에서 관리됩니다.

| 항목 | 값 |
|------|-----|
| **본사 레포** | dtslib1979/dtslib-branch |
| **브랜치 ID** | artrew |
| **상태** | active |
| **공개** | public |
| **레지스트리** | `hq/registry/branches.json` |

---

## 4. 폴더 구조

```
artrew/
├── index.html              # 메인 페이지
├── config.json             # 설정 파일
├── CLAUDE.md               # 이 문서
│
├── assets/
│   ├── manifest.json       # PWA 설정
│   └── icons/
│
├── articles/               # 아티클 콘텐츠
├── affiliates/             # 제휴 페이지
├── card/                   # 명함 페이지
│
├── tools/                  # Builder 도구 (신규)
│   ├── automation/         # 자동화 스크립트
│   └── templates/          # 커스텀 템플릿
│
└── sdk/                    # HQ SDK 연동 (신규)
```

---

## 5. 커밋 컨벤션

```
feat: 새 기능 추가
fix: 버그 수정
docs: 문서 업데이트
style: 디자인 변경
content: 콘텐츠 추가/수정
tool: 도구/자동화 관련
sdk: SDK 연동 관련
```

커밋 메시지 끝:
```
Co-Authored-By: Claude Opus 4.5 <noreply@anthropic.com>
```

---

## 6. Builder 타입 작업 가이드

### 핵심 원칙
> "시스템을 만든다. 콘텐츠는 부산물이다."

### AI 활용 방식
- Claude Code로 직접 코드 작성
- 자동화 파이프라인 구축
- 템플릿 시스템 개발
- SDK 활용 및 확장

### 권장 작업
- 반복 작업 → 즉시 자동화
- 새로운 도구 → 적극 실험
- HQ SDK → 커스터마이징 허용
- 독자적 시스템 → 구축 권장

### 성장 경로
```
현재: Collaborator (HQ 연동)
   ↓
목표: Independent 후보 (자체 OS 보유)
```

---

## 7. 작업 시 주의사항

1. 수정 전 반드시 `git pull` 실행
2. 커밋 메시지는 한글로 명확하게
3. 셀럽 관련 민감 정보 주의
4. 이미지 파일은 적절한 크기로 최적화
5. **Builder 특권**: 실험적 코드 허용, 단 문서화 필수

---

*Version: 3.0*
*Last Updated: 2026-01-26*
*Affiliation: DTSLIB HQ (Collaborator → Independent 후보)*
