# 📘 자바의 신 VOL.1 – 7장: 여러 데이터를 하나에 넣을 수는 없을까요?

---

## 1. 배열의 기본 개념

- 배열은 같은 타입의 데이터를 연속된 메모리 공간에 저장하는 자료 구조
- 선언 시 크기 지정 필수
- 크기는 변경 불가 → 컬렉션(Collection)으로 보완
- 인덱스는 0부터 시작

---

## 2. 배열의 초기화 및 기본값

- 크기만 지정하면 각 요소는 기본값으로 초기화됨
    - 숫자형 → 0
    - boolean → false
    - 참조형 → null
- 지역 변수는 초기화 필수지만, 지역 변수 배열은 크기 지정 시 기본값 자동 할당

---

## 3. 배열의 출력 및 순회

- 배열 자체를 출력하면 사람이 읽을 수 있는 값이 아닌 내부 구조 정보가 출력됨
- 출력 형태는 배열의 타입에 따라 다름

### ● 참조형 배열 출력
- 형식: `[L클래스이름;@해시코드`
    - `[` : 배열임을 의미
    - `L` : 참조형 객체
    - `@해시코드` : 해당 배열 인스턴스의 고유 주소

### ● 기본형 배열 출력
- 형식: `[타입문자@해시코드`
    - `[` : 배열
    - 타입문자: 기본형을 나타내는 한 글자 식별자
        - `B` - byte
        - `S` - short
        - `I` - int
        - `F` - float
        - `D` - double
        - `C` - char
        - `J` - long (`L`이 참조형에 쓰여서 `J`로 대체됨)
        - `Z` - boolean (`B`는 byte에 뺏겨서 울며 겨자 먹기로 `Z` 사용)

> long과 boolean이 이름값을 못 챙긴 이유는 이미 자리를 뺏겨서.  
> 그래서 long은 `J`, boolean은 `Z`를 억지로(?) 쓴다. 울며 겨자 먹기로.

### ● 배열 순회 방법
- 전통적인 for문 → 인덱스 기반 접근에 유용
- 향상된 for문 (for-each) → 값 순회에 깔끔함

---

## 4. 다차원 배열

- 선언: `int[][] arr = new int[행][열];`
- 메모리는 행 단위로 분리되어 저장됨
