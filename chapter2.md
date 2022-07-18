# 2.1.5 特征向量和特征值

## 2.21

**Repeat the proof of the spectral decomposition in Box 2.2 for the case when M is Hermitian, simplifying the proof wherever possible.**


---

## 2.22

**Prove that two eigenvectors of a Hermitian operator with different eigenvalues are necessarily orthogonal.**

先证明 **Hermite矩阵的特征值都是实数**

H 是 normal 的因此可对角化 $H = \sum_i \lambda_i |i\rangle \langle i|$

 $H^\dagger =H$

$H^\dagger = ( \sum_i \lambda_i |i\rangle \langle i|)^\dagger = \sum_i \lambda_i^*|i\rangle \langle i|$ 

因此 $\lambda_i = \lambda_i^*$，即特征值都是实数


假设 特征值 $\lambda_1,\lambda_2$ 对应的特征向量是 $|x\rangle , |y\rangle $

则有
$$
H|x\rangle = \lambda_1 |x\rangle,H|y\rangle = \lambda_2 |y\rangle
$$
由此得到
$$
\begin{aligned}
\langle y| H|x\rangle = \lambda_1\langle y|x\rangle
\end{aligned}
$$

并且

$$
\begin{aligned}
    
    &\langle x| H|y\rangle = \lambda_2\langle x|y\rangle\\
    &\langle y|H^\dagger |x\rangle = \lambda_2^* \langle y|x\rangle\\
    &\langle y|H|x\rangle = \lambda_2 \langle y|x\rangle
\end{aligned}
$$

比较上面两个式子，由于 $\lambda_1\ne \lambda_2$，只能是 $\langle y|x\rangle  = 0$ 

---

## 2.23

**Show that the eigenvalues of a projector P are all either 0 or 1.**

投影算子是幂等的

$$
\lambda |x\rangle = P|x\rangle = P^2|x\rangle = \lambda^2 |x\rangle
$$

因此 $\lambda^2 = \lambda$，$\lambda$ 是0或1

---

## 2.24

**(Hermiticity of positive operators) Show that a positive operator is necessarily Hermitian. (Hint: Show that an arbitrary operator A can bewritten A = B + iC where B and C are Hermitian.)**

由 positive 证明  Hermitian

将 A 的实数部分和虚数部分分开得到 $A = B + i C$，其中 B C 都是实矩阵。

对任意**实**向量 $\langle v|$，有 

$$
\langle v|A|v\rangle  = \langle v|B|x\rangle  + i\langle v|C|v\rangle  \in \R
$$

因此上式的虚部恒等于0，$C = 0$

下面只需证明$B$是对称的即可说明 A 是 Hermitian 的

任取 $v\in \R^n$

$$
(|v\rangle ,B|v\rangle ) = \langle v|B|v\rangle  = (B^T|v\rangle , |v\rangle ) = (|v\rangle , B^T|v\rangle ) 
$$


**引理**：如果 $<v|A|v> = 0$ 对于所有复向量v 成立，则 A = 0

> 证明：
> 对向量 x + k y($k\in \Z$)
> $$
> \begin{aligned}
> <x + k y | A | x + k y> &=k<x|A|y> + \bar k <y|A|x>\\
> &= k u + \bar k \bar u (u = <x|A|y>) = 0
> \end{aligned}
> $$
>  
> 分别取 k = 1, k = i,解上述方程组得到 $u= \bar u = 0$
> 因此 <x|A|y> = 0 对于任意x,y成立，因此 <x|A =0 对于任意x成立，因此A = 0

由于 $(|v\rangle ,B|v\rangle ) =  (|v\rangle , B^T|v\rangle )$

$(|v\rangle ,(B - B^T)|v\rangle )  = 0$对于任意v成立，由引理得到 $B - B^T = 0,B =B^T$，B是对称矩阵

A = B + iC = B 是Hermitian矩阵

## 2.25
**Show that for any operator $A, A^\dagger A$ is positive.**

对任意x
$$
\langle x|A^\dagger A|x\rangle = (A|x\rangle , A|x\rangle) \ge 0
$$

that means $AA^\dagger$ is positive


# 2.1.7 Tensor product （张量积）



## 2.26