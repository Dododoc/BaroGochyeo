# 바로고쳐 (BaroGochyeo) — standalone demo

Claude 없이 열리는 버전이에요. 데이터는 각 폰에만 저장되고, AI 결과는 예시 데이터예요.

## 올리는 법 (GitHub Pages)
1. github.com → New repository → 이름 입력 → Public → Create
2. "uploading an existing file" → 이 폴더의 파일 전부(index.html, ar-measure.html, manifest.webmanifest, icons 폴더)를 끌어다 놓기 → Commit
3. Settings → Pages → Deploy from a branch → main / (root) → Save
4. 1~2분 뒤 나오는 https 주소를 팀원에게 공유

## 쓰는 법
- 홈 화면에 추가하면 앱처럼 열려요 (안드로이드 Chrome ⋮ 메뉴 / 아이폰 Safari 공유 버튼)
- 시연용 데이터로 되돌리기: 주소 뒤에 `?reset` 을 붙여 한 번 열기
- AR 측정: 안드로이드 Chrome에서 확인 화면의 "AR measure"

## 네이버 지도 켜기
1. 네이버 클라우드 플랫폼 콘솔 → Maps → Application 등록 → Dynamic Map 선택
2. Web 서비스 URL에 GitHub Pages 주소 등록 (예: https://아이디.github.io)
3. 발급된 Client ID를 **config.js** 의 `window.NAVER_MAP_CLIENT_ID = "";` 따옴표 안에 넣고 저장 (index.html을 업데이트해도 ID는 유지돼요)
4. ID가 비어 있거나 틀리면 기본 원형 지도로 자동 전환돼요

## 사진 핀
- 사진이 있는 신고는 지도에서 사진 핀으로 보여요. 누르면 그 자리에 큰 사진 카드가 떠요.
- 지도에는 실제 사진 6장만 시연 데이터로 들어 있어요. 앱에서 새로 찍어 신고하면 그 사진이 핀으로 추가돼요.
- 새로 찍은 신고는 그 폰에만 저장돼요. 다른 폰에서는 보이지 않아요.
- 예전 시연 데이터가 남아 있으면 자동으로 새 데이터로 바뀌어요. 시연 전에 되돌리려면 주소 뒤에 `?reset` 을 붙여 한 번 열어요.
