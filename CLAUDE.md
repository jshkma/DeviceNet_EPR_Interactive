# CLAUDE.md

이 파일은 이 저장소에서 작업할 때 Claude Code(claude.ai/code)에 지침을 제공합니다.

## 프로젝트 개요

TES CO., LTD. S/W1 팀을 위해 제작된 **DeviceNet EPR(Expected Packet Rate) 타임아웃** 학습용 단일 HTML 파일 교육 도구입니다. UI는 전체 한국어로 구성되어 있습니다.

**실행 방법:** `DeviceNet_EPR_Interactive.html`을 현대적인 웹 브라우저에서 직접 열면 됩니다. 별도의 빌드 과정이나 외부 의존성이 없습니다.

## 아키텍처

모든 코드는 `DeviceNet_EPR_Interactive.html` 단일 파일 안에 HTML 구조, 내장 CSS, Vanilla JavaScript로 구성되어 있습니다.

**핵심 로직 (JavaScript):**
- EPR 타임아웃 공식: `EPR × 4 ms`
- 안전 임계값: EPR 타임아웃의 70%
- 판정: PIT 대비 타임아웃 비율에 따라 녹색(안전) / 노란색(경고) / 빨간색(오류)
- HTML5 Canvas API를 통한 타임라인 시각화 — 슬라이더 입력 시마다 재렌더링

**주요 인터랙티브 요소:**
- 슬라이더 2개: EPR 값(10–200 ms) 및 PIT(5–300 ms) 조정
- 폴 블록, PIT 갭, EPR 타임아웃 임계선을 표시하는 Canvas 타임라인 다이어그램
- 실시간 지표 표시(타임아웃, 마진, PIT 비율)
- 시나리오 프리셋 버튼 (안전 / 경고 / 위험)

**보조 참고 자료:** `DeviceNet_EPR_Timeout_Guide.pdf` — HTML에서 사용하지 않는 정적 참고 문서.
