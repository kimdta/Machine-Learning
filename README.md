# Machine-Learning
# 1. Supervised learning
The goal of supervised learning is to infer a function h : X → Y (hypothesis) based on available correct data.
X is called input space. An element x ∈ X is called an observation, or an input.
Y is the decision space.
This can be a continuous space such as Y = R (or $`Y = R^n`$) which makes a regression problem; or a discrete, finite space (e.g. Y = {α, β, γ}) which makes a classification problem.
• Assume we have a dataset of pairs (x,y) ∈ X ×Y
where x is the input and y the expected correct output (label or target)
• We can use the data as a training data set D = (x_i,y_i), i ∈ {1,...,n}􏰁 to learn the relationship between inputs and targets

Goal of Learning: Loss and Risk
For (x,y) ∈ (X,Y) let yˆ = h(x):
y is the correct label for x (target)
yˆ is the output of the model h (prediction)
What if they are different?
• Example: fruit classification. Let x be an image of an apple, so y = apple represents the correct output. If our model outputs h(x) = yˆ = orange the prediction is incorrect. All errors are equally wrong (i.e. predicting orange or banana is equivalent).
• Regression is easier to quantify for now: if y = 5 but yˆ = 3 we know that we are wrong by −2. Errors have magnitude.
• Loss function: L : Y × Y → R0+ is more than just the error: it measures the “cost” or “severity” of predicting yˆ = h(x) instead of y.
• WeusuallyassumeL(yˆ,y)=0ifyˆ =y,forally ∈Y.
