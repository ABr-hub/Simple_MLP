# Simple_MLP

***(Please be patient. This repository is under construction.)***

This repository contains a **basic MLP**, implemented from scratch to demonstrate it's capabilities in comparison to the **logistic regression** as a basline machine learning method across different problems of varying complexity.

NOTE: The drawings are taken out of my PhD Thesis ***"Deep-learning based condition monitoring of electro-mechanical drive-systems. (2024)"***

---
## The MLP

### Percepton
A simple perceptron is a single-layer neural network that consists of one input layer and one output layer. The perceptron takes input features, multiplies them by corresponding weights, sums them up with a bias term, and applies an activation function (commonly a step function or sigmoid function) to produce an output. The output is then compared to a threshold to make a binary prediction. 

$$f(x) = y = w_1 x_1 + w_2 x_2 + ... + w_n x_n + w_b b= \sigma(\mathbf{x}^T\mathbf{w} + b)$$

### Multi-Layer-Perceptron
A multilayer perceptron (MLP) is a type of artificial neural network with multiple layers, including one or more hidden layers between the input and output layers. Each neuron in the hidden layers receives inputs from the previous layer, performs a weighted sum of these inputs, adds a bias term, and applies an activation function to produce an output. The outputs of the hidden layers are passed to the subsequent layers until the final output layer, where the network produces predictions. MLPs can learn complex non-linear relationships in the data, making them suitable for various tasks such as classification, regression, and pattern recognition. Training an MLP involves adjusting the weights and biases using optimization algorithms like gradient descent to minimize a loss function, thereby improving the network's performance on the given task.

$$f(\textbf{x}) = \textbf{y} = \sigma (\textbf{x}^T \textbf{W}  + \textbf{b})$$


--- 
## A simple MLP in action

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
 * **Solution**:
   * *Logistic Regression*:
     The logistic regression as linear classifier, can find a relatively good separating line, depending on the difficulty of the dataset.
   * *MLP*:  When comparing the performance of the MLP classifier to logistic regression, it becomes evident that the MLP's ability to capture non-linear relationships leads to more complex and flexible decision boundaries. These boundaries better accommodate intricate patterns within the data, enhancing the classifier's discriminative power.
   
**<ins># 2. Gaussian Quantiles:</ins>**
 * **Problem**: This classification dataset is generated from a multi-dimensional standard normal distribution. The classes are determined by nested concentric multi-dimensional spheres, ensuring that each class contains roughly the same number of samples. These spherical boundaries divide the data into segments, or quantiles, based on the distribution's characteristics.
 * **Solution**:
   * *Logistic Regression*: Due to the non-inear nature of this specific classification problem the logistic regression classifier can not find appropriate decision boundaries to solve this problem. Due to the "symmetric" nature of the problem, the classification performance lies around ~50%.
   * *MLP*: Similar to the previous point, the MLP's non-linear capabilities facilitate the discovery of effective decision boundaries, resulting in high classification performance.

**<ins># 3. Circles:</ins>**
 * **Problem**: This classification task involves a circular structure where a larger circle encompasses a smaller circle within it.
 * **Solution**:
   * *Logistic Regression*: As in #2 the logistic regression classifier can not find appropriate decision boundaries to solve this problem.
   * *MLP*: Due to the non-linearity of the data distribution the implemented, very simple mlp faces difficulties. The mlp lacks the depth and complexity to learn the non-linear transformations, and struggles to delineate clear decision boundaries between the concentric circles, leading to poor classification performance.

**<ins># 4. Half-moons:</ins>**
 * **Problem**: This classification task involves two interleaving half circles.
 * **Solution**:
   * *Logistic Regression*: As in #2 the logistic regression classifier can not find appropriate decision boundaries to solve this problem.
   * *MLP*: The moons classification problem involves highly intricate or overlapping moon shape. Due to the low complexity of the implemented mlp, it struggles to find a suitable descision boundary to accurately separate the two classes.

...
  - Backrpop

Problems
...

Solutions
...


---

## Solving the unsolvable with ...

### ... neuroevolution

### ... higher complexity

The accompanying images illustrate the iterative problem-solving process observed during the neural network's training phase, featuring a selection of sample problems. As training progresses, notable refinements to the decision boundary are evident, ultimately yielding an accuracy rate surpassing 90% for each respective problem scenario.

<img src="https://github.com/ABr-hub/Simple_MLP/blob/f25321811243281fa3d8e7e76132016ffe8aeb8f/ressources/circlesMLP.gif"  width=44% height=44%/> <img src="https://github.com/ABr-hub/Simple_MLP/blob/f25321811243281fa3d8e7e76132016ffe8aeb8f/ressources/mlpMoon.gif"  width=44% height=44%/>
