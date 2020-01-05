[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

    sample = np.random.random(1000)
Creates 1000 random numbers uniformly distributed between 0 and 1.

    sample_pmf = thinkstats2.Pmf(sample)
    thinkplot.Pmf(sample_pmf, linewidth = 0.1)
    thinkplot.Config(xlabel='Random Variates',ylabel = 'PMF')
    
Plots the PMF of these 1000 random variates.

    sample_cdf = thinkstats2.Cdf(sample)
    thinkplot.Cdf(sample_cdf)
    thinkplot.Show(x_label = 'Random Variates', ylabel ='CDF')

Plots the CDF of these 1000 random variates.

Since the CDF is approximately a straight line, it means that the numbers are uniformly distributed.