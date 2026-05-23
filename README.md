# tiktok-chat-game-releases

[`yosubs/tiktok-chat-game`](https://github.com/yosubs/tiktok-chat-game) 의 BJ별 빌드 산출물(`.dmg` / `.exe`) 배포 전용 public 저장소입니다.

> 소스 코드는 private 저장소에서 관리되며, GitHub Actions가 빌드 시 이 저장소로 binaries만 푸시합니다.

## 받는 곳

[Releases](https://github.com/yosubs/tiktok-chat-game-releases/releases) 탭에서 본인 TikTok 아이디가 들어간 태그를 찾으세요.

태그 형식: `host-<tiktok_user>-v<version>`
예: `host-yo.sub-v0.1.0`

각 Release 자산:

- macOS: `.dmg` (arm64용과 x64용 두 종류 — 본인 Mac CPU에 맞는 파일)
- Windows: `.exe` (x64)

## 설치 시 주의

### macOS

코드 서명이 적용되지 않은 빌드입니다. `.dmg`로 앱을 `/Applications`에 끌어다 놓은 뒤, 터미널에서 한 번만 다음을 실행해 Gatekeeper 격리 속성을 제거하세요:

```bash
xattr -cr "/Applications/TikTok Chat Game.app"
```

이후로는 일반 앱처럼 더블클릭으로 실행됩니다.

### Windows

`.exe` 인스톨러를 실행하세요. SmartScreen 경고가 뜨면 "추가 정보" → "실행"으로 진행합니다.

## 자동 업데이트

앱이 부팅될 때마다 본인 태그 중 최신 버전을 자동으로 확인합니다. 새 버전이 있으면 다이얼로그가 뜨며, "다운로드 페이지 열기" 버튼으로 곧장 해당 Release 페이지로 이동합니다. 트레이 메뉴의 "업데이트 확인"으로 수동 체크도 가능합니다.
