# Buzzvil Ads Center — Claude UI Skill

Claude AI가 Buzzvil Ads Center 디자인 시스템을 참조해 일관된 UI 코드를 생성하도록 돕는 Skill 패키지입니다.



## 설치

1. [`buzzvil-ads-center-skill.skill`](./buzzvil-ads-center-skill.skill) 다운로드
2. [claude.ai](https://claude.ai) → Projects → New Project
3. Project Knowledge → Add content → `.skill` 파일 업로드



## 사용

프로젝트 내 Claude에게 자유롭게 요청하세요.

```
"광고 생성 페이지를 만들어줘. 광고의 타이틀, 예산, 집행 기간을 설정할 수 있어야 하고, 다음 단계에서는 광고 이미지 소재를 업로드하고 랜딩 URL 등을 입력한 뒤 심사를 신청할 수 있어야 해."
"광고머니 충전 관리 페이지를 만들어줘. 가상계좌를 충전할 수 있는 충전 버튼이 있고, 아래 목록에서는 충전, 소진, 환불, 환급 등의 내역을 볼 수 있어야 해."
```

디자인 토큰, 컴포넌트 패턴, 레이아웃이 자동으로 적용됩니다.



## 패키지 구성

```
buzzvil-ads-center-skill.skill
├── SKILL.md
└── references/
    ├── design-tokens.md       ← 색상·간격·타이포그래피
    ├── components.md          ← Button, Badge, Input, Modal, Table 등
    ├── layout-patterns.md     ← 페이지·사이드바·카드·테이블 레이아웃
    └── code-conventions.md    ← 파일 구조, 네이밍, 안티패턴
```



## 스택

Next.js 15 · TypeScript · Tailwind CSS v4 · shadcn/ui



## 업데이트

`references/` 문서 수정 후 `.skill` 파일 재패키징

```bash
PYTHONPATH=. python3 scripts/package_skill.py /path/to/buzzvil-ads-center-skill/
```
