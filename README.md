# High frequency brownians and Hayashi-Yoshida estimator

# Author 
Dumontel Pierre & Rouet William
Master's Degree Finance Quantitative & Insurance, Aix-Marseille School of Economics

# Syllabus

The aim of this study is to analyze the Epps effect which states that the correlation between returns depends on the sampling frequency and asynchronous sampling. Moreover the correlation is decreasing with the data frequency. 

For this study we’ll consider two correlated Brownian motions Xt and Yt that we’ll estimate over different windows of different frequencies in order to analyze the correlation between them in all these cases. 

We’ll also introduce the Hayashi-Yoshida covariance estimator that will allow us to obtain a non-biased correlation estimator while taking into account asynchronous trading. 

We can expect from the results that the correlation between Xt and Yt will be decreasing with the trading frequency especially when we’re going to model asynchronous trading. 

# Correlation between tow Brownian motions with a 3-months window of daily observations and a 90-seconds window with a frequency of one second

Throughout our study we’ll consider two correlated Brownian motions : Xt = x Wt1 and Yt =y Wt2 . With Wt1 and Wt2 two centered Gaussian processes that also respect the properties of Martingale and Markov processes assuming W01= 0  and W02= 0. 

In financial econometrics Brownian motions are used to model financial returns since both are random and share some important properties like the fact that the expected returns of a Brownian motion are independent of the value of the process or the similarity between the path of Brownian motion and the behavior of returns. 

Monte Carlo experiments : 

We used Monte Carlo method, which is a method of repeated random sampling, in order to generate multiple draws of our two Brownian motions Xt and Yt. The use of this method will allow us to compute our correlation estimators over a significant sample of results. We made 100 paths per motion and we worked over two different windows : a three months window with daily observations and a ninety seconds window with a frequency of one second. So for the two windows we have obtained ninety simulations beginning at zero. 



