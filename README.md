# SCERTS 자동화 시스템

검단ABA언어행동연구소 · 민다혜 (BCBA)

SCERTS® 모델 기반 ABA 임상 자동화 시스템 — 진단·IEP·중간·종결보고서 자동 생성

## 🚀 배포 URL

https://aba-geomdan.github.io/abageomdan-scerts/

## 로컬 개발

```bash
npm install
npm run dev
```

브라우저에서 http://localhost:3000 접속

## 환경 변수

`.env.local` 파일을 프로젝트 루트에 만들고 다음 내용 입력:

```
VITE_SUPABASE_URL=https://vdubgrxwijydwfabwpnk.supabase.co
VITE_SUPABASE_ANON_KEY=...(anon key)
```

`.env.local.example` 파일을 참고하세요.

## GitHub 배포

### 처음 한 번만 설정

1. **GitHub Secrets 등록**
   - 저장소 → Settings → Secrets and variables → Actions → New repository secret
   - `VITE_SUPABASE_URL` 추가 (값: Supabase Project URL)
   - `VITE_SUPABASE_ANON_KEY` 추가 (값: anon public key)

2. **GitHub Pages 활성화**
   - 저장소 → Settings → Pages
   - Source: **GitHub Actions** 선택

### 이후 배포

`main` 브랜치에 push하면 자동 배포됨 (1~2분 소요)

```bash
git add .
git commit -m "수정 내용"
git push
```

## 주요 기능

- 멀티유저 로그인 (관리자 + 선생님 계정)
- 다기기 데이터 동기화 (Supabase)
- 관리자 전체 조회
- SCERTS 단계별 진단 (사회적·언어·대화 파트너)
- 자동 채움: 현행수준 → IEP → 중간보고서 → 종결보고서
- PDF 인쇄
- 카톡 질문지 (부모용)
- 부가 양식: 가족 지원, 전문가 협력, 의사소통 일정표, FBA

## 기술 스택

- React 18 + Vite
- Supabase (REST API)
- GitHub Pages (Actions 자동 배포)

## 저작권

본 시스템은 SCERTS® 모델 (Prizant et al., Brookes Publishing / 한국어판 학지사)에 근거합니다.

© 검단ABA언어행동연구소 · 민다혜 (BCBA). 무단 복제·배포·재판매·온라인 게시를 엄격히 금지합니다.
