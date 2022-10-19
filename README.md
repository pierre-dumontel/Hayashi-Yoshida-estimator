# High frequency brownians and Hayashi-Yoshida estimator

# Authors
Dumontel Pierre & Rouet William
Master's Degree Finance Quantitative & Insurance \ 
Aix-Marseille School of Economics

# Syllabus

The aim of this study is to analyze the Epps effect which states that the correlation between returns depends on the sampling frequency and asynchronous sampling. Moreover the correlation is decreasing with the data frequency. 

For this study we’ll consider two correlated Brownian motions Xt and Yt that we’ll estimate over different windows of different frequencies in order to analyze the correlation between them in all these cases. 

We’ll also introduce the Hayashi-Yoshida covariance estimator that will allow us to obtain a non-biased correlation estimator while taking into account asynchronous trading. 

We can expect from the results that the correlation between Xt and Yt will be decreasing with the trading frequency especially when we’re going to model asynchronous trading. 

# Correlation between two Brownian motions with a 3-months window of daily observations and a 90-seconds window with a frequency of one second

### Brownian motions : 

Throughout our study we’ll consider two correlated Brownian motions : Xt = x Wt1 and Yt =y Wt2 . With Wt1 and Wt2 two centered Gaussian processes that also respect the properties of Martingale and Markov processes assuming W01= 0  and W02= 0. 

In financial econometrics Brownian motions are used to model financial returns since both are random and share some important properties like the fact that the expected returns of a Brownian motion are independent of the value of the process or the similarity between the path of Brownian motion and the behavior of returns. 

### Monte Carlo experiments : 

We used Monte Carlo method, which is a method of repeated random sampling, in order to generate multiple draws of our two Brownian motions Xt and Yt. The use of this method will allow us to compute our correlation estimators over a significant sample of results. We made 100 paths per motion and we worked over two different windows : a three months window with daily observations and a ninety seconds window with a frequency of one second. So for the two windows we have obtained ninety observations beginning at zero.
We observe on the graphs that our paths seem to be “bounded” and as expected totally random and unpredictable. 

### Pearson correlation estimator :

As previously said the aim of our study is to analyze the correlation between two Brownians in different conditions. The correlation will show us the strength with which our Brownians are varying together and the direction of the relationship. The first correlation estimator that we’ll use is the Pearson estimator which is the most common one. It’s a parametric estimator which allows measuring linear correlation. 
We observe from the results that the Pearson correlation estimators between our Brownians are very close in mean and in variance considering one window or another. However, we can see from the skewness that the distribution of the correlation is centered considering the ninety seconds window and right skewed considering the three months window. We can also state from the kurtosis that the distribution of the correlation is fatter in the case of the three months window than in the case of the ninety seconds window. All these results can be graphically observed thanks to the distribution shown above the table. 
Considering these results we can’t observe the Epps effect without asynchronous data while taking into account the Pearson correlation estimator. 

### Kendall correlation estimator :

We’ll now consider the Kendall correlation estimator. This is a nonparametric estimator that measures monotonic relationships. The information used by this method is only concerning the number of concordant and discordant pairs.
The conclusions we can draw from the results are very similar to those given by the Pearson estimator. The correlation between the two Brownians are very close in mean and in variance while the correlation distribution is more centered in the case of the ninety seconds window. We can also see that both distributions have fatter tails than the normal distribution. As previously with the Pearson estimator we can’t observe the Epps effect given the fact that, in mean, the correlation of the Brownians with a daily frequency and with a frequency of one second are quite the same. 
If we compare the correlation estimations given by Kendall's tau and by  the Pearson estimator there are some differences that we can spot. First, the correlations are on average lower using Kendall’s tau and also less variable. We can also see that the correlation distributions are less centered with the Kendall’s tau than with the Pearson estimator. Lastly, we can observe fatter tails in the correlation distributions using Kendall’s estimator compared to the Pearson’s one. These differences of results may be explained by the differences between the estimators themselves previously stated such as the fact that Kendall’s tau, which allows estimating monotonic relationships, is nonparametric contrary to the Pearson estimator which allows estimating correlation between linear relationships. 

# Correlation between two Brownian motions taking into account asynchronous samplings :
### Asynchronous sampling

Contrary to the first part of this study we will not consider anymore constant frequencies for the paths generation of our Brownian motions. Previously we considered time windows of ninety days and ninety seconds with constant frequencies of respectively one day and one second. Now we’ll still consider the same sizes of the time windows but with changing frequencies between the simulations. In order to do so we have simulated ninety uniforms on [0,1], cumulated them to have an increasing process and normalized it on [0,90/365] for the ninety days window and on [0,90/(365*24*60*60)] for the ninety seconds window. 

