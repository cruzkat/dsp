[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

    def CohenD(group_1,group_2):
        wgt_diff = group_1.mean() - group_2.mean()
        first_var = group_1.var()
        others_var = group_2.var()
        pooled_variance = (len(group_1) * first_var + (len(group_2) * others_var)) / (len(group_1) + len(group_2))
        d = wgt_diff / np.sqrt(pooled_variance)
        return d

    group_1 = firsts.totalwgt_lb
    group_2 = others.totalwgt_lb

    CohenD(group_1,group_2)
    -0.088672927072602

To find Cohen's D of the first-born babies and the others, I found the difference in means of both groups. Then calculated the variance of each group. To calculate the pooled variance, multiplied the size of each group by its variance, added those 2 values together and divided by the total size of both groups. Lastly, I divided the difference in means by the standard deviations using the square root of the pooled variance.

A negative Cohen's D means that there was a mean increase between group 2 and group 1. The size of .08 is a small effect and means that there .08 standard deviations between the means of total birth weight in lbs between the first born and other birth order groups. First babies are slightly lighter than other birth order babies.