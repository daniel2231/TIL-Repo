# 기본 포맷

>"프로그램은 우선 사람이 이해할 수 있어야 한다. 컴퓨터에서 실행되는가는 부가적인 문제다" <br>
> 도널드 커누스

## 스타일 가이드라인은 왜 필요한가?

- 작성자와 상관없이 어떠한 파일이든 다른 개발자가 작업할 수 있다.
- 에러가 훨씬 잘 보인다.

## 유용한 툴

- JSLint
- JSHint
- ESLint
- JSCS

> JSLint vs JSHint vs ESLint vs JSCS<br>
> [A Comparison of JavaScript Linting Tools](https://www.sitepoint.com/comparison-javascript-linting-tools/)

## 들여쓰기

- 들여쓰기는 거의 모든 언어에서 첫 번쨰로 결정하는 부분이다.
- 들여쓰기에 일관성이 없으면 코드를 빠르게 이해하기 힘들다.

**들여쓰기를 잘 슨 예**
```JavaScript
if (wl && wl.length) {
    for (i=0, 1=wl.lwngth; i < 1; ++i){
        p = wl[i];
        type = Y.Lang.type(r[p]);
        if (s.hasOwnProperty(p)) {
            if (merge && type == 'object') {
                Y.mix(r[p], s[p]);
            } else ir (ov || !(p in r)) {
                r[p] = s[p];
            }
        }
    }
}
```

### 들여쓰기 방식

- 탭을 이용한 들여쓰기
- 공백을 이용한 들여쓰기

## 문장 종료  
- 세미톨론을 입력하지 않아도 ASI(Automatic Semicolon Insertion) 메터니즘 덕분에 정상적으로 동작, 그러나 명시적으로 세미콜론을 넣기를 권장
- 세미콜론은 항상 사용하자

## 줄 길이
- 80자 제한

## 줄 바꿈
- 연산자 다음에 줄을 바꾸고 두 단계 들여쓰기를 한다.  

**예제**
```JavaScript
callAFunction(document, element, window, "some string value", true, 123,
        navigator);
```

- 변수를 다른 변수에 대입할 때 두 번째 줄의 들여쓰기는 첫번째 줄의 변수와 열을 맞춘다.
```javascript
var result = something + anotherThing + yetAnotherThing + somethingElse +
             anotherSomethingElse
```

## 빈 줄 넣기
- 여러개의 문단으로 구성되어 있으면 보기 편하다.
- 연관되지 않은 코드면 빈 줄을 줘서 가독성을 높힌다
- 메서드 사이
- 메서드 내 지역 변수와 첫 번째 문장 사이
- 한 줄 또는 여러 줄 주석 전
- 가독성을 높이기 위해 메서드 내에서 논리적으로 구분되는 곳
```javascript
if (wl && wl.length) {

    for (i=0, 1=wl.lwngth; i < 1; ++i){
        p = wl[i];
        type = Y.Lang.type(r[p]);

        if (s.hasOwnProperty(p)) {

            if (merge && type == 'object') {
                Y.mix(r[p], s[p]);
            } else ir (ov || !(p in r)) {
                r[p] = s[p];
            }
        }
    }
}
```

## 이름 규칙
> "컴퓨터 과학에서 가장 어려운 두 가지 문제는 캐시 무효화와 네이밍이다" <br>
> 필 칼튼

- camelCasing 표기법을 쓴다
- 일반적으로 자신이 사용하는 언어의 표준 라이브러리에서 따르는 이름 규칙을 사용해야 한다.

### 변수와 함수
- 변수명은 명사로
- 함수명은 동사로
- 변수명은 가능한 짧게, 이름만으로 데이터 타입을 알 수 있도록 한다
- 함수명과 메서드명의 첫 번째 단어는 동사로 시작해야 한다
- 보통 많이 쓰는 동사
    - can (불린 값을 반환)
    - has (불린 값을 반환)
    - is (불린 값을 반환)
    - get (불린 이외의 값 반환)
    - set (값을 저장)

