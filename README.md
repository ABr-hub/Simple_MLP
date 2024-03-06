# Simple_MLP

***(Please be patient. This repository is under construction.)***

This repository contains a **basic MLP**, implemented from scratch to demonstrate it's capabilities in comparison to the **logistic regression** as a basline machine learning method across different problems of varying complexity.

---

The table below presents different classification problems (= problems where data points belong to one of two classes). The objective is to identify separating lines (decision boundaries) that effectively distinguish between the blue and red dots.
Two possible classification methods are applied and compared to solve this problem:

1. <ins>Logistic regression</ins>: A linear classification model that predicts the probability that a given input belongs to a certain class.
2. <ins>Multi-layer-perceptron</ins>: A type of artificial neural network composed of multiple layers of nodes (neurons) that use non-linear activation functions.

The plots displays the resulting regions indicating the color affiliation. These regions are delineated to illustrate the classification outcomes, with distinct areas representing the affiliation of different colors.

| # | Problem     | Logistic Regression Solution | MLP Solution
| :----: |    :----:   |    :----:   |    :----:   |
| 1 | <img src="https://github.com/ABr-hub/Simple_MLP/blob/8cafb31ea28e5df6ea8a2a9b401f74b8f2fdb33f/ressources/Comparison_LR_MLP/Classification_Problem.png" width=95% height=95%> | <img src="https://github.com/ABr-hub/Simple_MLP/blob/7f005a126dae80dfbbd4f285fe9ac52c4f73594a/ressources/Comparison_LR_MLP/Classification_LR.png" width=95% height=95%>  |  <img src="https://github.com/ABr-hub/Simple_MLP/blob/7f005a126dae80dfbbd4f285fe9ac52c4f73594a/ressources/Comparison_LR_MLP/Classification_MLP.png" width=95% height=95%>           |
| 2 | <img src="https://github.com/ABr-hub/Simple_MLP/blob/817fda41d9ca4a699873cd992057347ec36d5d12/ressources/GaussianQuantilesProblem/GaussianQuantiles_Problem.png" width=95% height=95%> | <img src="https://github.com/ABr-hub/Simple_MLP/blob/817fda41d9ca4a699873cd992057347ec36d5d12/ressources/GaussianQuantilesProblem/GaussianQuantiles_LR.png" width=95% height=95%>  |  <img src="https://github.com/ABr-hub/Simple_MLP/blob/817fda41d9ca4a699873cd992057347ec36d5d12/ressources/GaussianQuantilesProblem/GaussianQuantiles_MLP.png" width=95% height=95%>           |
| 3 | <img src="https://github.com/ABr-hub/Simple_MLP/blob/dda64ba3f036427e5fa6fbf7f48ce5e76cc18075/ressources/CirclesProblem/circles_Problem.png" width=95% height=95%> | <img src="https://github.com/ABr-hub/Simple_MLP/blob/dda64ba3f036427e5fa6fbf7f48ce5e76cc18075/ressources/CirclesProblem/circles_LR.png" width=95% height=95%>  |  <img src="https://github.com/ABr-hub/Simple_MLP/blob/08ff0705d35ce800dfb310fda01cddb653f6545c/ressources/CirclesProblem/circles_MLP.png" width=95% height=95%>           |
| 4 | <img src="https://github.com/ABr-hub/Simple_MLP/blob/775fc542d07f9f4ce8e6f9d51c38730eee1b8332/ressources/MoonsProblem/moons_Problem.png" width=95% height=95%> | <img src="https://github.com/ABr-hub/Simple_MLP/blob/775fc542d07f9f4ce8e6f9d51c38730eee1b8332/ressources/MoonsProblem/moons_LR.png" width=95% height=95%>  |  <img src="https://github.com/ABr-hub/Simple_MLP/blob/775fc542d07f9f4ce8e6f9d51c38730eee1b8332/ressources/MoonsProblem/moons_MLP.png" width=95% height=95%>           |

**<ins># 1. Random classification:</ins>**
 * **Problem**: The data points are randomly distributed in a two-dimensional space.
 * **Solution**
   * Logistic Regression:
   * MLP: 

**<ins># 2. Gaussian Quantiles:</ins>**
 * **Problem**: This classification dataset is generated from a multi-dimensional standard normal distribution. The classes are determined by nested concentric multi-dimensional spheres, ensuring that each class contains roughly the same number of samples. These spherical boundaries divide the data into segments, or quantiles, based on the distribution's characteristics.
 * **Solution**
   * Logistic Regression:
   * MLP: 

**<ins># 3. Circles:</ins>**
 * **Problem**: This classification task involves a circular structure where a larger circle encompasses a smaller circle within it.
 * **Solution**
   * Logistic Regression:
   * MLP:  

**<ins># 4. Half-moons:</ins>**
 * **Problem**: This classification task involves two interleaving half circles.
 * **Solution**
   * Logistic Regression:
   * MLP: 




Description of the table and the problems as well as solutions showcased; (Unsolvable problems can be solved with more complex model; SVM etc.)




MLP Background (Draft Network, Perceptron as well as description)
...
  - Backrpop

Problems
...

Solutions
...


---

Solving the unsolvable with neuroevolution...

---

Stepping up the MLP with more complexity (Demonstrate neuroevolution at 'circles' and another complex problem)

---

The accompanying images illustrate the iterative problem-solving process observed during the neural network's training phase, featuring a selection of sample problems. As training progresses, notable refinements to the decision boundary are evident, ultimately yielding an accuracy rate surpassing 90% for each respective problem scenario.

<img src="https://github.com/ABr-hub/Simple_MLP/blob/f25321811243281fa3d8e7e76132016ffe8aeb8f/ressources/circlesMLP.gif"  width=44% height=44%/> <img src="https://github.com/ABr-hub/Simple_MLP/blob/f25321811243281fa3d8e7e76132016ffe8aeb8f/ressources/mlpMoon.gif"  width=44% height=44%/>





