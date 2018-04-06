[Think Stats Chapter 8 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2009.html#toc77) (scoring)

lam = 2
n = 10
num_exp = 1000

estimates = []
for _ in range(num_exp):
    xs = np.random.exponential(1.0/lam, n)
    lamhat = 1.0 / np.mean(xs)
    estimates.append(lamhat)

stderr = RMSE(estimates, lam)

cdf = thinkstats2.Cdf(estimates)

ci_lower = cdf.Percentile(5)

ci_upper = cdf.Percentile(95)

thinkplot.Cdf(cdf)
thinkplot.Config(xlabel='estimate',
                 ylabel='CDF',
                 title='Sampling distribution')
