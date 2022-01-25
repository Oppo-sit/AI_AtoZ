# 04 Linear independence

## 1. Linear independence

- Linear dependent
    - $a_{1}u_1 + a_{2}u_{2} + ... + a_{n}u_n = 0,$  $u_1, u_2, ...., u_n \in {S}$일 때, 최소 하나의 vector의 계수가 ($a_1, a_2, ...., a_n$) 0이 아니라면, subset S는 linear independent하다고 정의
    - 본 정의는, $a_{1}u_1 + a_{2}u_{2} + ... + a_{n}u_n = 0$를 이항한 $a_{2}u_{2}  = -(a_{1}u_1 + a_{3}u_3 + ... + a_{n}u_n)$에서 $a_2\neq{0}$라면, $u_2$는 다른 vector들의 선형결합으로 만들어지므로 고유한 vector가 아닌 dependence를 가짐

- if $a_1=a_2=...=a_n=0$ (trivial한 경우), $a_{1}u_1 + a_{2}u_{2} + ... + a_{n}u_n = 0$을 만족할 경우 subset S는 linearly independent
    - 반면, $a_1\sim a_n$중 하나라도 0이 아닌 경우(non-trivial),
        
        S는 linearly dependent $\leftrightarrow \exists{a}$ nontrivial representation of 0
        
    - example) $0\in{S}$ (zero vector가 S에 속한 경우)
        - 0 = 1 $\cdot$ 0 (어떠한 계수를 곱해도 zero vector가 나옴)
        - Subset S is linearly dependent
        - Subspace는 zero vector를 가지고 있으므로 항상 linearly dependent
    - example 2) $V=M_{2\times3}(R)$
        - $S=\{
        \begin{pmatrix}
        1 & -3 & 2  \\
        -4 & 0 & 5  \\
        \end{pmatrix},
        \begin{pmatrix}
        -3 & 7 & 4  \\
        6 & -2 & -7  \\
        \end{pmatrix},
        \begin{pmatrix}
        -2 & 3 & 11  \\
        -1 & -3 & 2 \\
        \end{pmatrix}
        \}$
        - S is linearly independent?
        - $au_1 + bu_2 + cu_3 = 0 → a=b=c=0$?
        - 위 식으로부터
            - a-3b-2c=0, -3a+7b+3c=0, 2a+4b+11c=0
                
                -4a+6b-c=0, -2b-3c=0, 5a-7b+2c=0
                
            - 위 방정식으로 부터 a=5, b=3, c=-2 (nontrivial representation이 존재)
            - S is linearly dependent
            
- Property(성질)
    
    1) $\emptyset$ is linearly independent
    
    2) {u} is linearly independent when u$\neq$0
    
    - Proof
        - {u}가 linearly dependent라 가정
        - $a\neq0$인 계수 존재 s.t. $a\cdot{u} = 0$
        - 양변에 $a^{-1}$을 곱하면 u=0, contradiction!
        
- Definition of Linear independence
    - The only representation of 0 is the trivial representation
    - $a_{1}u_1 + a_{2}u_{2} + ... + a_{n}u_n = 0\leftrightarrow{a_1=a_2=...=a_n=0}$ 이 성립한다면 linearly independent, 이는 어떤 벡터도 다른 벡터들의 linear combination으로 나타낼 수 없음을 의미

- Theorem 1.6
    - $S_1\subset{S_2}\subset{V}$를 가정하면 $S_1$ : linearly dependent ⇒ $S_2$ : linearly dependent
    - Set이 커지면 dependent해짐
    
- 어떤 vector space가 주어졌을 때, 가장 작은 generating(spanning) set은?
    - example) S={$u_1, u_2, u_3, u_4$}
    - $u_1$=(2, -1, 4), $u_2$=(1, -1, 3), $u_3$=(1, 1, -1), $u_4$=(1, -2, -1)의 linear combination은
        
        $-2u_1 + 3u_2 + u_3 - 0\cdot{u_4}=0$
        
    - Linearly dependent하므로 어떤 벡터는 다른 벡터들의 linear combination으로 표현 가능
        - if  $u_3 =2u_1 - 3u_2 + 0\cdot{u_4}$, $span(u_1, u_2, u_3, u_4) = span(u_1, u_2, u_4)$
        - Dependent한 속성을 가진 벡터는 고유한 벡터가 아니므로 다른 벡터로 대체할 수 있다는 의미
    
- Theorem 1.7
    - Subset S:linearly independent
    - $u_1, u_2, ..., u_n \in{S}$
    - $v\in{V}. v\notin{S}$일 때, $S\cup{\{v\}}$: linearly dependent $\longleftrightarrow{v}\in{span(S)}$
    - Proof (필요충분이므로 양방 검정이 필요)
        - → 검증
        - $a_{1}v + a_{1}u_{1} + ... + a_{n}u_n = 0$을 가정
        - $a_1\neq0$ ($a_1=0$이면, 모든 계수가 0이 됨)이므로
            
            $v = -a_{1}^{-1}(a_{1}u_{1} + ... + a_{n}u_n)$
            
        - v는 $\{u_1, u_2, ..., u_n\}$의 선형결합으로 나타낼 수 있으므로
            
            $v\in{span(S)}$
            
        - ← 검증
        - $v\in{span(S)}$이므로
            
            $v= b_{1}v_{1} + b_{2}v_{2} + ... +b_{m}v_m$ 
            
        - $b_{1}v_{1} + b_{2}v_{2} + ... +b_{m}v_m + (-1)v = 0$
            
            v의 계수가 0이 아니므로 linearly dependent
            
        - $\{v_1, v_2, ..., v_m, v\}$ : linearly dependent
            
            $\{v_1, v_2, ..., v_m, v\} \subset ({S}\cup{\{v\}})$
            
        - $\therefore {S}\cup{\{v\}}$ is linearly dependent