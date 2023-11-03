# 기능 요구 사항 목록

### 로또 정보 입력 및 출력

- [ ] 로또 구입 금액 입력시 구입 금액에 해당하는 갯수의 만큼 로또 갯수 반환

  - 로또 1장의 가격 : 1,000원
  - [ ] _예외) 구입 금액 입력값이 로또 1장의 가격 단위가 아니면 프로그램 종료_

- [ ] 로또 각 장에 대한 배열 생성(발행)
  - 로또 번호 : 숫자 범위 1~45에 해당하는 정수
  - 1개의 로또를 발행시 중복되지 않는 6개의 숫자 생성
- [ ] 발행한 로또 번호 출력
  - 로또 번호는 오름차순으로 정렬
- [ ] 당첨 번호 입력
- [ ] 보너스 번호 입력

### 당첨 통계 및 수익률 계산

- [ ] 당첨 기준에 따른 1~5등 판단 및 금액 반환 (당첨 기준 / 당첨 금액)
  - [ ] 1등: 6개 번호 일치 / 2,000,000,000원
  - [ ] 2등: 5개 번호 + 보너스 번호 일치 / 30,000,000원
  - [ ] 3등: 5개 번호 일치 / 1,500,000원
  - [ ] 4등: 4개 번호 일치 / 50,000원
  - [ ] 5등: 3개 번호 일치 / 5,000원
- [ ] 사용자가 구매한 로또 번호(각 장당)와 당첨 번호를 비교
- [ ] 수익률 계산
- [ ] 수익률은 소수점 둘째 자리에서 반올림
      예시) 100.0%, 51.5%, 1,000,000.0%

**실행 결과 예시**
구입금액을 입력해 주세요.
8000

8개를 구매했습니다.
[8, 21, 23, 41, 42, 43]
[3, 5, 11, 16, 32, 38]
[7, 11, 16, 35, 36, 44]
[1, 8, 11, 31, 41, 42]
[13, 14, 16, 38, 42, 45]
[7, 11, 30, 40, 42, 43]
[2, 13, 22, 32, 38, 45]
[1, 3, 5, 14, 22, 45]

당첨 번호를 입력해 주세요.
1,2,3,4,5,6

보너스 번호를 입력해 주세요.
7

당첨 통계
"---"(실제 출력시 ""(큰따옴표)삭제)
3개 일치 (5,000원) - 1개
4개 일치 (50,000원) - 0개
5개 일치 (1,500,000원) - 0개
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
6개 일치 (2,000,000,000원) - 0개
총 수익률은 62.5%입니다.

_**예외 상황 시 에러 문구 출력**
에러 문구는 "[ERROR]"로 시작
예시) [ERROR] 로또 번호는 1부터 45 사이의 숫자여야 합니다.
사용자가 잘못된 값을 입력할 경우 throw문을 사용해 예외를 발생. 그런 다음, "[ERROR]"로 시작하는 에러 메시지를 출력하고 해당 부분부터 입력을 다시 받음
예시) [ERROR] 숫자가 잘못된 형식입니다._