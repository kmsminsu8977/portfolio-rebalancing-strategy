# Portfolio Rebalancing Strategy

포트폴리오 리밸런싱 전략 프로젝트의 기본 연구 구조와 재현 가능한 baseline 산출물을 담은 저장소입니다.

**핵심 연구 질문**

> 고정 주기보다 밴드 기반 리밸런싱이 거래비용과 추적오차를 어떻게 절충하는가?

## 저장소 구조

```text
portfolio-rebalancing-strategy/
├── src/                         # baseline 계산 로직과 실행 엔트리포인트
├── data/sample/                 # 합성 샘플 입력 데이터
├── docs/                        # 방법론과 해석 기준
├── notebooks/                   # 실행 흐름을 보여주는 최소 노트북
├── outputs/tables/              # 재현 가능한 결과 CSV
├── presentation/                # 발표/보고서 초안
└── references/                  # 재작성 개념 노트와 참고문헌 메모
```

## 빠른 시작

```bash
python -m src.run_baseline
```

실행 결과는 `outputs/tables/baseline_results.csv`에 저장됩니다.

## 구현 범위

- 월별 수익률로 보유 비중을 drift시킨 뒤 목표비중 이탈이 밴드를 넘으면 리밸런싱한다.
- 회전율과 거래비용을 명시해 단순 성과 비교의 과대평가를 피한다.
- 수익률 표본은 구조 설명용 합성 데이터다.

## 주요 파일

- `src/rebalancing_baseline.py`: 목표 가중치와 허용 밴드가 거래 횟수, 비용, 누적성과에 미치는 영향을 계산한다.
- `data/sample/monthly_asset_returns.csv`: baseline 실행용 합성 입력값
- `docs/methodology.md`: 계산 절차, 입력/출력 정의, 해석상 주의점
- `outputs/tables/baseline_results.csv`: 현재 baseline 산출물

## 다음 확장 방향

- 실제 공개 데이터 또는 별도 수집 데이터 연결
- notebook 기반 탐색 분석 추가
- 차트와 표를 포함한 최종 보고서 작성
- 모델 검증, 민감도 분석, 비용/리스크 가정 보강
