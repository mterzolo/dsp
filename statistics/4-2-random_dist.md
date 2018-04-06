[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

>> rand_nums = np.random.random(1000)

>> rand_pmf = thinkstats2.Pmf(rand_nums, label='first')

>> rand_cdf = thinkstats2.Cdf(rand_nums)

>> thinkplot.Pmf(rand_pmf)

>> thinkplot.Cdf(rand_cdf)
