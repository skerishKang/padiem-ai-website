# Padiem AI 공식 웹사이트/블로그 구축 프로젝트 플랜

## 1. 프로젝트 목표 및 요구사항
- 컴포넌트 기반, 반응형, 자동 게시/배포, 유지보수성 높은 공식 웹사이트 및 블로그 구축
- Claude팀(디자인)과 Google팀(기획) 자료를 최대한 반영

## 2. 기술 스택 확정 및 개발 환경 구축
- SSG 후보: Hugo, Next.js(SSG), Astro 등
- CMS 후보: Decap CMS(Headless), 또는 마크다운+Git
- 호스팅: Netlify, Cloudflare Pages 등
- 1차 제안: Hugo + 마크다운 + Netlify (빠른 구축, 쉬운 Git 연동, Decap CMS 옵션도 병행 검토)
- 작업: 기술 스택별 폴더/파일 구조 조사 및 샘플 프로젝트 생성

## 3. 디자인 시스템 분석 및 컴포넌트 설계
- 첨부된 컴포넌트디자인.md, 컴포넌트설계가이드.md 분석
- SSG의 템플릿/컴포넌트 구조로 변환 설계
- 우선순위: 레이아웃(사이드바, 헤더, 메인, 푸터) → 네비게이션 → 버튼/카드 → 블로그/페이지 템플릿

## 4. 사이트맵 및 네비게이션 구조 반영
- Google팀 제공 사이트맵 구조 확인(필요시 추가 자료 요청)
- SSG의 메뉴 구조로 변환

## 5. CMS/콘텐츠 관리 방식 확정
- Decap CMS vs 마크다운+Git 비교
- Google팀의 콘텐츠 입력 편의성 고려
- 1차: 마크다운+Git 구조 설계, Decap CMS 연동 옵션도 문서화

## 6. 자동 게시/배포 파이프라인 설계
- Netlify 연동, Git push/Decap CMS 발행 시 자동 빌드/배포 설정
- 도메인 연결(추후 padiemai.com)

## 7. SEO/기본 설정
- 템플릿에 메타태그, sitemap.xml, robots.txt 자동 생성 기능 설계

---

## [즉시 실행할 1차 작업 목록]

1. 기술 스택 후보별 폴더/파일 구조 조사 및 샘플 프로젝트 생성
2. Claude팀 디자인 시스템 분석 요약 및 컴포넌트 변환 설계안 작성
3. Google팀 사이트맵/콘텐츠 구조 확인 요청(필요시)
4. 단계별 진행 상황 및 결정 사항을 본 파일에 지속적으로 업데이트

---

### [진행상황 로그]
- 1차 플랜 및 즉시 실행 작업 목록 기록 (2024-06-07)
- Hugo 샘플 프로젝트 생성 및 기본 구조 조사 완료 (2024-06-07)
- layouts/_default/baseof.html, partials/sidebar.html, header.html, footer.html, index.html, static/css/style.css, static/images 등 핵심 파일/폴더 생성 및 디자인 시스템 적용 (2024-06-07)
- hugo server로 로컬 개발 서버 실행, 기본 레이아웃 및 스타일 정상 적용 확인 (2024-06-07)
- content 하위 주요 디렉토리 및 archetypes(blog.md, pages.md) 생성, 구조 설계 완료 (2024-06-07)
- layouts/_default/list.html, single.html 등 핵심 템플릿 개발 및 각 디렉토리별 샘플 콘텐츠(.md) 생성, 로컬 서버에서 정상 렌더링 확인 (2024-06-07)
- layouts/blog/list.html, single.html, partials/blog_sidebar.html 등 블로그 전용 템플릿 및 사이드바 구현, taxonomies 설정, 로컬 서버에서 블로그 기능 정상 확인, tree.md 및 project_plan.md 문서 업데이트 (2024-06-07)
- content/solutions/solution-a.md에 솔루션 소개 실데이터(솔루션 개요, 주요 기능, 도입 효과 등) 1차 추가 완료 (2024-07-09)
- content/technology/ai-tech.md에 기술 소개 실데이터(핵심 AI 기술, 적용 분야, 차별점 등) 1차 추가 완료
- Playwright 기반 자동화 QA 테스트(회사소개, 솔루션, 기술 페이지 진입 및 스크린샷, 주요 UI/텍스트/접근성 확인, 콘솔 에러 로그 수집) 1차 완료. (404 에러 리소스 있음, 추가 점검 필요)
- 블로그 샘플 포스트(ai-technology-trends.md) 및 썸네일 이미지 추가, 블로그 목록/사이드바/카테고리/태그/요약/썸네일 등 QA 완료 (2025-05-05)

# 프로젝트 진행 상황 (2024-07-09)

## 완료된 일
- 디자인 시스템 1~3순위(타이포그래피, 색상, 레이아웃, 버튼, 카드, 네비게이션, 블로그, 폼, 푸터 등) CSS/HTML 구조 적용
- 반응형(모바일/태블릿/데스크탑/와이드) 중단점 및 레이아웃 완성
- 버튼/카드/블로그/폼/푸터 등 주요 컴포넌트 상태(hover, focus, active, disabled) 및 인터랙션(트랜지션, 그림자, 색상 변화) 구현
- 접근성(aria, tabindex, 포커스 스타일 등) 및 키보드 네비게이션 적용
- 사이드바/헤더/오버레이/햄버거 메뉴 등 모바일 UX 구현
- 블로그 목록/상세, 카드 그리드, 섹션, 본문 타이포그래피, 인용/코드/이미지/캡션 등 세부 스타일 적용
- 푸터에 회사 정보, 소셜 미디어, 사업자, 이메일 등 공식 정보 및 반응형/접근성 적용

## 진행 중
- 전체 레이아웃/접근성/반응형 최종 점검 및 마무리 QA
- 실데이터/콘텐츠 적용 및 렌더링 테스트(콘텐츠 전달 시)
- Playwright 등 자동화 테스트 환경 구축(예정)

## 다음 단계
- 최종 QA 및 버그 수정
- 실데이터/콘텐츠 반영 및 최종 디자인/기획팀 피드백 수렴
- 배포 및 운영 가이드 문서화

## 2024-07-09
content/about/company.md에 회사소개 실데이터(회사 개요, 미션, 비전, 연혁 등) 1차 추가 완료 

- [완료] padiem-logo-white.svg (화이트 로고) 파일 추가
- [완료] padiem-logo-black.svg (블랙 로고) 파일 추가
- [완료] padiem-icon-only.svg (아이콘 전용 로고) 파일 추가
- [완료] favicon.svg (SVG 버전 파비콘) 파일 추가 및 favicon.ico 변환 필요

- [정책] 모든 브랜드 자산 SVG 파일은 static/brand-assets/logo 또는 static/brand-assets/favicon 경로에 저장 및 관리 