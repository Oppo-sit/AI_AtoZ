# 02 Vector Space

## 1. Vector Space

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

## 2. Examples of vector space

- 1주차 내용
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
            
- 2주차 : 이전 vector space의 예시에 이어서 예시 진행
    
    1) 정의역 : [0, 1] (0~1). 공역이 R(실수)인 벡터(함수)들의 집합
    
    ![Untitled](02%20Vector%20Space%20ce86b2e8af064e9f8159762808327a99/Untitled.png)
    
    - 위 함수들은 vector space에 속한다
    - 위 조건을 만족하는 영벡터는? x=0 (상수함수)
    - 위 함수 그래프의 역원은 위 함수를 x축 대칭한 함수
    
    2) 유한차수의 다항식들의 집합 V=P(R)
    
    - P는 polynomial, R은 다항식의 요소가 R(실수 필드)에 속해있음을 의미
    - $f(x) = a_{n}x^{n} +  a_{n-1}x^{n-1} +  a_{0} \in{V}$
        
        $g(x) = b_{n}x^{n} +  b_{n-1}x^{n-1} +  b_{0} \in{V}$
        
    - f(x)와 g(x)는 $f(x) + g(x) \in{V}, cf(x) \in{V}$를 만족한다.
    
    3) 2차원 평면의 한 점 $S = \{(a_1, a_2)|a_1, a_2 \in{R}\}$에 대한 +와 ·의 정의는 다음과 같음
    
    - $(a_1, a_2) + (b_1, b_2) = (a_1+b_1, a_2-b_2)$
        
        $c(a_1, a_2) = (ca_1, ca_2)$
        
    - S는 vector space가 될 수 있을까? → X
        - 교환법칙 : $(a_1+b_1, a_2-b_2) \neq (b_1+a_1, b_2-a_2)$
        - 결합법칙 : $\{(a_1, a_2) + (b_1, b_2)\} + (c_1, c_2) 
        \\= (a_1+b_1, a_2 - b_2) + (c_1, c_2)
        \\= (a_1+b_1+c_1, a_2+b_2-c_2)
        \\(a_1, a_2) + \{(b_1, b_2) + (c_1, c_2)\}
        \\= (a_1, a_2) + (b_1 + c_1, b_2 -c_2)
        \\= (a_1+b_1+c_1, a_2-b_2+c_2)$
            
            위 식의 전개에 따라 교환법칙과 결합법칙은 성립하지 않는다
            
    
    4) 2차원 평면의 한 점 $S = \{(a_1, a_2)|a_1, a_2 \in{R}\}$에 대한 +와 ·의 정의는 다음과 같음
    
    - $(a_1, a_2) + (b_1, b_2) = (a_1+b_1, 0)$
        
        $c(a_1, a_2) = (ca_1, 0)$
        
    - S는 vector space가 될 수 있을까? → X
        - $∃ 0\in V s.t. x+0 = x$
            
            → (a, b) + (0, 0) = (a, 0), 영벡터가 존재할 경우 항상 x+0 = x여야 하는데, b+0 = 0
            
            $∀ x \in V s.t. 1 · x = x$
            
            → 1·(3, 5) = (3, 0), 1·5 = 0 ≠ 5
            
            본 space는 두 성질을 만족하지 못함
            
    

## 3. Theorem, Corollary of Vector Space

- Vector space의 정리와 Corollary를 정리
    
    <aside>
    💡 Theorem은 정리, corollary는 정리로부터 유도되는 명제를 의미
    
    </aside>
    
- Theorem 1 Cancellation Law : 같은 element는 제거
    - $∀ x, y, z \in{V}
    \\x+z=y+z => x=y$
    - Proof
        
        $(x+z)+(-z)=(y+z)+(-z)$ 
        
        $x+\{z+(-z)\}=y+\{z+(-z)\}$ (결합법칙)
        
        $x+0=y+0
        \\\therefore{x=y}$ 
        
- Corollary from cancellation law
    - ‘0’ is unique
        
        → 서로 다른 ‘0’과 ‘0`’를 가정,
        
        $0+x = 0` +x$  에서 cancellation law에 의해 x를 지울 수 있다.
        
        $\therefore0=0`$ 
        
    - 덧셈의 역원 또한 unique
        
        → x의 두 역원 a, b를 가정
        
        $x+a=0, x+b=0
        \\x+a=x+b$ 
        
        Cancellation law에 의해, $a=b$
        
- Theorem 2
    - $\forall{x}\in{V}, 0\cdot{x}=0$
        - 좌변의 0은 scalar, 우변의 0은 영벡터를 의미
        - Proof
            
            $0\cdot{x}=(0+0)\cdot{x} = 0\cdot{x}+0\cdot{x}$
            
            Cancellation law에 의해, 양변의 $0\cdot{x}$은 지워진다.
            
            $\therefore0\cdot{x}=0$
            
    - $\forall{a}\in{F}, a\cdot{0}=0$
        - 좌우변의 0은 모두 영벡터를 의미
        - Proof
            
            $a\cdot{0}=a\cdot(0+0) = a\cdot{0}+a\cdot{0}$
            
            Cancellation law에 의해, 양변의 $a\cdot{0}$은 지워진다.
            
            $\therefore{a}\cdot{0}=0$
            
    - $\forall{x}\in{V}, \forall{a}\in{F}
    \\ (-a)\cdot{x}=-(a\cdot{x})=a\cdot(-x)$
        - Proof
            
            본 정리의 경우 $(a\cdot{x})$의 역원을 이용한다.
            
            $ax+(-a)x=\{a+(-a)\}x=0\cdot{x}=0
            \\ax+a(-x)=a\{x+(-x)\}=a\cdot{0}=0$
            
            위 두 식으로 $(-a)\cdot{x}$과 $a\cdot{(-x)}$이 $(a\cdot{x})$의 역원임을 증명
            
            또한, 위의 corollary에서 덧셈의 역원은 unique하다는 명제에 의해 위 정리는 성립한다.
            
    -