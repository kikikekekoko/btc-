# ₿ 가계부 — BTC 자산 추적기

원화(KRW)로 수입/지출을 기록하면 BTC(sats)로 자동 변환해주는 개인 가계부 앱.

## 기능

- 📅 **달력 뷰** — 일별 수입/지출을 한눈에 확인
- 💰 **원화 → sats 자동 변환** — CoinGecko API로 일별 BTC 시세 반영
- 📊 **카테고리 분석** — 지출 항목별 비율 차트
- 📈 **자산 비교** — 전월 대비, 연초 대비, 월별 추이 차트
- 📱 **PWA** — 홈화면에 추가하면 앱처럼 사용 가능
- 🔒 **로컬 저장** — 모든 데이터는 브라우저 IndexedDB에 저장 (서버 전송 없음)

## 사용법

### GitHub Pages로 호스팅

1. 이 저장소를 GitHub에 Push
2. **Settings → Pages → Source**를 `main` 브랜치로 설정
3. `https://아이디.github.io/저장소명/` 으로 접속

### 앱 설치

| 기기 | 방법 |
|------|------|
| iPhone | Safari → 공유(□↑) → 홈 화면에 추가 |
| Android | Chrome → ⋮ 메뉴 → 홈 화면에 추가 |
| PC | Chrome → 주소창 설치 아이콘(⊕) 클릭 |

## BTC 시세

- CoinGecko → Blockchain.info → CoinCap 순서로 3중 백업
- 실패 시 상단 가격을 탭하여 수동 입력 가능

## 파일 구조

```
├── index.html       ← 앱 본체 (HTML/CSS/JS 올인원)
├── manifest.json    ← PWA 설정
├── sw.js            ← 서비스 워커 (오프라인 지원)
├── icons/
│   ├── icon-192.png
│   └── icon-512.png
└── README.md
```

## 기술 스택

Vanilla JS · IndexedDB · CoinGecko API · PWA · GitHub Pages
