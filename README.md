# DeviceNet EPR 타임아웃 인터랙티브 학습 도구

TES CO., LTD. S/W1 팀을 위한 **DeviceNet EPR(Expected Packet Rate) 타임아웃** 개념 학습용 단일 HTML 파일 교육 도구입니다.

---

## 실행 방법

별도 설치나 빌드 과정 없이 바로 사용할 수 있습니다.

```
DeviceNet_EPR_Interactive.html  ← 이 파일을 웹 브라우저로 열기
```

Chrome, Edge, Firefox 등 현대적인 웹 브라우저에서 파일을 직접 열면 됩니다.

---

## 주요 기능

| 기능 | 설명 |
|------|------|
| EPR 슬라이더 | EPR 값을 10–200 ms 범위에서 조정 |
| PIT 슬라이더 | PIT 값을 5–300 ms 범위에서 조정 |
| 타임라인 시각화 | HTML5 Canvas로 폴 블록·PIT 갭·EPR 타임아웃 임계선 실시간 표시 |
| 판정 표시 | PIT/타임아웃 비율에 따라 녹색(안전) / 노란색(경고) / 빨간색(오류) |
| 시나리오 프리셋 | 안전 / 경고 / 위험 3가지 예시 값 즉시 적용 |

---

## EPR 타임아웃 계산 공식

```
EPR 타임아웃 = EPR × 4 ms
안전 임계값  = EPR 타임아웃 × 70%
```

---

## 파일 구성

```
DeviceNet_EPR_Interactive.html   # 인터랙티브 학습 도구 (단일 파일)
DeviceNet_EPR_Timeout_Guide.pdf  # 정적 참고 문서
CLAUDE.md                        # Claude Code 프로젝트 지침
.gitignore                       # Git 제외 파일 설정
```

---

## 기술 스택

- HTML5 / CSS3 / Vanilla JavaScript (외부 의존성 없음)
- HTML5 Canvas API (타임라인 시각화)
