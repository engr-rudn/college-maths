

# Category Theory

## Natural Transformation

$\tau: S\dot{\rightarrow}T, S, T: Fun(C, D)$.

```
C:              D:
c          Sc ------> Tc
|           |    tc   |
|  ===>  Sf |       Tf|
V           V         V
c'         Sc'------> r'
                tc'
```

Nat = morphism of Fun. $Nat(C,D)=Hom(Fun(C,D))$.

#### Example

$\{a_i\},\{b_i\}$ seq of $C$, $\tau:a\dot\to b$, $\tau_i:a_i\to b_i$

```
C:
ai ------> bi
|    ti   |
|         |
V         V
aj------> bj
    tj
```

#### Def of cone

$\tau:\{a_i=c\}\to\{b_i\}, \{a_i\}\to \{b_i=c\},c\in C$.



## Universals and Limits

#### Definition

$S:D\to C, c\in C$, $(r,u),r\in D, u:c\to Sr$ is the universal arrow (ua) if $\forall (d,f),d\in D,f:c\to Sd, \exists! f':r\to d, Sf'\circ u=f$.

```
C:           <----  D:  S
c  ----->  Sr       r
  \   u    |        |
    \   Sf'|      f'|
   f  \    V        V
        \> Sr'      r'
```

#### Fact

$(r,u)$ is the initial obj of $c\downarrow S$, namely, $io(c\downarrow S)=ua(c, S)$

#### Example of ua $u:c\to Sr$

1. $j:X\to U(V_X)$
2. $P:G\to U(C)$


#### Definition(univ. element)

$S:D\to C, c\in C$, $(r,e),r\in D, e:Sr$ is the universal element (ue) if

 $\forall (d,x),d\in D,x:Sd, \exists! f':r\to d, Sf'(e)=x$.

#### Fact

$(r,e)$ is the initial obj of $*\downarrow S$. $ue(S)=io(*\downarrow S)=ua(*,S)$, where $e=u*$ (we identifies $ e$ with $u$).

### Yoneda Lemma

#### Proposition

$S:D\to C, (r,u)$ is ua iff $\exists\phi_d:f'\mapsto Sf'\circ u:$

$$
D(r,d)\simeq C(c,Sd),
$$

natural in $d\in D$. (i.e. $C(c, S-)$ is rep.)

i.e. $\phi:D(r,\cdot)\dot{\leftrightarrow} C(c,S\cdot)$.

#### Def. of Yoneda rep.

Let $D$ have small hom-sets. $(r,\psi)$ is a rep. of $K:D\to Set$, $r\in D$, and $\psi:D(r,\cdot)\simeq K$.

#### Proposition

$(r,u:*\to Kr)$ is ua iff $\psi(f':r\to d)= K(f')(u*)\in Kd$ is rep. of $K$.

 $(r, e)$ is ue iff $\psi(f':r\to d)= K(f')(e)\in Kd$ is rep. of $K$.

#### [Yoneda Lemma](https://en.wikipedia.org/wiki/Yoneda_lemma)
If $K:D\to Set,r\in D$, then $\exists y:Nat(D(r,\cdot),K)\simeq Kr$, $y:\alpha\mapsto \alpha_ri_r$, natural in $K\in Set^D, r\in D$.

$\alpha_d(f)=K(f)(\alpha_ri_r), f:r\to d$.

#### Corollary

esp. for $K=D(s,\cdot)$, $s\mapsto D(s,\cdot)$ Yoneda functor.



#### Def. of Yoneda Functor (full, faithful)

$Y(r)=D(r,\cdot), Y(f:s\to r)=D(f,\cdot):D(r,\cdot)\dot{\to} D(s,\cdot)$.

```
D   --- Y ---> Set^D           d1  ---------> d2
s              D(s, .)         D(s,d1) -----> D(s,d2)
|               ^                ^             |
| h             |.               | h*          | h*
v               |                |             v
r              D(r, .)          D(r,d1) -----> D(r,d2)
```

dual Yoneda functor $Y'(r)=D(\cdot, r)$.

