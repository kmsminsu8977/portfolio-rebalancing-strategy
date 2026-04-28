# 발표 초안

## 1. 문제 정의

고정 주기보다 밴드 기반 리밸런싱이 거래비용과 추적오차를 어떻게 절충하는가?

## 2. 데이터와 가정

- 합성 샘플 데이터: `data/sample/monthly_asset_returns.csv`
- 재현 가능한 baseline 실행을 우선 구성

## 3. 방법

목표 가중치와 허용 밴드가 거래 횟수, 비용, 누적성과에 미치는 영향을 계산한다.

## 4. 현재 산출물

- 실행 스크립트: `python -m src.run_baseline`
- 결과 표: `outputs/tables/baseline_results.csv`

## 5. 후속 작업

- 실제 데이터 연결
- 민감도 분석
- 차트/보고서 산출
- 프로젝트별 상세 검증
