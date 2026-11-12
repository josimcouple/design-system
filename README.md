# 루미너스 블루 디자인 시스템

맑고 또렷한, 내가 만드는 모든 앱과 웹의 공통 규칙. 밝은 푸른 회백색 바탕에 선명한 파랑 한 가지만 포인트로 쓴다.

원본: [루미너스 블루 디자인 시스템 아티팩트](https://claude.ai/artifact/9WjzwMTvMbvuDS7m3BW5M2)

## 구조

규칙은 **공통 층**과 **플랫폼 층** 두 단계로 나눈다.

```
design-system/
├─ tokens/tokens.json      # 공통: 색, 글자, 간격, 모서리, 크기 토큰
├─ principles/             # 공통: 원칙, 색·글자 사용법, 문구
├─ components/             # 공통: 컴포넌트 규칙 (플랫폼별 동작은 표시)
└─ platforms/
   ├─ mobile.md            # 모바일 웹앱 전용 규칙
   └─ desktop.md           # PC 앱 전용 규칙 (아직 미정)
```

- **공통 층**은 모바일과 PC가 똑같이 따른다.
- **플랫폼 층**은 입력 방식(터치 / 마우스·키보드), 레이아웃, 팝업 모양처럼 기기에 따라 달라지는 것만 적는다.
- 플랫폼 문서에 없는 내용은 공통 규칙을 따른다.
- 특정 프로그램에만 필요한 예외는 이 저장소가 아니라 그 프로그램 저장소에 적는다.

## 문서 목록

| 문서 | 내용 |
| --- | --- |
| [principles/README.md](principles/README.md) | 원칙 4가지 |
| [principles/color.md](principles/color.md) | 색 토큰과 쓰는 곳 |
| [principles/typography.md](principles/typography.md) | 글꼴, 굵기, 글자 스타일 |
| [principles/writing.md](principles/writing.md) | 문구 규칙 |
| [components/buttons.md](components/buttons.md) | 버튼 4종 |
| [components/popups.md](components/popups.md) | 팝업 3종 |
| [components/inputs.md](components/inputs.md) | 입력창 |
| [components/choices.md](components/choices.md) | 선택지가 많을 때 |
| [components/amounts.md](components/amounts.md) | 금액 표시 |
| [platforms/mobile.md](platforms/mobile.md) | 모바일 전용 규칙 |
| [platforms/desktop.md](platforms/desktop.md) | PC 전용 규칙 (미정) |

## Claude Code에서 쓰는 법

각 프로그램 저장소의 `CLAUDE.md`에 아래를 넣는다. 플랫폼 줄은 그 프로그램에 맞는 것 하나만 남긴다.

```
## 디자인 규칙
- UI는 루미너스 블루 디자인 시스템을 따른다 (색·글자·간격·모서리는 토큰 이름으로만 사용).
- 플랫폼: 모바일 (platforms/mobile.md) / PC (platforms/desktop.md)
- 버튼은 메인/보조/텍스트/삭제 4종만, 팝업은 확인창/하단 시트/토스트 3종만 사용한다.
- 새 버튼·팝업 모양을 만들지 말고 기존 공통 컴포넌트를 재사용한다.
- 문구는 해요체, 버튼은 동사형("저장", "내역 추가").
```
