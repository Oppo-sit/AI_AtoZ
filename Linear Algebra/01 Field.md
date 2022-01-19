# 01 Field

## 1. Vector의 정의

- 크기와 방향이 있는 것(물리)
- \[1 2 3 4\](수학)
- 위의 정의보다 더 자세한 정의를 알기 위해서는 ‘Field’와 ‘Vector space’에 대한 정의를 먼저 알아야 함

## 2. Field

- 두 개의 연산(+, · )을 가진 집합
    
    <aside>
    💡 이 때, +, ·  연산은 단순한 사칙연산의 결과가 아닐 수 있으며, 즉 우리가 아는 연산이 아닐 수 있음
    
    </aside>
    
- 성질 ( Field가 되기 위한 조건)
    - Closed : 연산 결과가 해당 Field와 같은 집합에 속해있어야 한다.
    - a + b = b + a, a · b = b · a (교환법칙)
    - (a + b) + c = a + (b + c), (a · b) · c = a · (b · c) (결합법칙)
    - “Additive identity(0 + a = 0)”와 “multiplicative identity(1 · a = a)”의 존재 (항등원)
    - “Additive inverse(a + (-a) = 0)”와 “multiplicative inverse(a · 1/a = 1)”의 존재 (역원)
    - a · (b + c) = ab + ac (분배법칙)
    - 대수학의 목적은 방정식을 해결하는 것인데, 방정식을 구하는 과정에서 위 성질들은 필수적으로 이용해야 한다.
- Example
    - R(실수), C(유리수), Q(복소수) 집합은 field에 속한다
    - Field는 infinite할 수 있고, finite할 수 있다
        - $\{a+b\sqrt{2}|{a,b} \in Q\}$의 경우, field에 속하며, 집합에 속한 원소의 개수가 무한하므로 infinite field
        - 어떤 수를 2로 나눈 나머지에 대한 field $Z_2 = \{0, 1\}$의 경우에는 field에 속하지만 원소가 0과 1뿐이기 때문에 finite field
            
            <aside>
            💡 $Z_2$ field는 정의역과 공역이 전부 0, 1이며, product 연산과 multiplt 연산 이후에도 2로 나누어 나머지를 구하는 방식이기 떄문에, +, ·의 결과가 기존의 사칙연산과 다르다
            
            in $Z_2$, 1+1 = ‘0’ (2%2 = 0)
            
            </aside>
            
    - Field에 속하지 않는 경우
        - $Z_4 = \{0, 1, 2, 3\}$에서, 2의 역원을 찾아보자
        - 2 · 0 = 0, 2 · 1 = 2, 2 · 2 = 0, 2 · 3 = 2
        - 역원의 정의 : 2 · a = 1, 그러나 위 정의역에서는 2의 역원이 존재하지 않는다
            
            →Not a field
            
<<<<<<< HEAD:Linear Algebra/01 Field.md
        - 이 외에도 자연수, 정수도 field에 속하지 않음
=======
        - 이 외에도 자연수, 정수도 field에 속하지 않음

## 3. Vector Space

- 벡터들의 집합으로, +(element-wise product of vector), · (scalar dot)을 가짐
- 성질 (field와 유사하지만, +, ·의 의미가 다르므로 유의)
    - Closed
    - x + y = y + x (덧셈의 교환법칙), (x + y) + z = x + (y + z) (덧셈의 결합법칙)
    - 벡터 x에 대해 x + 0 = x를 만족하는 0(영벡터)가 존재 → $∃ 0\in V s.t. x+0 = x$
    - 모든 벡터 x에 대해 1 · x = x를 만족하는 벡터 x가 존재 → $∀ x \in V s.t. 1 · x = x$
    - (a · b) · x = a · (b · x) (곱셈의 결합법칙, a, b는 scalar value로, a · b의 · 는 field의 연산자)
    - a(x+y) = ax + ay (분배법칙, 이 때 a는 scalar value)
    - (a+b)x = ax + bx (분배법칙, 이 때 a, b는 scalar value)
    - 벡터 안의 값들은 F(field)안에 존재해야 함
- Vector는 vector space에 속하는 원소이며, Field는 Field에 속하는 원소
    - 벡터 간의 연산은 vector space의 연산이지만, scalar operation은 Field 간의 연산
    - 벡터와 유사한 ‘tuple’이 있는데, 이는 단순히 scalar를 나열한 것 (1, 2, 3, 4)
- Example : 중요한 것만
    - 행렬도 벡터에 속해있다
        - 정의 : $M_{m \times n}(F) = \{[a_{i,j}|a_{i,j} \in F\}$
        - a는 Field에 속하는 스칼라 값이며, 이러한 값들이 m x n개 만큼 존재
        - $\begin{pmatrix}
          2 & 3 & 4 \\
          5 & 6 & 7
        \end{pmatrix} \in M_{2 \times 3}(F)$ 와 같이 2 X 3 행렬은 vector space에 속한다
        - 영벡터의 존재
            
            $\begin{pmatrix}
            0 & 0 & 0 \\
            0 & 0 & 0
            \end{pmatrix}$와 같이 행렬은 영벡터가 존재한다.
>>>>>>> 81db1ec0f3e717a47ffa3c33ecc399a02a7a2cd2:Linear Algebra/01 Field, Vector Space.md
