---
title: C# 삼항연산자(Ternary Operator)로 간결한 코딩을!
source: https://spaghetti-code.tistory.com/51
author:
  - "[[파이브 툴 플레이어]]"
published: 2019-05-14
created: 2024-11-14
description: 삼항연산자(?)란 피연산자의 갯수가 3개인 조건부 연산자를 의미합니다.
tags:
  - clippings
  - programming
---
삼항연산자(?)란 피연산자의 갯수가 3개인 조건부 연산자를 의미합니다. if else 구문을 한줄로 간단하게 표현할 수 있기 때문에 인라인 if(inline-if)라고도 합니다. if else 구문과 결과는 동일하지만 if else 구문은 여러줄로 작성되는 반면, 삼항연산자를 사용하면 한줄로 간단하게 표현할 수 있기 때문에 소스가 간결해집니다. 

다음의 코드를 통해 if else와 삼항연산자의 차이를 알아보도록 하겠습니다.

- if else

```
int number = 2;
bool isEven;

if (number % 2 == 0)
{
	isEven = true;
}
else 
{
	isEven = false;
}
```

- ? : 삼항연산자

```
int number = 2;
bool isEven;

isEven = (number % 2 == 0) ? true : false ;
```

삼항연산자는 일반적인 형식은 다음과 같습니다.

```
condition ? consequent : alternative
```

위에서 condition의 결과는 부울(bool)형태 즉, true 또는 false 이어야 합니다. condition의 결과가 true이면 consequent가 반환되고 false이면 alternative가 반환됩니다.

자료참조 : [MSDocs](https://docs.microsoft.com/ko-kr/dotnet/csharp/language-reference/operators/conditional-operator)