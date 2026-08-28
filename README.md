# 호랑팜 거래처 배포 자료 (암호화 · 기간 만료 자동 삭제)

- `r/<token>/index.html` — StatiCrypt(AES-256-CBC, PBKDF2 60만회)로 암호화된 보고서 HTML. 비밀번호는 이 저장소에 없다.
- `EXPIRES` — 열람 마지막 날(KST). 다음 날 00:00 KST에 `expire` 워크플로가 `r/` 전체를 삭제하고 안내 페이지로 교체한다. 자료 본문에도 같은 날짜의 만료 가드가 있다.
- **즉시 파기**: Actions → expire → Run workflow → force=`true`. 또는 저장소 삭제.
- **기간 연장**: `EXPIRES` 값 수정 후 push. (자료 안의 "열람 링크는 ~까지" 문구와 본문 만료 가드는 재빌드가 필요하다.)
- 공개 저장소인 이유: 무료 플랜의 GitHub Pages는 공개 저장소에서만 동작한다. 노출되는 것은 암호문뿐이다.
