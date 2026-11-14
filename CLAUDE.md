# LAMFU Archive — 프로젝트 안내

작가 서진의 일러스트·썸네일 포트폴리오 사이트. 작가 캐릭터는 LAMFU(Lamb + wolf).
보고와 설명은 한국어로, 짧고 직접적으로.

## 배포
- GitHub 조직 `lamfu-profile`의 저장소 `lamfu-profile.github.io` → GitHub Pages(main / root)로 배포.
- 주소: https://lamfu-profile.github.io
- **joysanup.co.kr(서진의 의뢰 사이트)은 절대 연결하거나 수정하지 말 것.** 도메인·DNS·CNAME 관련 제안 시 이 도메인 제외.

## 구조
- `index.html` — 화면 전체(HTML·CSS·JS 한 파일). 빌드 도구 없음.
- `data/works.json` — 작품 배열. 필드: title, image, category, description, tags[], date(YYYY-MM-DD), featured(boolean)
- `data/site.json` — profile{name, role, lead, intro, fields[], tools[], email, links[{label,url}], commission(open|closed), commissionNote}, hero{image, zoom, x, y}, categories[{name, en, color}]
- `images/` — 이미지. Pages CMS 업로드도 여기로 저장됨.
- `.pages.yml` — Pages CMS 입력 화면 설정. `data/*.json` 필드 이름을 바꾸면 `.pages.yml`과 `index.html`을 함께 고칠 것.

## 콘텐츠 관리
- 작품·프로필은 Pages CMS(app.pagescms.org)에서 편집하며, 편집 결과는 GitHub에 커밋됨 → 코드 작업 전 반드시 `git pull`.
- 작품의 category는 site.json categories의 name과 같은 문자열로 매칭. 목록에 없는 이름은 회색 탭으로 자동 추가됨.
- Pages CMS 업로드는 약 4.5MB 요청 한도(413 오류)가 있음 → 이미지는 3MB 이하 권장(긴 쪽 2000~2500px, JPG/WebP). 큰 파일은 GitHub 웹에서 `images/`로 직접 업로드.
- 저장소·사이트 용량 1GB 기준. 큰 원본 업로드 금지(삭제해도 히스토리에 남음).

## 디자인
- 밝은 게임 UI: 웜그레이 바탕, 흰 패널, 차콜 글자, 코랄(#D6545C) 포인트. `:root` 토큰 기준으로 수정.
- 요소: 왼쪽 아이콘 레일 메뉴, LAMFU 글자 모양 프레임(SVG clipPath), 캐릭터 스탯 패널, 기울어진 Featured 띠, 코너 브래킷.
- 마우스 반응 애니메이션은 최소한으로 유지, prefers-reduced-motion 존중.
- 커미션 OPEN/CLOSED 표시는 버튼이 아님(표시 전용).
- 라우팅은 #home / #works / #profile 해시. 링크 클릭은 JS가 직접 처리.

## 로컬 미리보기
- `index.html`을 파일로 직접 열면 JSON을 못 읽음 → `python3 -m http.server 8000` 또는 VS Code Live Server 사용.
