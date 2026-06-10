# INO_Manual — 이지롤 통합 가이드 (웹 공개용)

> **사용설명서 + Home Assistant 연동 가이드**를 한 사이트로 제공하는 통합 문서 저장소.
> GitHub Pages(MkDocs Material)로 배포 — 상단 탭으로 두 가이드 구분.

## 📂 구조

```
INO_Manual/
├── mkdocs.yml                  ← 사이트 설정 (탭 내비게이션: 사용설명서/HA)
├── .github/workflows/deploy.yml ← main 푸시 시 자동 빌드·배포
└── docs/
    ├── index.md                ← 홈 (가이드 선택)
    ├── easyroll/               ← 사용설명서 (일반 고객용, 6편)
    └── ha/                     ← HA 연동 가이드 (스마트홈 사용자용, 5편)
```

## ✍️ 작성 규칙 (공개용)

1. **고객 눈높이** — 내부 용어(rc코드, abs 등) 금지.
2. **보안** — 실제 계정/비밀번호/서버IP 절대 금지 (내부용 `../INO_HA/` 가이드엔 실계정 있음 — 복사 시 주의).
3. **✍️ 표시** = 채울 자리 (사진·앱 스크린샷·스토어 링크·고객센터·리모컨 사양·HA 캡처).
4. 기술 출처: `../INO_Algorithm/` 문서와 일치 유지. HA 기능 변경 시 ha/ 문서도 갱신.

## 🚀 배포 절차

1. GitHub **공개** 저장소 생성 (예: `inoshade/easyroll-docs`)
2. 이 폴더를 push (이미 git 저장소로 초기화됨, 브랜치 main)
3. push하면 Actions가 자동으로 `gh-pages` 브랜치에 사이트 빌드
4. 저장소 Settings → Pages → Source = `gh-pages` 브랜치 → 주소 발급
5. (선택) 도메인 연결: 예 `docs.inoshade.com` + 제품 QR코드

## 진행 상태

- [x] 초안 11편 + 통합 사이트 구성 (2026-06-10, 펌웨어 v2.9.8 기준)
- [ ] ✍️ 채우기 (사진·스크린샷·링크·연락처·리모컨 버튼 사양)
- [ ] 검수 (처음 보는 사람이 따라해 보기)
- [ ] GitHub 저장소 생성 + push + Pages 활성화
- [ ] 도메인 연결 + QR코드 제작
