[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> pmf = thinkstats2.Pmf(resp['numkdhh'], label='actual')

>> biased_pmf = BiasPmf(pmf, label='observed')

>> thinkplot.PrePlot(2)

>> thinkplot.Pmfs([pmf, biased_pmf])

>> thinkplot.Config(xlabel='Number of Siblings', ylabel='PMF')
