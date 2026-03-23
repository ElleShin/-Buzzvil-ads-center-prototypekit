Buzzvil Ads Center UI 목업을 Claude가 자동으로 만들어주는 스킬입니다.
요구사항을 텍스트로 입력하면 광고센터 디자인 시스템에 맞는 인터랙티브 HTML 목업을 생성합니다.

## [⬇️ Skill 파일 다운로드](../../releases/latest/download/buzzvil-ads-center-dx.zip)

---

## 사용 예시

```
"라이브커머스 목록 화면 만들어줘"
"정산 페이지 만들어줘"
"선불충전 화면 만들어줘"
"협력광고 생성 폼 만들어줘"
```

결과물은 `.html` 파일로 생성되며, 다운로드 후 브라우저에서 바로 열어 확인할 수 있습니다.

---

## 설치 방법

### 준비물
- [Claude Desktop 앱](https://claude.ai/download)
- **Pro 이상의 플랜** (Skills 기능 필요)

### 설치 순서

➊ 위 **스킬 다운로드** 버튼 클릭 → `buzzvil-ads-center-dx.zip` 다운로드


➋ Claude Desktop 앱 실행

   
➌ **Settings → Capabilities → Skills**로 이동
<img width="4320" height="2040" alt="경로 안내" src="https://github.com/user-attachments/assets/6a6cd72d-e41a-453b-855f-716e893b6955" />


➍ `+` 버튼 → **Upload a skill** → zip 파일 선택
<img width="4320" height="2040" alt="경로 안내2" src="https://github.com/user-attachments/assets/54ea3c41-0750-4021-8ef5-432c6ea9ec42" />


➎ 설치 완료

---

## 사용 방법

설치 후 새 대화에서 만들고 싶은 화면을 자유롭게 입력하면 됩니다.

**기존 화면 재현**
- 라이브커머스 목록, 협력광고 목록, 정산, 리포트, 카탈로그, 멤버 관리 등

**신규 화면 생성**
- Figma에 없는 화면도 기존 디자인 패턴을 참고해서 자동으로 만들어줍니다

---

## GitHub Release 등록 방법 (관리자용)

스킬을 업데이트하거나 처음 등록할 때:

1. GitHub repo → **Releases** → **Create a new release**
2. **Tag version** 입력 (예: `v1.0.0`)
3. **Attach binaries** → `buzzvil-ads-center-dx.zip` 업로드
4. **Publish release**

이후 위 다운로드 버튼이 항상 최신 버전을 가리킵니다.

---

## Figma MCP 연결 (선택사항)

기본 설치만으로도 충분히 사용할 수 있습니다.
Figma MCP를 추가 연결하면 Figma 파일을 실시간으로 읽어 더 정확한 목업을 생성합니다.

<details>
<summary>Figma MCP 설정 방법 보기</summary>

### 1. Figma Personal Access Token 발급
1. Figma → 프로필 → Settings → Security
2. Personal access tokens → **Generate new token**
3. 이름 입력 (예: `claude-mcp`)
4. Scopes 체크:
   - ✅ `file_content:read`
   - ✅ `file_dev_resources:read`
   - ✅ `library_assets:read`
5. 토큰 복사 (창 닫으면 다시 볼 수 없음)

### 2. `claude_desktop_config.json` 설정

파일 위치:
- Mac: `~/Library/Application Support/Claude/claude_desktop_config.json`
- Windows: `%APPDATA%\Claude\claude_desktop_config.json`

아래 내용 추가:
```json
{
  "mcpServers": {
    "figma": {
      "command": "npx",
      "args": ["-y", "figma-developer-mcp"],
      "env": {
        "FIGMA_API_KEY": "여기에_발급받은_토큰_붙여넣기"
      }
    }
  }
}
```

> 기존 설정이 있다면 `mcpServers` 안에 `"figma": { ... }` 블록만 추가하세요.

### 3. Claude Desktop 재시작
Mac: `Cmd+Q` → 다시 실행 / Windows: 트레이 아이콘 종료 → 다시 실행

</details>

---

Made by Buzzvil Design Team
