### Random Uncertainty
If you attempt to repeat your measurement you most likely will observe some spread in your measured values (you do not get an identical measurement under “identical” conditions). There will be slight and uncontrollable differences from one trial to another. These uncontrollable differences generally arise from a huge variety of detailed causes. Maybe the air conditioning happens to blow a slight puff of air on your setup the first time. Maybe a speck of lint falls onto your setup. But, however these differences arise, they cause different results when a single procedure is repeated several times. The differences don’t trend in any particular direction, and their causes are subtle and hard to identify, let alone control, in the lab – so we call them random. These variations in data cause a spread in your data.


To think through how we should treat these random uncertainties, let's look at an example thought experiment. Suppose we measure the length of an object using two different techniques/procedures, call them "Technique A" and "Technique B". Let's assume that Technique B somehow has more randomness in the measurement process (maybe the procedure for Technique B requires the experiments to occur in a dusty wind tunnel?). We can think of the experimental process as creating a theoretical probability density function with a mean $$\mu$$ and standard deviation $$\sigma$$. Each time we perform a single experimental measurement, we are sampling from these theoretical probability distributions, and suppose in our thought experiment they look like: 

![theoretical probability density function of two different experiments](images/theor-pdf.jpg)

Although the two techniques theoretically have the same mean value, Technique B has a larger standard deviation. This means that if we were to use Technique B for our experiment, we would be sampling from a broader probability distribution than if we used Technique A. 

So now let's start taking data in these two thought experiments. Suppose we took $$n=3$$ data points using each technique (with each point taken under “identical” experimental conditions), and looked at the number of times we measured each value of the length:

![experiment with 3 data points](images/exper-n3-nostats.jpg)

In these first 3 data points from each technique, we happened to have measured values between 83.4 and 83.5 cm. For each technique we calculate three important statistical quantities:

------------------------------

#### Sample mean
The sample mean is the sum of all the observed values divided by the sample size:

$$x_\mathrm{mean} = \frac{x_1 + x_2 + ... + x_n}{n}$$

#### Sample standard deviation
The sample standard deviation is (approximately) the root-mean-squared deviation of the observed values from the sample mean:

$$x_\mathrm{dev.} = \sqrt{\frac{ (x_1-x_\mathrm{mean})^2 +(x_2-x_\mathrm{mean})^2 + ... +(x_n-x_\mathrm{mean})^2}{n-1}}$$

Intuitively, the sample standard deviation represents a most likely range of values around the mean for where were would find our data. If we were taking one more data point, more than likely ($$\approx$$ 68% of the time if we are sampling from a Normal Distribution) we would expect to find that next data point within one sample standard deviation of the sample mean. 

*Tip: Google Sheets can calculate the standard deviation of your data for you by using the function STDEV().  You can read more on this [here](https://support.google.com/docs/answer/3094054?hl=en){:target="_blank"}. In MATLAB, you can use the [std function](https://www.mathworks.com/help/matlab/ref/std.html).*

#### Standard error of the mean (SEM)
The standard error of the mean represents the expected deviation of the calculated sample mean if many other samples of $$n$$ datapoints were taken. Intuitively, SEM reflects how confident we are that the sample mean is truly representative of the "actual" mean value of our distribution (what we called $$\mu$$ in our theoretical distributions; this actual mean value is also called the "population mean"). The standard error of the mean can be estimated from the sample standard deviation as:

$$\mathrm{SEM} = \frac{x_\mathrm{dev.}}{\sqrt{N}}$$

*For more information about the SEM, check out paragraph 130-131 and associated footnotes [of this document](images/Essentials-of-Statistical-Methods.pdf){:target="_blank"}.*



**Main point: our best estimate of our experimentally measured value is the sample mean, and our best estimate of its random uncertainty is the standard error of the mean. So only considering random sources of uncertainty, we would report $$x_\mathrm{mean} \pm  \mathrm{SEM}$$**
