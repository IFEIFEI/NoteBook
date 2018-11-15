# What is Decidable About Arrays?
---
## 关注点
- 比较不同非限制数组的两个片段的相等性 [^1]
- 
---
## 语法约定
对于一个数组，使用array,elem, index分别表示数组，元素还有引用下标
a[i] 表示数组读取
a{i $$\leftarrow$$ e} 表示给数组的第i个元素赋值为e
#### axiom of read-over-write
$$(\forall\ array\  a)(\forall\ elem\ e)(\forall\ index\ i,j)\begin{bmatrix}
   \quad i=j \rightarrow a\{i\leftarrow e\}[j]=e \\   
  \wedge \  i\neq j \rightarrow a\{i\leftarrow \}[j]=a[j]
  \end{bmatrix}$$

### extensional theory
$$(\forall\ array\ a,b)[(\forall\ index \ i)a[i]=b[i] \rightarrow a=b]$$
### definition 1(theories): $$\bold{T}_{{\Bbb Z}}$$ for array indices, $$\bold{T}_{elem}^m$$ for its elements
signature: $$\Sigma_{\Bbb Z} =\{0,1,+,-,=,<\}$$ $$\Sigma_{\Bbb A} =\Sigma_{\Bbb Z} \bigcup \bigcup_k \Sigma_{elem}^k \bigcup \{ \cdot [\cdot],\cdot \{\cdot \leftarrow \cdot\}\}$$
### definition 2(terms and sorts) index variables : $${\Bbb Z}$$, element variables : $$elem_k$$
### definition 3(literal and formula): $$\bold{T}_{\Bbb A}$$-literal
### definition 4(array property): An array property is a formula of the form 
$$(\forall\ \overline{i})(\varphi_I(\overline(i)\rightarrow\varphi_V(\overline(i))$$
### definition 5(Array property fragment)

## Decision procedure $$SAT_{\rm A}$$
### Definition 6(Read Set) The read set for formula $$\psi$$ is the set 
$${\frak R}=\{t:\cdot[t]\in\psi\}$$
### Definition 7(Bounds Set) 
### Definition 8(Index Set)
$${\frak I}\xlongequal{def}
f(x)=\left\{
\begin{aligned}
\{0\}  \quad & if\ {\frak R}={\frak B}=\emptyset \\
{\frak R \bigcup \frak B} \quad &  otherwise
\end{aligned}
\right.$$
### Definition 9 ($$SAT_A$$)
## Proof the completeness and soundness
[^1]: 原文第七篇引用
---
## 启发点
- 不同数组之间的数值相等，引用相等判定？
---
## 相关知识点
- [ ] EUF: equality with uninterpreted functions
- [ ] $$\pi$$VC verifying compiler
- [ ] Presburger arithmetic
