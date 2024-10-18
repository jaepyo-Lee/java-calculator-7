# java-calculator-precourse

## 아키텍처
**MVC (Model-View-Controller)** 패턴을 따릅니다.

>- **Model**: 이벤트를 처리하고, 변경된 데이터를 View에게 전달합니다.
>- **View**: Model로부터 받은 데이터를 이용해 화면을 구성합니다.
>- **Controller**: View로부터 발생한 이벤트를 Model에게 전달하고, Model로부터 받은 데이터를 View에게 반환합니다.

---

## 도메인별 기능 구현

### Model

#### Calculator
- 모델간의 계산을 처리를 위한 중간다리역할

#### Decryptor
- **입력값**: 문자열 (사용자 입력)
- **출력값**: 정수 배열 (입력값에서 파싱된 숫자 배열)

    - [ ] 구분자에 따라 숫자를 파싱.
    - [ ] 문자열 배열을 정수 배열로 변환.

#### Mathematician
- [ ] 정수 배열에 있는 숫자를 모두 더함.

#### NumberValidator
- [ ] 배열이 양수로만 이루어졌는지 검증.
    - 양수 이외의 값일경우 `IllegalArgumentException`을 발생.

#### Delimiter    Manager
- [ ] 구분자를 추가.
- [ ] 가지고있는 구분자를 통해 정규식패턴 구성.
- [ ] 커스텀 구분자를 없앤 문자열 반환.

---

### View

#### InputView
- [ ] 사용자 입력을 받음.
- [ ] 입력값이 빈 문자열(`""`)이면 `0`으로 수정.

#### OutputView
- [ ] 입력과 결과를 출력할 때 메시지 출력.

---

### Controller

#### CalculateController
- [ ] View와 Model간 데이터 전달을 처리.