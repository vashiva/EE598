**Exercise:**

Background material I've drawn the questions from include 

<https://www.kdnuggets.com/2017/10/seven-steps-deep-learning-keras.html> 

Consider the following for starting out:

<https://www.kdnuggets.com/2017/10/neural-networks-step-1.html>

Answer the following questions (even if you already have a good idea based on your readings and our discussions). Give an analogy primarily using Tupperware and soup. You may add to the analogy, but make sure you denote the weights as containers, and the food as inputs. Thus a weight with value 0.6 will be a Tupperware container containing only %60 of the soup. Also, assume  inputs and weights are non-negative and normalized on the range 0 to 1 (see [the wiki article for calculating](https://en.wikipedia.org/wiki/Feature_scaling) normalization if interested). Thus we avoid "negative" soup amounts.

To start things off: A [linear feedforward](https://en.wikipedia.org/wiki/Feedforward_neural_network) neural network is really just a vector multiplied by a matrix. It also serves to illustrate "forward propagation" of values. See image below for a network partially drawn:

![resize](./asset/resize.png)

Image from  https://matrices.io/deep-neural-network-from-scratch/

As a matrix:
$$
X = \begin{bmatrix} 
1.4 & -1 & 0.4 \\ 
\end{bmatrix} \\[1.5em]


W^1 = \begin{bmatrix} 
0.01 & 0.05 & 0.07 \\ 
0.20 & 0.041 & 0.11 \\ 
0.04 & 0.56 & 0.13 
\end{bmatrix} \\[2.5em]

Z^{(2)} = X\cdot W^1\\[1.5em]

Z^{(2)} = \begin{bmatrix} 
1.4 & -1 & 0.4 \\ 
\end{bmatrix} . \begin{bmatrix} 
0.01 & 0.05 & 0.07 \\ 
0.20 & 0.041 & 0.11 \\ 
0.04 & 0.56 & 0.13 
\end{bmatrix}\\[2.5em]

Z^{(2)} = \begin{bmatrix} 
-0.17 & 0.253 & 0.04 \\ 
\end{bmatrix}
$$
If considered using the analogy, the soup will first be transferred to the input layer (a vector) of containers. Above, the input-layer is yellow.

Each entry in the input-layer, e.g. container or single yellow node, may contain differing amounts of soup, just like each input to a real neural network may have different values. The dot product, or "soup splash" consists of: taking the soups from each entry of the input vector, multiplying and then summing each "entry" as normal for the dot product and storing the result. Explanation of mathematical operations via analogy:

* Multiplication of soup: take the percentages of each bowl filled, and multiply them together. Now store that amount of soup in a new container labeled "product." (Ask yourself, do you need more than one container for the product if the inputs are normalized)
* Addition of soup: Sum works like pouring the soup from one container into another. You may find multiple containers to hold the contents of all the soup if necessary (like the two in your hand). Thus, you may need more containers as the result of the dot product summing past a value of 1.

For a single layer case, you then decide if the amount of soup produced consists of a positive or negative classification (e.g. is the amount above a threshold, say %50 of the container capacity ). Now, for the multilayer case, we will perform re-normalization between layers to ensure that each vector entry again contains only a single container (thus values between 0 and 1).

 Note that this analogy may break in some cases, feel free to call them out. It would be difficult to use this analogy for negative soup amounts. However, adding an element to the analogy  would fix this: make the bowls hot, e.g. temperature wise. We thus define the negativity in terms of how "hot" the bowl is, and thus how much soup would evaporate if poured in. A bit of a stretch, but it works and remains creative. 

As a reminder, I'm only looking for a way to facilitate your description of the work we do in a rigorous manner understandable to others. Avoiding technical terms in the analogy or explaining them is the really the first part of this exercise. 

Using an analogy (preferably soup and Tupperware) describe/answer: 

* What purpose does [back-propagation](https://www.kdnuggets.com/2017/10/neural-network-foundations-explained-gradient-descent.html) serve? 
* Can you describe the back propagation in a feedforward neural network that's trying to learn? 
* Can you explain the back-propagation process for deep-learning in terms of the analogy (add more if necessary)?
* With or without an analogy, but in your own words, describe the gradient descent algorithm here: https://www.kdnuggets.com/2017/04/simple-understand-gradient-descent-algorithm.html
* Imagine and state a problem that you could use gradient descent on. Try to think of your own stuff, I'm more interested in seeing an example not available on the internet. 
* Bonus: Can gradient descent help for problems related to sequences over finite fields? A finite field is a set with the normal arithmetic operations (add,sub,mult,div). Given a starting sequence, can we use gradient descent to determine what the next element in a sequence might be? For example, [given a long list of numbers over](https://groupprops.subwiki.org/wiki/Cyclic_group:Z4)  $\mathbb{Z}_4 $: $[1,1,1,2,2,0,3,\dots]$ ? What alternatives exist?



