# AI Links — AI 서비스 링크 모음 사이트

> AI 및 개발 관련 서비스를 카테고리별로 정리한 단일 HTML 사이트  
> **배포 URL:** https://iwishkim.github.io/myappsite/

---

## 제작 과정

### 1단계 — 요구사항 정의
- 카드 형식의 UI
- 상단 메뉴(대 카테고리) + 사이드 메뉴(소 카테고리) 구조
- 초기 요청 서비스: Claude, Gemini, Grok, Genspark, Whisk, SUNO, Lovable, V0, Hugging Face, GitHub
- 추가 요청: 기타 AI 관련 사이트 자동 추가

### 2단계 — 사이트 구현 (`index.html`)
별도 프레임워크 없이 **순수 HTML + CSS + JavaScript** 단일 파일로 구현

| 구성 요소 | 내용 |
|---|---|
| 레이아웃 | 고정 헤더 + 좌측 고정 사이드바 + 메인 카드 그리드 |
| 상호작용 | 카테고리 클릭 시 카드·사이드바 동적 필터링 |
| 카드 기능 | 클릭 또는 "바로가기 →" 버튼으로 새 탭 오픈 |
| 디자인 | 보라색 계열 포인트, 호버 시 카드 부상 효과 |

### 3단계 — 브라우저 검증
Python HTTP 서버 + Playwright 헤드리스 브라우저로 4개 화면 자동 스크린샷 캡처 후 정상 동작 확인

### 4단계 — GitHub 배포
```
git init
git add index.html .gitignore
git commit
gh repo create myappsite --public --push
gh api repos/iwishkim/myappsite/pages  # GitHub Pages 활성화
```

---

## 수록 서비스 (총 29개)

### AI 어시스턴트 (7개)
| 서비스 | 분류 | URL |
|---|---|---|
| Claude | AI 챗봇 | https://claude.ai |
| ChatGPT | AI 챗봇 | https://chatgpt.com |
| Gemini | AI 챗봇 | https://gemini.google.com |
| Grok | AI 챗봇 | https://grok.com |
| Copilot | AI 챗봇 | https://copilot.microsoft.com |
| Perplexity | AI 검색 | https://www.perplexity.ai |
| Genspark | AI 검색 | https://www.genspark.ai |

### AI 크리에이티브 (11개)
| 서비스 | 분류 | URL |
|---|---|---|
| Whisk | 이미지 생성 | https://labs.google/fx/tools/whisk |
| Midjourney | 이미지 생성 | https://www.midjourney.com |
| Ideogram | 이미지 생성 | https://ideogram.ai |
| Leonardo AI | 이미지 생성 | https://leonardo.ai |
| Stable Diffusion | 이미지 생성 | https://stability.ai |
| SUNO | 음악 생성 | https://suno.com |
| Udio | 음악 생성 | https://www.udio.com |
| Runway | 영상 생성 | https://runwayml.com |
| Pika | 영상 생성 | https://pika.art |
| Kling AI | 영상 생성 | https://klingai.com |
| ElevenLabs | AI 음성 | https://elevenlabs.io |

### AI 개발 도구 (6개)
| 서비스 | 분류 | URL |
|---|---|---|
| Lovable | AI 빌더 | https://lovable.dev |
| V0 | AI 빌더 | https://v0.dev |
| Bolt.new | AI 빌더 | https://bolt.new |
| Cursor | AI 코딩 | https://cursor.com |
| Replit | AI 코딩 | https://replit.com |
| GitHub Copilot | AI 코딩 | https://github.com/features/copilot |

### 개발자 플랫폼 (5개)
| 서비스 | 분류 | URL |
|---|---|---|
| Hugging Face | 모델 허브 | https://huggingface.co |
| GitHub | 코드 저장소 | https://github.com |
| Vercel | 배포 플랫폼 | https://vercel.com |
| Anthropic | AI 연구 | https://www.anthropic.com |
| OpenAI | AI 연구 | https://openai.com |

---

## 파일 구조

```
myappsite/
├── index.html   # 전체 사이트 (HTML + CSS + JS 단일 파일)
├── .gitignore
└── README.md
```

---

## 메뉴 구조

```
[상단 - 대 카테고리]
전체 | AI 어시스턴트 | AI 크리에이티브 | AI 개발 도구 | 개발자 플랫폼

[사이드 - 소 카테고리] (선택된 대 카테고리에 따라 동적 변경)
전체 / AI 챗봇 / AI 검색 / 이미지 생성 / 음악 생성 / 영상 생성 / AI 음성 / AI 빌더 / AI 코딩 / 모델 허브 / 코드 저장소 / 배포 플랫폼 / AI 연구
```
