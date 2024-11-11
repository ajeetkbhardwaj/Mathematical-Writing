---
marp: true
theme: gaia
class: invert
math: mathjx
size: 16:9
footer: Ajeet Kumar Bhardwaj | ajeetskbp9843@gmail.com | [Linkedin](https://www.linkedin.com/in/ajeetkumar09)

---

# Singular Value Decomposion(SVD)

---
### Clustering a Mixture of Spherical Gaussians
Clustering problems, we partition data points into k subsets of nearby points is called a k-clustering problem. How to measure the quality of clustering and find the best out of it ? We formulate
1. K-Meadian : Minimize the sum of distances
2. K-Means : Sum of squared distances

Generally both problems are NP-Hard, so we can't solve them exactly but there are two ways to deals with NP-hardness
1. Approximately optimal solution, 
---
this is what we focus on operational research but there is a problem if we do $\epsilon$ change in parameter then the result will become useless

2. Assume stochastic models of data, what do we  mean by stochastic model ? It is the hidden model that generates the data, we don't want it to be approximately but it should model it exactly as hidden model generated it.

What are Mixture models ?
Mixture models are importent class of the stochastic models, Let's take $p_1(x), p_2(x) \dots, p_k(x)$ be k probability density functions then mixture of these k-densities will be $f(x) = w_1p_1(x) + w_2 p_2(x) + \dots + w_k p_k(x)$

---
where $w_1, w_2, \dots, w_k \ge 0 \; and \; \Sigma_{i=1}^{k} w_i p_i(x) = 1$ are weights associated to each densities resp.

**What is Learning Problem ?**
> Given n identically independently distributed samples from a mixture, we have to learn the mixture i.e $w_i \; \& \; p_i(x)$. The class of basic densities is known but not what specific members of the class generation used like spherical gaussians.

What are equivalent ways of how hidden hand generates samples which gives sample properites as distribution ?

---
1. Pick each sample according to mixture $f$ on $R^d$ i.e density generates i.i.d samples
2. Pick $i$ from $\{1, 2, \dots, k\}$, probability of picking $i$ is $w_i$ then pick $x$ according to $p_i$ for each $i$.

Now, learning problem(model fitting problem) has 2 subproblems
1. Cluster data into k clusters according to which $p_i$ generated sample.(hard)
2. Fitting one gaussian to each cluster(easy)

**Means seperated by $\Omega(1)$ standard deviations**

---
* If component gaussians have centers very close togather then clustering impossible.
* 