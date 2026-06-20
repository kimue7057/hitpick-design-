# Hitpick Project Context

이 문서는 새 채팅이나 새 작업자가 현재 Hitpick 디자인 프로젝트의 진행 상태를 빠르게 이해하기 위한 핸드오프 문서입니다.

## 1. Project Goal

현재 Hitpick의 구현 방향을 완전히 뒤엎지 않고,
기존 서비스 톤을 최대한 유지한 상태에서
서비스 인식이 `크라우드펀딩/투자형 플랫폼`에만 머무르지 않도록
`콘텐츠 IP 기반 수익화 매칭 플랫폼`으로 읽히게 만드는 디자인 방향을 검토 중입니다.

## 2. Important Direction

- 기존 Hitpick의 시각적 톤은 최대한 유지합니다.
- 흰 배경, 보라 포인트, 둥근 카드, 현재 헤더/검색/카테고리 구조를 살립니다.
- 개발자 부담이 커질 정도의 대규모 기능 추가는 하지 않습니다.
- 디자인 검토가 우선이며, 이 레포는 현재 `디자인 시안 저장소` 역할입니다.

## 3. Confirmed Decisions

- 메인 화면은 기존 디자인을 살린 보수적 방향으로 수정합니다.
- 첫인상은 `투자 모집`보다 `콘텐츠 IP`, `크리에이터 확보`, `광고/PPL`, `수익화 가능성`이 먼저 읽히게 합니다.
- `배급` 관련 강조는 현재 단계에서 제외합니다.
- 프로젝트 상세 상단도 기존 참여 구조는 유지하되, 정보 우선순위를 더 읽기 쉽게 정리하는 방향으로 갑니다.
- 새 화면은 만들 수 있지만, 새로운 복잡한 기능 엔진을 전제로 하면 안 됩니다.

## 4. What To Avoid

- 기존 Hitpick 디자인 언어를 완전히 버리는 전면 리디자인
- 관리자/백엔드/DB/API 설계 문서를 이 레포에서 과도하게 확장하는 것
- 실제 제품 코드인 것처럼 과한 프레임워크 구조를 먼저 만드는 것
- 아직 합의되지 않은 `배급 중심 메시지`를 다시 앞세우는 것

## 5. Current Deliverables

- `index.html`
  - 레포 진입용 안내 페이지
- `mockups/home-v2-existing-tone.html`
  - 기존 Hitpick 톤을 유지한 메인 화면 시안
- `mockups/project-detail-v1-existing-tone.html`
  - 기존 Hitpick 톤을 유지한 프로젝트 상세 상단 시안

모든 mockup 파일은 다른 노트북에서도 바로 열 수 있도록 self-contained HTML 형태로 저장되어 있습니다.

## 6. Design Intent Per Screen

### Home

- 기존 헤더/검색/카테고리 구조 유지
- 메인 배너에 실제 예시 비주얼 삽입
- 우측 카드에는 프로젝트/사용자 관점의 요약 정보 배치
- 프로젝트 카드는 `시청층`, `광고 포인트`, `확장성`을 먼저 보여주고
  진행률/목표금액은 하단 보조 정보로 유지

### Project Detail

- 좌측: 메인 비주얼 + 썸네일 갤러리
- 우측: 제목, 크리에이터, 핵심 태그, 시청층/광고 포인트/확장성
- 참여 정보와 CTA는 유지하되, 맥락 설명 뒤에 오도록 재배치

## 7. Recommended Next Steps

우선순위는 아래 순서가 좋습니다.

1. 메인 화면 문구/간격/카드 디테일 정리
2. 프로젝트 리스트 페이지 시안 정리
3. 프로젝트 상세 하단 섹션 정리
4. 공통 컴포넌트화 가능한 부분 식별
5. 이후 실제 제품 프론트엔드 레포로 옮길 범위 결정

## 8. Working Rules For Future Chats

새 채팅은 아래 원칙으로 이어가면 됩니다.

- 먼저 `README.md`와 `PROJECT_CONTEXT.md`를 읽습니다.
- 그다음 `mockups/home-v2-existing-tone.html`과
  `mockups/project-detail-v1-existing-tone.html`을 확인합니다.
- 이미 합의된 방향을 깨지 않는 선에서만 수정합니다.
- 방향 변경이 필요하면 먼저 `기존 톤 유지 여부`, `개발 부담 증가 여부`를 확인합니다.

## 9. Suggested Starter Prompt For A New Chat

아래 문장을 새 채팅 첫 메시지로 쓰면 이해가 빠릅니다.

```text
이 레포는 Hitpick 디자인 시안 프로젝트입니다.
먼저 README.md와 PROJECT_CONTEXT.md를 읽고,
mockups/home-v2-existing-tone.html 과 mockups/project-detail-v1-existing-tone.html을 확인한 뒤,
현재 합의된 방향을 유지하면서 다음 작업을 이어가 주세요.

중요 조건:
- 기존 Hitpick 디자인 톤 최대한 유지
- 개발자 부담이 커지는 큰 기능 추가 금지
- 현재는 배급 강조 제외
- 콘텐츠 IP / 크리에이터 / 광고-PPL / 수익화 가능성이 먼저 읽히게 유지
```
