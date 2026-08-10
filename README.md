# 최성우 · 崔作家 — 개인 브랜딩 사이트

GitHub Pages용 커리어 사이트. 메인 홈(경력 서사)과 AI QA 포트폴리오(콘솔 대시보드)로 구성.
공통 톤: Navy #1B2A4A · Orange #E8710A / Pretendard · JetBrains Mono.

## 폴더 구조

```
/ (repo root)
├─ index.html            ← 메인 홈 (경력 스토리: 광고 AE → IT PM → AI QA)
├─ qa/
│   ├─ index.html        ← AI QA 포트폴리오 메인 (콘솔 대시보드, 10개 프로젝트)
│   ├─ project-01.html   ← 킬러: VOC 멀티에이전트 QA
│   ├─ project-02.html   ← 킬러: AI 품질 평가 플랫폼
│   ├─ project-05.html   ← 킬러: RaiT 평가 시스템
│   └─ style.css         ← QA 포트폴리오 전용 스타일
├─ assets/
│   └─ resume.pdf        ← [넣어야 함] 이력서·경력기술서 PDF
└─ README.md
```

- 첫 화면은 루트 `index.html`(메인 홈). 상단 우측 "QA 포트폴리오 →" 및 히어로 버튼이 `./qa/` 로 연결됨.
- `qa/` 안의 페이지들은 상단 "← 메인 홈"으로 루트 `index.html`로 복귀.
- `index.html`은 인라인 스타일(자체 완결), `qa/`는 `qa/style.css`를 공유.

## 배포 절차

1. 저장소 생성 후 위 구조 그대로 루트에 업로드/푸시
   - 대표 사이트: 저장소명 `<username>.github.io` → `https://<username>.github.io/`
   - 프로젝트 페이지: 임의 이름 → `https://<username>.github.io/<repo>/`
2. Settings → Pages → Source: `Deploy from a branch`
3. Branch `main` / 폴더 `/ (root)` → Save
4. 1~2분 후 게시 URL 확인

## 배포 전 채워야 할 항목 (index.html)

| 위치 | 플레이스홀더 | 설명 |
|------|--------------|------|
| Contact · Links | `{{GITHUB_USER}}` | GitHub 사용자명 |
| Contact · Links | `{{LINKEDIN_URL}}` | LinkedIn 프로필 전체 URL |
| Contact · 서류 | `./assets/resume.pdf` | 이력서·경력기술서 PDF 실제 파일 배치 |

## 연결 점검 체크리스트

- [ ] 메인 홈 폰트(Pretendard·JetBrains Mono) 적용 확인
- [ ] 히어로/네비 "QA 포트폴리오 →" → `qa/` 진입
- [ ] qa 포트폴리오 킬러 카드(01·02·05) → 상세페이지 진입, "← 메인 홈" 복귀
- [ ] Contact의 GitHub·LinkedIn·PDF 링크 동작 (플레이스홀더 교체 후)
- [ ] 모바일(≤640px) 네비 축약·카드 1열 정상

## 수정 메모

- v4 원본은 `<style>` 안 `@import`가 `:root` 뒤에 있어 웹폰트가 로드되지 않는 상태였음.
  → `<head>`의 `<link>` 방식으로 이전해 폰트가 정상 적용되도록 수정함(디자인은 동일).
- 타임라인·프로젝트 내용은 업로드본(v4)을 그대로 유지함.
