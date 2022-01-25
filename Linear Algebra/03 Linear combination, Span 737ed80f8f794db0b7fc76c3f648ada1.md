# 03 Linear combination, Span

## 1. Linear combination

- Def : $v=  a_{1}u_1 + a_{2}u_{2} + ... + a_{n}u_n$
    - $u_i$는 ‘vector’형태의 변수라 생각
- simple example
    - v=(3, 5) = 3(1, 0) + 5(0, 1)
    - (3, 5)는 (1, 0)과 (0, 1)의 linear combination
- Example
    - $2x^{3}-2x^{2}+12x-6$ is a linear combination of $x^{3}-2x^{2}-5x-3$ and $3x^{3}-5x^{2}-4x-6$?
    - $2x^{3}-2x^{2}+12x-6 = a(x^{3}-2x^{2}-5x-3) + b(3x^{3}-5x^{2}-4x-6)$
        
        → a+3b = 2, -2a-5b=-2, -5a-4b=12, -3a-6b=-6
        
        - 본 방정식을 만족하는 해를 찾으면 linear combination이 맞음
        - 방정식을 해결하는 방법 : ‘가감법’(gaussian elimination)
            
            (inverse matrix, determinent를 이용한 방법은 ‘정방행렬’에서 가능)
            
        
        <aside>
        ❔ Gaussian elimination
        방정식을 해결하는 방법 중 하나로, 방정식을 matrix로 변환, 맨 윗 행의 첫번째 열을 pivot으로 하여 아래 열을 모두 0으로 만들고, 이후 한 행씩 내려가며 pivot으로 선택 및 pivot 아래의 한 열을 모두 0으로 만들면서 답을 찾아나가는 방식
        Gaussian elimination이 모두 진행된 후에 계단모양의 matricies가 나오면 이를 ‘echelon form’이라 부름
        
        ![Untitled](03%20Linear%20combination,%20Span%20737ed80f8f794db0b7fc76c3f648ada1/Untitled.png)
        
        </aside>
        
    - 방정식을 행렬로 만들면   $\begin{pmatrix}
    1 & 3  \\
    -2 & -5  \\
    -5 & -4 \\
    -3 & -6 
    \end{pmatrix}
    \begin{pmatrix}
    a \\
    b \\
    \end{pmatrix}
    = \begin{pmatrix}
    2  \\
    -2  \\
    12 \\
    -6
    \end{pmatrix}$
        - 본 행렬을 gaussian elimination을 하면 두번째 행과 마지막 행이 충돌함을 알 수 있음
        - 따라서 본 방정식의 해(a, b)는 없으므로 linear combination이 아님

## 2. Span

- Def
    - $\emptyset\subsetneq{S}\subset{V}$ (Subset는 공집합을 포함하지만 공집합은 아니며, Vector Space의 부분집합)
    - Span(S) = {All linear combinations of vectors in S}
        - 이 때, vectors는 S에 속하는 모든 vector를 의미하며, span을 구한다는 것은 S의 전체 벡터에 대한 linear combination로부터 나올 수 있는 case(space)들을 구하는 것
    - if S = $\emptyset$, Span($\emptyset$) = {0} (zero-vector)로 정의함
- Example
    - Span{{1, 0, 0}, {0, 1, 0}} = xy-plane in $\mathbb{R}^3$
        - a{1, 0, 0} + b{0, 1, 0} = {a, b, 0}에서 a, b는 실수이므로 실수 공간의 x, y평면을 의미
- Theorem 5
    - span(S) is a subspace of V
    - Proof
        - if S $=\emptyset$ , Span(S}={0} is a subspace of V
        - if S $\neq\emptyset, x, y\in{span(S)}, u_1, u_2,...., u_n \in S$
            - $x=  a_{1}u_1 + a_{2}u_{2} + ... + a_{n}u_n, y= b_{1}u_1 + b_{2}u_{2} + ... + b_{n}u_n$
            - (x+y)도 span(S)의 원소이며, cx도 span(S)의 원소이므로 +, $\cdot$에 대해 닫혀있음
        - span(S) is a subspace of V
    
    - Any subspace that contain S must contain span(S)
    - 이 뜻은 W(subspace)가 subset S를 포함한다면 span(S)또한 포함해야 한다는 뜻
    - Proof
        - W를 V의 subspace, 그리고 S를 포함한다고 가정
        - $w\in{span(S)}$를 가정,
            
            $w = c_{1}w_1 + c_{2}w_{2} + ... + c_{n}w_n$
            
        - $w_1, w_2, ..., w_n\in{S}$이므로,
            
            $S\subset{W}$이기 떄문에, $w_1, w_2, ..., w_n\in{W}$
            
        - W는 subspace이기 때문에
            
            $w = c_{1}w_1 + c_{2}w_{2} + ... + c_{n}w_n\in{W}$가 성립함
            
        - $\therefore{span(S)}\in{W}$
    
    - new definition : A subset S generates(spans) V if span(s)=V
    - span(s)=V를 S는 V를 generate한다고 정의, 이는 어떤 subset S의 모든 linear combination을 만들면 임의의 vector space V가 생성됨을 의미
        - Example 5
        - $M_{2\times{2}}(R) = span\{
        \begin{pmatrix}
        1 & 0  \\
        0 & 1  \\
        \end{pmatrix},
        \begin{pmatrix}
        1 & 1  \\
        0 & 1  \\
        \end{pmatrix},
        \begin{pmatrix}
        1 & 0  \\
        1 & 1  \\
        \end{pmatrix}
        \}$이 성립할까?
            - $a\begin{pmatrix}
            1 & 0  \\
            0 & 1  \\
            \end{pmatrix} +
            b\begin{pmatrix}
            1 & 1  \\
            0 & 1  \\
            \end{pmatrix} +
            c\begin{pmatrix}
            1 & 0  \\
            1 & 1  \\
            \end{pmatrix}
            = \begin{pmatrix}
            a+b+c & b  \\
            c & a+b+c  \\
            \end{pmatrix}$
            - 행렬의 (1,1)과 (2,2)가 같으므로 M[1,1]과 M[2,2]가 다른 경우를 만들어내지 못하므로 span이 generate되지 않음