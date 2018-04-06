[Think Stats Chapter 7 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2008.html#toc70) (weight vs. age)

thinkplot.Scatter(live['totalwgt_lb'], live['agepreg'], alpha=1.0)

bins = np.arange(10, 48, 3)
indices = np.digitize(live['agepreg'], bins)
groups = live.groupby(indices)

ages = [group.agepreg.mean() for i, group in groups][1:-1]
cdfs = [thinkstats2.Cdf(group['totalwgt_lb']) for i, group in groups][1:-1]

thinkplot.PrePlot(3)
for percent in [75, 50, 25]:
    weights = [cdf.Percentile(percent) for cdf in cdfs]
    label = '%dth' % percent
    thinkplot.Plot(ages, weights, label=label)

thinkplot.Config(xlabel="Mother's age (years)",
                 ylabel='Birth weight (lbs)',
                 xlim=[14, 45], legend=True)

Corr(live['totalwgt_lb'], live['agepreg'])

SpearmanCorr(live['totalwgt_lb'], live['agepreg'])
