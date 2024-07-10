---
title: "Machine Learning for beginners"
date: 2024-07-05T15:44:20+08:00
author: "Daoyuan"
slug:
draft: false
toc: false
---

Machine Learning is the subfield of the artificial interlligence that give computers the ability to learn without being explicityly programmed.[^1]
[^1]:Authur Samuel,1959.

The main types of machine learning are **supervised learning** and **unsupervised learning**. 

# Supervised Learning
 **Supervised Learning** learns from being given “right answers” has been used most widely in real-world applications including *spam filtering, speech recoginition, machine translation, online adversising, self-driving cars and visual inspection*. The two major algorithms in supervised learning are **regression** and **classification**.

## Regression
**Regression** predict a number infinitely many possible outputs, such as inferring the price of a house from a given housing price dataset. The algorithm used here is a typical type of *Linear Regression*. The terminology of the dataset should *trainning set*, where x represents the input variable and y represents the output variable. 

Here is a summary of some of the notation you will encounter.  

|General <img width=70/> <br />  Notation  <img width=70/> | Description<img width=350/>| Python (if applicable) |
|: ------------|: ------------------------------------------------------------||
| $a$ | scalar, non bold                                                      ||
| $\mathbf{a}$ | vector, bold                                                      ||
| **Regression** |         |    |     |
|  $\mathbf{x}$ | Training Example feature values (in this lab - Size (1000 sqft))  | `x_train` |   
|  $\mathbf{y}$  | Training Example  targets (in this lab Price (1000s of dollars))  | `y_train` 
|  $x^{(i)}$, $y^{(i)}$ | $i_{th}$Training Example | `x_i`, `y_i`|
| m | Number of training examples | `m`|
|  $w$  |  parameter: weight                                 | `w`    |
|  $b$           |  parameter: bias                                           | `b`    |     
| $f_{w,b}(x^{(i)})$ | The result of the model evaluation at $x^{(i)}$ parameterized by $w,b$: $f_{w,b}(x^{(i)}) = wx^{(i)}+b$  | `f_wb` | 

## Cost Function
- **Cost Function**  provides a measure of how well your predictions match your training data. The equation for cost with one variable is:$$J(w,b) = \frac{1}{2m} \sum\limits_{i = 0}^{m-1} (f_{w,b}(x^{(i)}) - y^{(i)})^2 \tag{1}$$. If the $(f_{w,b}(x^{(i)}) - y^{(i)})^2 $ term will be zero, then the cost is minimized, indicating that the best parameters fit the model well.
  
- **Visulization of Cost Function**
Both 3D plots and contour plots can visualize a cost function to observe if the corresponding parameters fit the data well. To automate the process of optimizing w and b, we should use **gradient descent**. 

-**gradient descent**

- **Classification** predict categories and small finite limited numbers.

**Unsupervised Learning** find something interesting in unlabeled data. The data comes with input x, but without labels y. 
- *Clustering* is used to group similar data points like google news.
- *Anomaly detection* is for finding unusual data points like fraud detections.
- *Demensionality reduction* compress data using fewer numbers.


