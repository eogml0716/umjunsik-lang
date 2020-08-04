# 엄랭

**주의: 이미 Umlang이라는 프로젝트가 있기때문에, 꼭 한글로만 표기해주세요.**
영문표기를 해야할때는 "Um. Junsik Lang" (or "Umjunsik-lang")이라고 표기해주세요.

엄랭은 세계 최초의 인물이름으로 만들어진 난해한 프로그래밍 언어입니다. 엄준식이 어떻게 인물 이름이냐고요? 그러게요ㅋㅋ 어떻게 엄준식이 어떻게 사람 이름이지ㅋㅋ "엄준식 사람이름인데요"

# 문법

엄랭은 "엄", "준", "식", "동탄" 네개의 키워드와 "!", ".", " ", "~", "ㅋ" 다섯개의 기호로 코드가 이루어집니다.
모든 프로그램은 "어떻게"로 시작하며, 항상 "이 사람이름이냐ㅋㅋ"로 끝나야 합니다.

## 자료형

정수: 온점, 반점의 갯수로 나타냅니다. 온점의 갯수만큼 1을 더하며, 반점의 갯수만큼 1을 뻅니다다.

```
... => 3
.. => 2
,, => -2
,,, => -3
.,., => 0
```

## 연산자

- 1 증가: `.`
- 1 감소: `,`
- 곱하기: " "(공백)
- 나누기: (미정)

## 변수

변수는 인덱싱(양의 정수)을 통해 접근하고 대입할 수 있습니다. 지정하지 않았을경우 모든 변수의 기본값은 0입니다.

### 대입(엄)

연음의 갯수번째 변수에 뒤에 오는 수를 대입합니다

```
어어엄 => 3번째 변수에 0 지정
어엄 => 2번째 변수에 0 지정
엄.. => 1번째 변수에 2 지정
어엄. => 2번째 변수에 1 지정
엄,,, => 1번째 변수에 -3 지정
```

### 사용(어)

연음의 갯수번째 변수를 불러옵니다

```
어 => 1번째 변수
어어 => 2번째 변수
어어어 => 3번째 변수
```

## 콘솔

### 식?

콘솔에서 정수를 입력받습니다.

```
엄식? => 콘솔을 입력받아서 1번째 변수에 대입한다.
어엄식? => 콘솔을 입력받아서 2번째 변수에 대입한다.
```

### 식!

콘솔에 정수를 출력합니다.

```tsx
식..! => 콘솔에 2 출력
식어! => 콘솔에 첫번째 변수 출력
```

### 식ㅋ

콘솔에 문자를 출력합니다. `식`과 `ㅋ`사이에 오는 정수를 유니코드 문자로 변환하여 콘솔에 출력합니다. `식`과 `ㅋ`사이에 정수가 주어지지 않으면 개행합니다(`식ㅋ` => `\n`)

```tsx
식........... ........ㅋ => 콘솔에 X 출력
```

## 기타

- 준: 라인이동(one-line 작성일경우 글자이동) `준.. => 2번째 줄(글자)로 이동`
- "화이팅!"은 프로그램의 종료를 의미합니다. return할 필요가 없어도 프로그램의 맨 마지막 줄에 삽입되어야 합니다.
- 확장자는 `.umm`입니다.
- One-line 작성은 `\n`을 `~`로 치환합니다. (예제: 구구단 참조)

# 예제

[위키를 참조해주세요](./wiki)

# History

- 20200626 0030 : 엄랭 공개
- 20200626 0855 : 엄랭 문서 완성
- 20200625 1256 : 엄랭 Deno 구현체 배포
- 20200702 : 엄랭v2
  1. 모든 콘솔 출력은 인라인
  1. `화이팅!` 후에 오는 문자열을 반환하며 프로그램이 종료
  1. 새 문법 추가: `식ㅋ`
