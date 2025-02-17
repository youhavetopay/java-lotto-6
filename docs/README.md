# 로또 게임

### 기능 설명

- 로또를 구매할 금액을 입력
    - 로또는 한장 당 1,000원
    - 금액은 1,000원 단위로 입력해야 함
    - 입력 가능 금액은 1,000 ~ 100,000 원
- 입력한 금액에 따른 랜덤 로또 번호를 생성
    - 하나의 로또 번호는 중복 없이 1 ~ 45 까지의 랜덤 숫자가 오름차순으로 정렬되어 있음
- 당첨 번호 및 보너스 번호를 입력
    - 당첨 번호는 공백 없이 , 으로 구분하여 1 ~ 45까지의 숫자 6개를 입력 ex) 1,2,3,4,5,6
    - 보너스 번호는 1 ~ 45 까지의 숫자 중 당첨 숫자와 중복되지 않은 숫자를 입력해야 함
- 생성된 로또들의 수익률을 계산
    - 5등 ~ 1등까지의 당첨 갯수를 알려줌
    - 수익률은 `(당첨금액 / 구입 금액) x 100%` 이고 소수점 둘째 자리에서 반올림됨  
      ex) 100.0%, 51.5%, 1,000,000.0%

### 실행 결과 예시

```
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
---
3개 일치 (5,000원) - 1개
4개 일치 (50,000원) - 0개
5개 일치 (1,500,000원) - 0개
5개 일치, 보너스 볼 일치 (30,000,000원) - 0개
6개 일치 (2,000,000,000원) - 0개
총 수익률은 62.5%입니다.
```

# 구현 기능 목록

- [x]  로또 구입 기능
    - [x]  구입 금액 입력 기능
        - 1,000 ~ 100,000 원 까지 (천 단위로 입력)
    - [x]  이 외 입력인 경우 에러 문구 띄우기
        - 에러 문구 띄우고 다시 입력 받기  
        ~~- 이전에 출력된 문구 지우기~~ -> 이거 생각보다 복잡해서 나중에 시간되면 해보기... [참고링크](https://www.delftstack.com/ko/howto/java/java-clear-console/)
    - [x]  구매 개수 출력 기능
    - [x]  구매한 로또 번호 출력 기능
        - 하나의 로또에는 중복 번호 X
        - 오름차순으로 정렬해서 보여주기
- [x]  당첨 번호 입력 기능
    - [x]  당첨 번호 입력 기능
        - 중복 X
        - 1 ~ 45 사이의 숫자
    - [x]  보너스 번호 입력 기능
        - 당첨 번호와 중복 X
        - 1 ~ 45 사이의 숫자
    - [x]  예외사항이 발생한 경우 안내메시지 출력 기능
        - 에러 문구 띄우고 당첨번호 다시 입력 받기
- [x]  당첨 통계 출력 기능
    - [x]  3개 일치
    - [x]  4개 일치
    - [x]  5개 일치
    - [x]  5개 일치 및 보너스 일치
    - [x]  6개 일치
    - [x]  총 수익률 출력
        - 소수점 둘째 자리에서 반올림하기 ex) 100.0%, 1,000,000%
        - 자릿수 구별 `,` 넣어주기

# 별도 요구사항

- [x]  함수 길이 15 라인 넘어가지 않게 하기
- [x]  Java Enum 적용하기
    - Enum 이랑 클래스 static final 로 하는거랑 차이점 공부해보기
- [x]  핵심 로직을 구현하는 코드와 UI를 담당하는 로직 분리하기
- [x]  indent 3이 넘지 않도록 하기