## Adjoints

### Adjunctions

#### Def.

$<F,G,\phi>:X\rightharpoonup A, F:X\to A, G:A\to X$, iff (nat iso.)
$$
\phi_{x,a}: A(Fx,a)\simeq X(x,Ga)
$$
#### Thm.

$\eta_x:=\phi(i_{Fx}), \epsilon_a:=\phi^{-1}(i_{Ga})$. (unit and counit) $\phi(f)=G(f)\eta_x:x\to Ga$ for $f:Fx\to a$.

$(Fx, \eta_x)​$ is ua of $x\downarrow G​$. $(Ga,\epsilon_a)​$ is ua of $F\downarrow a​$.



#### Thm.

If $\eta:1_X\dot\to GF,\eta_x:=\phi_{x,Fx}(i_{Fx}):x\to GFx$ is ua of $x\downarrow G$, then $\langle F, G,\phi\rangle:X\rightharpoonup A$ is adj, where

$\phi(f)=G(f)\eta_x​$.



### Equiv. of Cat.

$ST\simeq I:C\to C, TS\simeq I: A\to A$.

#### Thm

$S:A\to C$ is an equiv. iff $S$ is part of equiv. $\langle T,S,\eta,\epsilon \rangle: C\rightharpoonup A$. iff $S$: full and faithful, $\forall c\in C,\exists a\in A, c\simeq Sa$.



## Monads and Algebras

### Monods

#### Def.

$<T:X\to X,\eta,\mu>$ is a monad of $X$ iff $\eta: i_X\dot{\to}T,\mu:T^2\dot{\to}T$

```
     Tmu, muT            mu
T^3  ========>  T^2 -----------> T
# (Tmu)_x:=T(mu_x), (muT)_x:= mu_Tx

    Teta, etaT        mu
T  ========>  T^2 -----------> T
```

#### Fact

If $T^2=I$ , and $\mu: I\dot\to T$, then $<T,\mu,\mu>$: monad.

```
 Haskell  采用的单子
      f           
x -----------> y
|             |
| etax        |etay (invertable)
V      Tf     V
Tx -----------> Ty

X^T:h=\eta_x^{-1}
```



#### Def. of $T$-algebra

$X^T: T^2x  \xrightarrow{Th,\mu_x}  Tx  \xrightarrow{h}  x \xrightarrow{\eta_x} Tx$

$f:<x,h>\to <x',h'>$



#### Thm

$$
Adj: <F^T,G^T,\eta^T,\epsilon^T>:X\rightharpoonup X^T
\\
G^T:<x,h>\mapsto x, F^T: x\mapsto <Tx,\mu_x>
\\
\eta^T=\eta,\epsilon^T_{<x,h>}=h
$$



#### Thm

$\langle F,G,\eta,\epsilon\rangle:X\rightharpoonup A$ defines $\langle GF,\eta,G\epsilon F\rangle$, then $\exists ! K:A\to X^T, G^TK=G,KF=F^T$.

### Free Algebras

#### Thm (Kleisli Cat. $X_T$)

$<T,\eta,\mu>$:Monad, $F_T:x\mapsto x_T(=x),f:x\to Ty\mapsto f^\flat:x_T\to y_T$.
$$
g^\flat f^\flat = (\mu_zTg f)^\flat
\\
F_T(k:x\to y)=(\eta_yk)^\flat, G_T(f^\flat:x_T\to y_T)=\mu_yT(f): Tx\to Ty
\\
<F_T,G_T,\phi:f^\flat\to f>: Adj (defines T)
$$

$f^\flat :x\to y \in X_T\iff f:x\to Ty\in X$

```haskell
f>=> g = gb o fb  -- haskell fish operator
```



#### Thm

$T-Adj$: $<F,G,\eta, \epsilon>:X\rightharpoonup A$ defines $<T,\eta,\mu>$.

$X_T\rightarrow A\rightarrow X^T$



*Remark.*  $ Ma = Hom(r, Ta)$, $m\triangleright f = \lambda x:r. m(x)\triangleright \lambda z:a.f(z,x)$