[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=12027614&assignment_repo_type=AssignmentRepo)
# Asymptotic Equivalences

In the lectures, we said that logarithms with different bases don't affect the
asymptotic complexity of an algorithm. Prove that $O(\log_{2} n)$ is the same as
$O(\log_{5} n)$. Use the mathematical definition of $O$ -- do a formal proof,
not just the intuition.

I have started with the formal definition of $O$ below. Add your answer to this
markdown file. [This
page](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/writing-mathematical-expressions)
might help with the notation for mathematical expressions.


<u>**Proof :**</u>

==> Prove that $O(\log_{2}n) = O(\log_{5}n)$

**NOTE** : $O(\log_{2} n)$ and $O(\log_{5} n)$ are both sets

**NOTE** : <i>to prove the equivelence of two sets we have determine that any element in $\theta(\log_{2} n)$ is also in $\theta(\log_{5} n)$, and vice versa</i> 

**NOTE** : <i>Def of Big $O$ : $T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$</i>

<u>**Prove that any element in $O(\log_{2} n)$ is also in $O(\log_{5} n)$**</u>

==> $T(n) \in O(\log_{2} n) \iff \exists c, n_0: T(n) \leq c \cdot (\log_{2} n) \forall n \geq n_0$

====> **NOTE** : <i>we can multiply by a constant factor to change bases</i>

====> **NOTE** : <i>$\log_{x}y = \frac{log_{z}y}{log_z{x}}$</i>

====> $T(n) \leq c \cdot \frac{1}{\log_{5}2} \cdot (\log_{2} n)$

====> $T(n) \leq d \cdot (\log_{5}n)$

====> $T(n) \in O(\log_{5}{n})$

==> $\forall T(n) \in O(\log_{2}n) \implies T(n) \in O(log_{5}n)$

<u>**Prove that any element in $O(\log_{5}n)$ is also in $O(\log_{2}n)$**</u>

==> $T(n) \in O(\log_{5}n) \iff \exists c, n_0: T(n) \leq c \cdot (\log_{5} n) \forall n \geq n_0$

====> **NOTE** : <i>we can multiply by a constant factor to change bases</i>

====> **NOTE** : <i>$\log_{x}y = \frac{log_{z}y}{log_z{x}}$</i>

====> $T(n) \leq c \cdot \frac{1}{\log_{2}5} \cdot (\log_{5} n)$

====> $T(n) \leq d \cdot (\log_{2} n)$

====> $T(n) \in O(\log_{2}{n})$

==> $\forall T(n) \in O(\log_{5}n) \implies T(n) \in O(log_{2}n)$
