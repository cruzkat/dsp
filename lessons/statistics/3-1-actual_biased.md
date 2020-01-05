[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

    resp = nsfg.ReadFemResp()

    pmf = thinkstats2.Pmf(resp.numkdhh, label = 'numkdhh')
    thinkplot.Pmf(pmf)
    thinkplot.Config(xlabel = 'Number of Children', ylabel = 'PMF')
    
Plots the PMF of the variable 'numkdhh' from the NSFG data.

    def BiasPmf(pmf, label):
       new_pmf = pmf.Copy(label=label)
       for x, p in pmf.Items():
           new_pmf.Mult(x, x)
           new_pmf.Normalize()
    return new_pmf
    
Function to create a Bias PMF by multiplying each value's probability by the value. Then, to get the PMF back to 1, we normalize the data by dividing by the new total probability.

    biased = BiasPmf(pmf, label = 'biased')
    thinkplot.PrePlot(2)
    thinkplot.Pmfs([pmf, biased])
    thinkplot.Show(xlabel = 'Number of Children', ylabel ='PMF')
  
Plots the 'numkdhh' actual and the biased. The biased plot shows that the data is skewed and especially for 0 children because only families with children were sampled.

    pmf_mean = pmf.Mean()
    biased_mean = biased.Mean()
    print(pmf_mean, biased_mean)
    
1.024205155043831, 2.4036791006642817

The biased mean is higher than the actual mean.


