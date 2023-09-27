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

$T(n) \in O(f(n)) \iff \exists c, n_0: T(n) \leq c \cdot f(n) \forall n \geq n_0$

Thm : $T(\log_{2} n) \in O(\log_{5} n) \iff \exists c, n_0: T(\log_{2} n) \leq c \cdot (\log_{5} n) \forall n \geq n_0$

Note : $ \log_{y}x = \frac{\log(x)}{\log(y)}$

Proof : 

==> $T(\log_{2} n) \in O(\log_{5} n)$

==> $T(\log_{2} n) \in O(\log_{5} n) \iff T(\log_{2} n) \leq c \cdot \log_{5}n $

==> $T(\log_{2} n) \in O(\log_{5} n) \iff T(\frac{\log(n)}{\log(2)}) \leq c \cdot (\frac{\log(n)}{\log(5)}) $

==> $T(\log_{2} n) \in O(\log_{5} n) \iff T(\frac{1}{\log(2)}) \leq c \cdot (\frac{1}{\log(5)}) $ 

==> True

