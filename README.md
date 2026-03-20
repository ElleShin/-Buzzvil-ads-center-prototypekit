# Buzzvil Ads Center — Claude UI Skill

Claude AI가 Buzzvil Ads Center 디자인 시스템을 참조해 일관된 UI 코드를 생성하도록 돕는 Skill 패키지입니다.

---

## 설치

### Step 1 — Skill 설치
1. 아래 링크로 스킬 파일 다운로드
   **[⬇ buzzvil-ads-center-skill.skill 다운로드](https://github.com/ElleShin/-Buzzvil-ads-center-prototypekit/raw/main/buzzvil-ads-center-skill.skill)**
2. 파일 열기 → **"Add to library"** 클릭
3. Claude.ai → New Project → 라이브러리에서 해당 스킬 선택

### Step 2 — 레퍼런스 이미지 업로드 (권장)
실제 화면 이미지를 함께 업로드하면 Claude가 더 정확한 UI를 생성할 수 있어요.

1. 아래 링크로 폴더 이동 후 이미지 개별 다운로드
   **[📁 reference-images 폴더 바로가기](https://github.com/ElleShin/-Buzzvil-ads-center-prototypekit/tree/main/reference-images)**
2. Claude.ai → 해당 프로젝트 → **Files** → `+` 버튼 → 이미지 파일들 업로드

> 이미지 없이도 동작하지만, 실제 화면 레퍼런스가 있으면 결과물 품질이 높아집니다.

---

## 사용

프로젝트 내 Claude에게 자유롭게 요청하세요.

```
"광고 생성 페이지를 만들어줘. 광고의 타이틀, 예산, 집행 기간을 설정할 수 있어야 하고,
다음 단계에서는 광고 이미지 소재를 업로드하고 랜딩 URL 등을 입력한 뒤 심사를 신청할 수 있어야 해."

"광고머니 충전 관리 페이지를 만들어줘. 가상계좌를 충전할 수 있는 충전 버튼이 있고,
아래 목록에서는 충전, 소진, 환불, 환급 등의 내역을 볼 수 있어야 해."
```

디자인 토큰, 컴포넌트 패턴, 레이아웃이 자동으로 적용됩니다.

---

## 패키지 구성

```
buzzvil-ads-center-skill.skill
├── SKILL.md
└── references/
    ├── design-tokens.md       ← 색상·간격·타이포그래피
    ├── components.md          ← Button, Badge, Input, Modal, Table 등
    ├── layout-patterns.md     ← 페이지·사이드바·카드·테이블 레이아웃
    └── code-conventions.md    ← 파일 구조, 네이밍, 안티패턴

reference-images/              ← 실제 화면 레퍼런스 이미지 (별도 업로드)
├── README.md                  ← 이미지 업로드 가이드
└── (여기에 캡처 이미지를 넣어주세요)
```

---

## 스택

Next.js 15 · TypeScript · Tailwind CSS v4 · shadcn/ui

---

## 업데이트

`references/` 문서 수정 후 `.skill` 파일 재패키징

```bash
PYTHONPATH=. python3 scripts/package_skill.py /path/to/buzzvil-ads-center-skill/
```
