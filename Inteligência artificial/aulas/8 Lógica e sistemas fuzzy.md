
## Fuzzy:

Um grupo não exatamente definido

Lógica fuzzy funciona como um range entre 0 e 1

* quanto mais proximo de 1 maior o grau de pertinência do elemento para o conjunto
* quanto mais proximo de 0 menor o grau de pertinência do elemento para o conjunto

![](imagens/qm2fyvjf_w6u4hTug5WSPYD528MOFjvk0rlAT8oTu9w=.png)

nota-se que os estados de transição não são instantaneos e variam entre o grau de pertinência

## Funções de pertinência:

### Linear:

![](imagens/EBVg3ZKZ0RbDPWxCefCCAR0_o-e2qjkTt8atskDJkTE=.png)

### Trapezoidal:

![](imagens/c2ZHfE0tsGxAw66TU7b0ztWGeXwlUWj3eDCDYVNPtF4=.png)

$$
Trap(x,a,b,c,d)= \begin{cases}
0 & x \le a \\
1-\dfrac{b-x}{b-a} & a \lt x \le b \\
1 & b \lt x \le c \\
\dfrac{d-x}{d-c} & c \lt x\le d \\
0 & x \gt d
\end{cases}
$$

### Triangular:

![](imagens/7-8BRC0-03E4mpcoplEOKUFUsBudFKHoNt714OGr3h8=.png)

$$
Tri(x,a,b,c)= \begin{cases}
0 & x \le a \\
1-\dfrac{b-x}{b-a} & a \lt x \le b \\
\dfrac{c-x}{c-b} & c \lt x\le d \\
0 & x \gt d
\end{cases}
$$

## Formato S (Sigmoid):

![](imagens/8gKxWNgTO06D3lFhzxp_v84--_XwJCWVExeyNsRHReQ=.png)

$$
S(x,a,b)= \begin{cases}
0 & x \le a-b \\
\dfrac{[x-(a-b)]^2}{2b^2} & a-b \lt x \le a \\
1-\dfrac{[(a+b)-x]^2}{2b^2} & a \lt x \le a+b \\
1 & x \gt a+b
\end{cases}
$$

### formato Z:

![](imagens/IXikANWaP32KZXfjy3G0VVYjzEQTSjAd12T7Ji4SLqU=.png)

$$
Z(x,a,b) = \begin{cases}
1 & x \le a-b \\
1- \dfrac{[x-(a-b)]^2}{2b^2} & a-b \lt x \le a \\
\dfrac{[(a+b)-x]^2}{wb^2} & a \lt x \le a+b \\
0 & x \gt a+b
\end{cases}
$$

### Formato pi:

![](imagens/n1oFfEGkXRs42ENHTxu8p5vkcgYdN_n8Vjec2WrLKhU=.png)

### Formato gaussiano:

![](imagens/XRMn5j-WM3c-YvfwsUzn7HgIdPGgfbdNLKJwZdUC7dc=.png)

### Singleton:

![](imagens/FOcljI5tYLyLtSK5KfYOSXrPMGuHNCXuBu8V4TE09Ig=.png)

$$
Sgl(x,a)= \begin{cases}
1 & x = a \\
0 & x \neq a
\end{cases}
$$

## Também pode ser um formato irregular

que ultiliza os operadores **or** **and** e **not**

## calcular o fuzzyfy:

ultiliza-se centro de gravidade ou centroid da figura gerada pelo gráfico:

![](imagens/N6WsPxxKYoEmQUdN1BoQ47J10ayyw64YhsUlFrcWfq0=.png)

Descrito por:

$$
C.G. = \dfrac{\sum_y y \cdot \mu_B(y)}{\sum_y \mu_B(y)}
$$

Equivalente discreto de $y_p$

$$
y_p = \dfrac{\int y \mu_B(y)dy}{\int \mu_B(y)dy}
$$