Thanks to this method we obtained four asynchronous time axes, one per time window and per Brownian. And importantly, these observation times are assumed independent of each other and of the Brownian motions. That allowed us to perform our Monte Carlo experiments as previously explained in the first part. 
The use of asynchronous trading will help us to analyze one of the results stated by Epps. This result is the fact that the Epps effect is mainly due to asynchronous sampling. This could be a reason why in the first part we haven’t observed the Epps effect. We’ll try to observe it thanks to the following correlation estimators.

### Pearson and  Kendall correlation estimators 

Since those correlation estimators have already been defined, we can go directly to  the results obtained. We know that these methods will be biased in this case because of the fact that they will not take into account the asynchrony. Therefore we can expect similar results as those previously computed. 
In mean and in variance, we come back to the same conclusions as in the previous question, the Pearson correlation estimator between our Brownians are very close considering one window or another. We noticed also that means and variances are very close to those obtained with synchronous data.
However, the skewness doesn’t give the same conclusions as obtained previously,  we can see that the distribution of the correlation is right skewed considering the ninety seconds window and centered considering the three months window. 
Finally, we can state again from the kurtosis that the distribution of the correlation is fatter in the case of the three months window than in the case of the ninety seconds window. Those coefficients are close to those obtained in the previous part.  All these results can be graphically observed thanks to the distribution shown above the table. 
Considering these results, Pearson estimators don't capture Epps effect with asynchronous data. We will analyze Kendall’s tau and introduce Hayashi-Yoshida estimator before concluding on this point. 

The correlation between the two Brownians are very close in mean and in variance. Those results are very close to those obtained with synchronous times. We can also see that both distributions have fatter tails than the normal distribution. We can also state that they are right skewed. Both the skewness and the kurtosis are substantially higher considering the ninety seconds window than the three months  window whereas with synchronous times it was the other way around. 

Here again we can’t observe the Epps effect given the fact that, in mean, the correlation of the Brownians with a daily frequency and with a frequency of one second are quite the same as it was with  the Pearson estimator. 
Between the correlation estimations given by Kendall's tau and by the Pearson estimator there are some differences that we can spot and compare to the previous part. First, the correlations are on average lower using Kendall’s tau and also less variable. We can also see that the correlation distributions are less centered with the Kendall’s tau than with the Pearson estimator. Lastly, we can observe fatter tails in the correlation distributions using Kendall’s estimator compared to the Pearson’s one. The explanations between these differences of results may be the same as before.
But what is more interesting here, is the fact that those estimators are very similar in mean and variance whether we use synchronous or asynchronous times. In their calculations, those estimators do not take into account the fact that time is asynchronous. That is why we will introduce the  Hayashi-Yoshida estimator. 

### Hayashi-Yoshida correlation estimator

This estimator is a specific one for non-synchronous processes. As the Pearson estimator, it is computed like the quotient of  the covariance on the product of standard deviations but taking into account the fact that time is asynchronous. The article https://papers.ssrn.com/sol3/papers.cfm?abstract_id=2225753 explains well how this estimator is implemented.

Here, two intervals of times of Xt have an intersection with the same interval of time of Yt. So, what the Hayashi-Yoshida correlation estimator does is to compute the covariance between Xt and Yt when the time intervals of these two processes cross. This modified covariance is then divided by the product of the modified standard deviations of Xt and Yt.
We can observe from these results that the Hayashi-Yoshida correlation estimator between our Brownians are proportional in mean and in variance considering their window. That means in average, the smaller the window is, the smaller the correlation is and the less it’s dispersed from the mean. We can see from the skewness that the distribution of the correlation is right-skewed considering both windows. We can also state from the kurtosis greater than three that the distributions of the correlation are both leptokurtic. We clearly see that this effect is predominant in the case of the three months window. 
All these characteristics can be seen on the histogram of the correlation distributions. We can also clearly spot on this graphic the Epps effect thanks to the peak of the correlation distribution considering the ninety seconds interval. The Hayashi-Yoshida covariance estimator is even more biased towards zero in this case than in the case of the ninety days interval. 

# Resume 

Considering these results we observe the Epps effect in the case of  asynchronous data thanks to the Hayashi-Yoshida correlation estimator. We clearly see that this estimator is biased towards zero when taking into account asynchronous data and that it allows us to see the decrease of correlation with the trading frequency. This wasn’t observable previously with the Pearson and the Kendall estimators that were unable to take into account the asynchrony. 
