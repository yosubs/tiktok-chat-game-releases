# tiktok-chat-game-releases

[`yosubs/tiktok-chat-game`](https://github.com/yosubs/tiktok-chat-game) 의 BJ별 빌드 산출물(`.dmg` / `.exe`) 배포 전용 public 저장소입니다.

> 소스 코드는 private 저장소에서 관리되며, GitHub Actions가 빌드 시 이 저장소로 binaries만 푸시합니다.

## 받는 곳

[Releases](https://github.com/yosubs/tiktok-chat-game-releases/releases) 탭에서 본인 TikTok 아이디가 들어간 태그를 찾으세요.

태그 형식: `host-<tiktok_user>-v<version>`
예: `host-yo.sub-v0.2.0`

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

## 자동 업데이트 (v0.2.0+)

앱이 부팅된 직후와 그 뒤 1시간 주기로 본인 태그(`host-<tiktok_user>-v*`) 중 최신 버전을 백그라운드에서 조용히 확인합니다. 새 버전이 발견되면 **어드민 창 상단 "상태" 섹션에 `⬆️ 업데이트 가능 vX.Y.Z` 버튼이 노출**됩니다.

- 버튼을 누르면 해당 Release 페이지가 브라우저에서 열립니다 → 본인 OS에 맞는 자산을 받아 재설치하세요.
- **버튼을 누르지 않으면 기존 버전을 그대로 계속 사용**합니다. 라이브 도중 강제로 끊기거나 갑자기 재시작되는 일은 없습니다.
- 트레이 아이콘 메뉴의 "업데이트 확인"으로 즉시 수동 체크도 가능합니다.

### v0.1.0 사용자 주의

v0.1.0에는 자동 알림 기능이 없습니다. v0.2.0을 **한 번은 [Releases 페이지](https://github.com/yosubs/tiktok-chat-game-releases/releases)에서 직접 받아 재설치**해 주세요. v0.2.0 이후의 모든 업데이트는 어드민 버튼으로 자동 안내됩니다.
