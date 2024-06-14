# Lecture 2

Outline: 
* [00:00](https://www.youtube.com/watch?v=4b4MUYve_U8&list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU&index=2&t=0s)  Intro 
* [00:45](https://www.youtube.com/watch?v=4b4MUYve_U8&list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU&index=2&t=45s) Motivate Linear Regression 
* [03:01](https://www.youtube.com/watch?v=4b4MUYve_U8&list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU&index=2&t=181s) Supervised Learning 
* [04:44](https://www.youtube.com/watch?v=4b4MUYve_U8&list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU&index=2&t=284s) Designing a Learning Algorithm 
* [08:27](https://www.youtube.com/watch?v=4b4MUYve_U8&list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU&index=2&t=507s) Parameters of the learning algorithm 
* [14:44](https://www.youtube.com/watch?v=4b4MUYve_U8&list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU&index=2&t=884s) Linear Regression Algorithm 
* [18:06](https://www.youtube.com/watch?v=4b4MUYve_U8&list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU&index=2&t=1086s) Gradient Descent 
* [33:01](https://www.youtube.com/watch?v=4b4MUYve_U8&list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU&index=2&t=1981s) Gradient Descent Algorithm 
* [42:34](https://www.youtube.com/watch?v=4b4MUYve_U8&list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU&index=2&t=2554s) Batch Gradient Descent 
* [44:56](https://www.youtube.com/watch?v=4b4MUYve_U8&list=PLoROMvodv4rMiGQp3WXShtMGgzqpfVfbU&index=2&t=2696s) Stochastic Gradient Descent

---

My notes:
1. Model representation -- this is the hypothesus. An equation that could define the relationship between inputs and output
    1. Picking the right model / equation / or hypothesus: Depending on the shape of the data when plotted, if a straight line  doesn't fit the relationship, we can use any order of polynomial. The idea is to identify the correct polynomial or function that doesn't underfit or overfit the data. 
1. Cost function: We need to find the right parameters for the equations; for example, values of `a` and `b` in `h(x)=a+bx`. We start by using any random value for the parameters (for example 0 and 1) and then calculate how accurate these random parameters. We calculate the accuracy of a model in linear regression using [mean squared error](https://en.wikipedia.org/wiki/Mean_squared_error). We call this the cost function -- could also be called an error function. 
1. Linear regression: simplest supervised learning algo
    1. Example: predict house price based on size (sq feet) of a house, or # of beds, school rating, built year...
    1. General algo process:
        1. Get a training set
        1. Feed it to the learning algo (hypothesis -- or a model) i.e. `h(x)=a+bx`
        1. Use a learning algo to find the model constants / parameters. For example, values of `a` and `b` in `h(x)=a+bx`
    1. Goal of the linear regression algo: The goal of the algo is to find the parameter set with the lowest error. When plotted, a cost function, often creates a U type curve with a single parameter -- and a hills and pits like bowl/convax shape with multiple parameters. The goal here is to find the lowest point (pit) of the cost function.
    1. Gradient descent algo: Gradient descent algo takes the derivative (tangent line) of the cost function and dives slowly down from the hill towards a pit. Basically, you do `a := a - const * deriv of cost function`. Constant is used to speed up the descent. 
    1. "Batch" gradient descent: The above process is also called a batch gradient descent since it uses the cost function which loops through entire dataset to calculate the squred error. Consider if you have millions of these inputs, every step in descent would mean calculating errors at every step. 
    1. Stochastic gradient descent: Instead of the entire parameter set, you can use just one parameter and apply the gradient descent algo to it. This gets to the results close enough and saves compute.
    1. Normal equation: Only works on linear regression. It's a simplified version of GD which uses one step to compute global minimum (lowest point / pit of the cost function)
---

Recap by Tammy AI
* [0:41](https://www.youtube.com/watch?v=4b4MUYve_U8&t=41s):  This class will cover linear regression, batch and stochastic gradient descent, and the normal equations as algorithms for fitting linear regression models.
* [5:35](https://www.youtube.com/watch?v=4b4MUYve_U8&t=335s):  The speaker discusses using multiple input features, such as size and number of bedrooms, to estimate the size of a house.
* [12:03](https://www.youtube.com/watch?v=4b4MUYve_U8&t=723s):  The hypothesis is defined as the sum of features multiplied by parameters.
* [18:40](https://www.youtube.com/watch?v=4b4MUYve_U8&t=1120s):  Gradient descent is a method to minimize a function J of Theta by iteratively updating the values of Theta.
* [24:21](https://www.youtube.com/watch?v=4b4MUYve_U8&t=1461s):  Gradient descent is a method used to update values in each step by calculating the partial derivative of the cost function.
* [30:13](https://www.youtube.com/watch?v=4b4MUYve_U8&t=1813s):  The partial derivative of a term with respect to Theta J is equal to XJ, and one step of gradient descent updates Theta J
* [36:08](https://www.youtube.com/watch?v=4b4MUYve_U8&t=2168s):  The choice of learning rate in the algorithm affects its convergence to the global minimum.
* [41:45](https://www.youtube.com/watch?v=4b4MUYve_U8&t=2505s):  Batch gradient descent is a method in machine learning where the entire training set is processed as one batch, but it has a disadvantage when dealing with large datasets.
* [47:13](https://www.youtube.com/watch?v=4b4MUYve_U8&t=2833s):  Stochastic gradient descent allows for faster progress in large datasets but never fully converges.
* [52:23](https://www.youtube.com/watch?v=4b4MUYve_U8&t=3143s):  Gradient descent is an iterative algorithm used to find the global optimum, but for linear regression, the normal equation can be used to directly jump to the global optimum.
* [58:59](https://www.youtube.com/watch?v=4b4MUYve_U8&t=3539s):  The derivative of a matrix function with respect to the matrix itself is a matrix with the same dimensions, where each element is the derivative with respect to the corresponding element in the original matrix.
* [1:05:51](https://www.youtube.com/watch?v=4b4MUYve_U8&t=3951s):  The speaker discusses properties of matrix traces and their derivatives.
* [1:13:17](https://www.youtube.com/watch?v=4b4MUYve_U8&t=4397s):  The derivative of the function is equal to one-half times the derivative of Theta multiplied by the transpose of X minus the transpose of y.