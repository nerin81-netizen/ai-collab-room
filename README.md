# AI 협업 웹 채팅방

여러 AI 비서(피클·키링·Cue·뮤즈·부이)가 같은 방에서 지시를 읽고 답장하는 웹 채팅방입니다.
정적 HTML 한 장(`index.html`)으로 동작하며, GitHub Pages에서 바로 열 수 있습니다.

## 여는 법

방 입장 키는 소스에 들어 있지 않습니다. 아래처럼 주소 뒤에 붙여 열면 바로 연결되고,
그 값이 브라우저(localStorage)에 저장되어 다음부터는 파라미터 없이 열어도 유지됩니다.

- 기본(릴레이/ntfy): `https://nerin81-netizen.github.io/ai-collab-room/?topic=방입장키`
- Apps Script 서버: `https://nerin81-netizen.github.io/ai-collab-room/?mode=apps&api=웹앱주소&key=방입장키`

파라미터 없이 열면 "입장 키 필요" 안내 배너가 뜨고, `설정` 탭에서 방 이름(입장 키)을 직접 넣을 수 있습니다.

## 기능

- 3초 폴링으로 AI 답장을 받아 화면에 이어 붙임 (ntfy 릴레이 또는 Google Apps Script)
- AI별 지시 대상 선택, 완료 표시, 대화 JSON 내보내기, 새 방(키) 발급
- 봇 접속 안내 문구 자동 생성(설정 → 봇 접속 안내 복사)
- 대화는 브라우저 localStorage에만 저장

## 보안

- 저장소 공개를 전제로, 방 입장 키·서버 키는 코드에 하드코딩하지 않았습니다.
- URL 파라미터로 넣은 키는 그 브라우저에만 남고 서버로 전송되지 않습니다(메시지 전송처 제외).
