# Machine-Learning
# 1. Supervised learning
The goal of supervised learning is to infer a function h : X → Y (hypothesis) based on available correct data.
• X is called input space.
An element x ∈ X is called an observation, or an input.
• Y is the decision space.
This can be a continuous space such as Y = R (or Y = R^n) which makes a regression problem; or a discrete, finite space (e.g. Y = {α, β, γ}) which makes a classification problem.
• Assume we have a dataset of pairs (x,y) ∈ X ×Y
where x is the input and y the expected correct output (label or target)
• We can use the data as a training data set D = 􏰀(x_i,y_i), i ∈ {1,...,n}􏰁 to learn the relationship between inputs and targets
