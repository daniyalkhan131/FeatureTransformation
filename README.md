# FeatureTransformation

discretization-
Discretization is the process of transforming continuous variables into discrete variables by
creating a set of contiguous intervals that span the range of the variable's values.
Discretization is also called binning, where bin is an alternative name for interval. Why use
adv-
	To handle Outliers
﻿﻿﻿	To improve the value spread

converting numerical data to categorical data
sometimes we need to do that because it rep. better
like age in an aaplication where only young adult old works well, it is decided by seeing
the distribution.
it is problem specific
types-
	binning(disceretization)
	binarization

binning-
make bins like histogram, and then count values of occurance to assign value

by bining we can handle outliers, like very large value outlier so it comes in 1 bin(last),
and improve the spread of data

binning types-
	unsupervised:
		equal width(uniform)
		equal frequency(quantile)
		kmeans binning
	supervised: 
		decision tree binning (learn this by yourself)
	custom binning

equal width-
define bins by ourself
(max-min)/bins
and frequency count is cal.
all bars of hist. are of equal width as equal size bin

no change in spread of data, but handle outlier


equal frequency-
in this if we choose 10 bins then we go to that range where we get 10 percitile means 10%
of the data, then go range where get 20percentile and so on we do.. 
in this range can vary(not equal width)
it is considered more as good for outliers and  make value spread uniform(will get uniform hist)


kmeans binning-
it is used when our nearly data is spread in clusters
in this k means used to form clusters
and the means we got are the bins, like if k=5 then get 5 bins


use KBinsDisceretizer in sklear for using all this
parameters-
	bins
	strategy (uniform,quantile,kmeans)
	encoding(ordinal,onehot)

custom binning-
if have domain knowledge so can create own bins manually, like age into young adult old
type thing.


binarisation-
converting continuous variaboe to binary 0 or 1
like in image if >127.5 then white(1) and if <127.5 then black(0)
image convert to black n white

binarization class in sklearn
params-
	thresh
 	copy(if true then new col created)

