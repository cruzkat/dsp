[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

    mu = 178
    sigma = 7.7
    normal_distribution = scipy.stats.norm(loc=mu, scale=sigma)
Plots the normal distribution with the parameters of mu and sigma for the men.

    percentage_qualified = normal_distribution.cdf(185.4) - normal_distribution.cdf(177.8) 
    percentage_qualified = 0.3420946829459531
    
Finds the percentage qualified by finding the percentages of the heights 5'10" and 6'1" within the CDF and subtracting them.
We are left with the percentage qualified for the Blue Man Group which is approximately 34% of males.

5'10" to cm = 177.8  6'1" to cm = 185.4
total interviewed 414,509
