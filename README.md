[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-718a45dd9cf7e7f842a935f5ebbe5719a5e09af4491e668f4dbf3b35d5cca122.svg)](https://classroom.github.com/online_ide?assignment_repo_id=11908407&assignment_repo_type=AssignmentRepo)
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

# Proof: 
$f(n) \in O(log_2(n))$:

$\exists c_1, n_0: f(n) \in c_1 \cdot \log_{2} n \forall n \geq n_0$

$\log_{b}(a) = \log_{c}(a) / \log_{c}(b)$ thus $\log_{5}(n) = \log_{2}(n) / \log_{2} 5$

$f(n) \in (c / \log_{2}(5)) \cdot \log_{2}(n)$ but $(c / \log_{2}(5))$ is just a constant, let's call it K.
Thus there exists a $c_1$ and $n_0$ such that $f(n) \in K \cdot \log_{2}(n) \forall n \geq n_0$


Furthermore $f(n) \in O(\log{5}(n))$:

$\exists c_2, n_0: f(n) \in c_2 \cdot \log_{5} n \forall n \geq n_0$

$\log_{b}(a) = \log_{c}(a) / \log_{c}(b)$ thus $\log_{2}(n) = \log_{5}(n) / \log_{5}(2)$

$f(n) \in (c / \log_{5}(2)) \cdot \log_{5}(n)$ but $(c / \log_{5}(2))$ is just a constant, let's call it N.
Thus there exists a $c_2$ and $n_0$ such that $f(n) \in N \cdot \log_{5}(n) \forall n \geq n_0$

Therefore $O(\log_{2}(n)) = O(\log_{5}(n))$ asymptotically. 
