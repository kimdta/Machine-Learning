# Machine-Learning
# 1. Supervised learning
The goal of supervised learning is to infer a function h : X → Y (hypothesis) based on available correct data.
X is called input space. An element x ∈ X is called an observation, or an input.
Y is the decision space.
This can be a continuous space such as Y = R (or $`Y = R^n`$) which makes a regression problem; or a discrete, finite space (e.g. Y = {α, β, γ}) which makes a classification problem.

Assume we have a dataset of pairs (x,y) ∈ X x Y
where x is the input and y the expected correct output (label or target)
We can use the data as a training data set $`D =(x_i, y_i)`$,  $`i \in {1,...,n}`$to learn the relationship between inputs and targets

## Goal of Learning: Loss and Risk
For (x,y) ∈ (X,Y) let $`\hat{y} = h(x)`$:
y is the correct label for x (target)
$`\hat{y}`$ is the output of the model h (prediction)
What if they are different?

Loss function: L : Y × Y → $`R_{0+}`$ is more than just the error: it measures the “cost” or “severity” of predicting $`\hat{y} = h(x)`$ instead of y.
We usually assume $`L(\hat{y},y)= 0`$ if $`\hat{y} = y`$, for all $`y \in Y$.

The expected loss is called Risk (expected Loss):

$R(h) = E[L(h(x),y)] = \int_{X x Y} L(h(x),y). P(x,y)$

The goal of supervised learning can be defined as inferring (finding, building)an hypothesis h with minimal risk.
However the distribution P is unknown. In practice we can only compute the empirical risk:

$\hat{R}(h) = \sum_{i=1}^{n}L(h(x_i),y_i)$

# 2. Linear Classification and Perceptron

## Linear Classification
Given an input, decide to which of two classes it belongs
Example: X are fruits, Y are the labels {apple, organge}. Learn hypothesis *h*: X -> Y that classifies as correctly as possible.
The hypothesis separates the input space into 2 regions: $h^{-1}$ (apple) and $h^{-1}(organge).
Using a linear model here yeilds *linear separation*: the decision boundary between two regions is a hyperplane (i.e a line in n dimensions)

* Let the input space X be a vector space with inner product. Think of $X=R^p$ with standard inner product:
* We consider hypothesis (i.e models) of the form

$$
h(x)=
\begin{cases}
apple & \quad \text{if $f(x)>0$}\\ 
0 & \quad \text{if} $f(x)<0$
\end{cases}
$$
$f(x) = \langle(w,x)\rangle + b$
$h(x) = sign(f(x))$

