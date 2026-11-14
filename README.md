# LAMFU Archive

일러스트·썸네일 포트폴리오 사이트. 작품과 설정은 Pages CMS(app.pagescms.org)에서 편집합니다.

## 폴더 구조
- `index.html` — 사이트 화면
- `data/works.json` — 작품 목록
- `data/site.json` — 프로필, 커미션 상태, 카테고리, 홈 프레임 그림
- `images/` — 이미지 (Pages CMS로 올린 그림도 여기에 저장됨)
- `.pages.yml` — Pages CMS 입력 화면 설정 (지우지 마세요)

## 처음 한 번만
1. 이 폴더의 파일을 저장소 맨 위(root)에 올리기
2. Settings → Pages → Source: Deploy from a branch → main / (root) → Save
3. 도메인 연결: 기존 저장소의 Settings → Pages에서 joysanup.co.kr을 먼저 지운 뒤, 이 저장소의 Custom domain에 입력 → Enforce HTTPS 체크
4. app.pagescms.org → Sign in with GitHub → GitHub App 설치 (Only select repositories → 이 저장소) → 저장소 열기

## 작품 올리기
Pages CMS → 작품 → 항목 추가 → 이미지·제목·카테고리·설명·해시태그·날짜 입력 → Save
저장 후 1~2분 뒤 사이트에 반영됩니다.

## 주의
- 카테고리 이름은 '사이트 설정 > 카테고리'에 있는 한글 이름과 똑같이 적어야 같은 탭에 모입니다.
- 이미지 파일 이름은 영문·숫자를 권장합니다.
