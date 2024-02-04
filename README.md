# dsei2100s23hw1p6-Bayes-Error
Classification of 1-D data and Bayes Error

## HW1 P6: Classification of 1-D data and Bayes Error

Suppose we have two populations of beans. The weights of these beans are normally distributed, so if $\mu$ is the mean weight of one type of beans beans and $\sigma$ is the standard deviation, so that means that the probabilty density is given by 
    
$p_{\mu,\sigma}(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-\frac{1}{2\sigma}(x-\mu)^2}$

and then the probability of measuring a weight in interval $I=[x_1,x_2]$ of bean of that type is given by

$P_{\mu,\sigma}(I) = \int_{x_1}^{x_2} p_{\mu,\sigma}(x) dx$

The mean weight of bean type A, $\mu_A$ is 5 grams and the standard deviation, $\sigma_A$, is 2. The mean weight of bean type B, $mu_B$, is 4 grams and has a standard deviation $\sigma_B$, of  1.4.

Our classifier $C_T(x)$ is determined by a weight threshold $T$:

$f\_T(x) = -1 \mbox{ if } x \leq T $

$f\_T(x) = 1  \mbox{ if } T < x  .$

The [*Bayes error*](https://en.wikipedia.org/wiki/Bayes_error_rate) is the probability that we will misclassify. Assume  that there are equally many beans of each type (no prior).

a. For a given T write down the theoretical expression (in terms of integrals) for the probability that you will classify a point as bean type A when it is bean type B and similarly that it is bean type B when it is bean type A.

b. In python just using numerical functions (you can take 1000 data points from min of weight x=1 to x=8) compute the theoretical probabilities from part a. Use matplotlib to make a curves showing the probability of classifying something class A ($\hat{C}=A$ )assuming it is really class B $C=B$, in other words $P(\hat{C}=A| C=B)$ is the figure y-axis, as a function of $T$, the figure x-axis. Similarly plot $P(\hat{C}=B| C=A)$ as a function of $T$. Putting these together since $P(A)=P(B)=1/2$, adding the curves and dividing by 2 you get the probability of miss-classification or Bayes error as a function of $T$. Plot that as well. 

c. Use the numpy random.randn to simulate 10000 data points, 5,000 from bean type A and 5,000 from bean type B. You can now pick 1000 values of $T$ using linspace between $T=1$ and $T=8$. For each of these you can compute the miss classification rate. Make the figure. These should match closely your results for $b$ above.

This problem should be a Jupyter notebook with markdown explaining each of your steps. In all cases seed your random numbers for reproducibility.
