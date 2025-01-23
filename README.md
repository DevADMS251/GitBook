# 숫자 자료형

## **정수형 (`int`)**: 소수점이 없는 정수 값

* 예) `5`, `-3`, `42`
* 파이썬 3에서는 `int` 타입의 크기에 제한이 없으며, 메모리가 허용하는 한 매우 큰 수까지 표현할 수 있습니다.

{% code fullWidth="false" %}
```python
a = 10
b = 3
print(a + b)  # 덧셈: 13
print(a - b)  # 뺄셈: 7
print(a * b)  # 곱셈: 30
print(a / b)  # 나눗셈: 3.3333333333333335
print(a // b) # 몫: 3
print(a % b)  # 나머지: 1
print(a ** b) # 거듭제곱: 1000
```
{% endcode %}

***

## **부동소수점형 (`float`)**: 소수점을 포함한 실수 값

* 예: `3.14`, `-0.001`, `2.71828`
* 부동소수점 수는 근사값으로 저장되므로, 계산 시 오차가 발생할 수 있습니다.

```python
x = 3.14
y = 2.71
print(x + y)  # 덧셈: 5.85
print(x - y)  # 뺄셈: 0.4299999999999997
print(x * y)  # 곱셈: 8.5094
print(x / y)  # 나눗셈: 1.1594202898550725
```

***

## **복소수형 (`complex`)**: 실수부와 허수부로 구성된 복소수 값입니다.

* 예: `3 + 4j`, `-1 - 2j`
* 복소수는 수학적 계산에서 주로 사용되며, 파이썬에서는 `j`를 허수 단위로 사용합니다.

```python
z1 = 2 + 3j
z2 = 1 - 4j
print(z1 + z2)  # 덧셈: (3-1j)
print(z1 - z2)  # 뺄셈: (1+7j)
print(z1 * z2)  # 곱셈: (14-5j)
print(z1 / z2)  # 나눗셈: (-0.4117647058823529+0.7058823529411765j)
```

***

## 숫자형 관련 함수

*   **`abs()`**: 절댓값 반환

    ```python
    python복사편집print(abs(-5))  # 5
    ```
*   **`round()`**: 반올림

    ```python
    python복사편집print(round(3.14159, 2))  # 3.14
    ```
*   **`pow()`**: 거듭제곱

    ```python
    python복사편집print(pow(2, 3))  # 8
    ```
*   **`divmod()`**: 몫과 나머지 반환

    ```python
    python복사편집quotient, remainder = divmod(10, 3)
    print(quotient)   # 3
    print(remainder)  # 1
    ```

{% hint style="success" %}
-   부동소수점 연산은 근사값으로 처리되므로, 비교 시 오차가 발생할 수 있습니다.

    ```python
    python복사편집a = 0.1 + 0.2
    print(a == 0.3)  # False
    print(a)         # 0.30000000000000004
    ```
-   복소수는 실수부와 허수부로 구성되며, `j`를 허수 단위로 사용합니다.

    ```python
    python복사편집z = 3 + 4j
    print(z.real)  # 3.0
    print(z.imag)  # 4.0
    ```
{% endhint %}





