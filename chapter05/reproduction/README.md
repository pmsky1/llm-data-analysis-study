# Chapter 05 재현용 코드

공식 수업 자료의 `src/data_loader.py`, `src/preprocessing.py`, `scripts/preprocess_data.py`를 기반으로 실습에 적용한 수정본입니다. 출처: https://github.com/GilbertMoon/llm-data-analysis-course

수정 사항은 pandas 문자열 타입 처리, 상품 범주 내부 공백 통일, 주문 월의 실제 결측 유지, Chapter 05 전용 Raw 입력과 출력 경로 지정입니다. 분석 규칙과 결과는 제출 Notebook에 설명했습니다.

## Notebook 실행

기존 수업 Python 3.12 가상환경을 사용합니다. 수업 저장소 `llm-data-analysis-course`와 제출 저장소 `llm-data-analysis-study`를 같은 부모 폴더에 두고, 수업 자료의 `practice/chapter05/data/raw/`에 전용 CSV 4개를 준비합니다. 공통 `data/raw/`와 구분합니다.

`chapter05.ipynb`는 이 폴더의 모듈과 스크립트를 사용합니다. 수업 저장소의 코드를 수정할 필요가 없습니다.

## 스크립트 단독 실행

이 폴더에서 실행합니다. 경로는 실제 위치로 지정합니다.

```bash
python scripts/preprocess_data.py --raw-dir /path/to/practice/chapter05/data/raw --output-dir /path/to/output/processed --report-dir /path/to/output/reports
```

원본 CSV는 읽기만 하며 출력 폴더는 별도로 지정합니다. Notebook은 단계별 처리와 함수·스크립트 CSV 전체 값 일치 및 원본 해시 보존을 검증합니다. 미연결 고객 2건·주문 2건·상품 26건과 날짜 변환 실패는 실습 결과로 유지됩니다.
