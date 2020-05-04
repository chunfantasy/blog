---
layout: post
title: Deep Learning
description: "This is a learning note about deep learning."
modified: 2020-04-01
tags: [AI]
comments: true
mathjax: true
---

This is a learning note about deep learning.

{% if page.mathjax  %}
<script type="text/javascript" async src='https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.2/MathJax.js?config=TeX-MML-AM_CHTML'></script>
{% endif %}
<div class="social-share" data-initialized="true">
    <a href="#" class="social-share-icon icon-weibo"></a>
    <a href="#" class="social-share-icon icon-qq"></a>
    <a href="#" class="social-share-icon icon-wechat"></a>
</div>
<link rel="stylesheet" href="https://resource.chun.no/sharejs/css/share.min.css">
<script src="https://resource.chun.no/sharejs/js/social-share.min.js"></script>

---

## Definition

The term, Deep Learning, refers to training Neural Networks,
sometimes very large Neural Networks.

## Logistic Regression

It tries to solve binary classification problem.

### Given x, want

$$
\begin{align*}
  \hat{y} = P(y = 1 | x)
\end{align*}
$$

### Sigmoid function

$$
\begin{align*}
  \sigma(z) = \frac{1}{1 + {e^{-z}}}
\end{align*}
$$

### Output

$$
\begin{align*}
  \hat{y} = \sigma({w^T} + b)
\end{align*}
$$

### Loss (error) function

$$
\begin{align*}
  L(\hat{y}, y) = -(y\log \hat{y} + (1-y)\log (1-\hat{y}))
\end{align*}
$$

### Cost function

$$
\begin{align*}
  J(w, b) = \frac{1}{m} \sum_{i=1}^m L(\hat{y}^{(i)}, y^{(i)})
\end{align*}
$$

$$
\begin{align*}
  = -\frac{1}{m} \sum_{i=1}^m (y^{(i)}\log \hat{y}^{(i)} + (1-y^{(i)})\log (1-\hat{y}^{(i)}))
\end{align*}
$$

### Gradient Descent

Modify the paramters w and b to reduce the loss L by utilizing derivatives with a Computation Graph.

---

## Neural Network

### Neural Network Representation

Input layer, hidden layer(s), output layer

### Activation Function (binary classification)

If output is 0, 1, use sigmoid activation function, or tanh activation function for -1, 1.

For all other cases, use ReLU, or the rectified linear unit activation function.

### Gradient descent for Neural Networks

+ Forward propagation
+ Backward propagation

---
