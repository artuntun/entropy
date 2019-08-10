## **Information Entropy**

For me, entropy has being always an elusive term to grab. Yes, no matter which field, I have being told that it's a measurement of disorder. Great. But how shannon entropy represents information disorder? What does it even mean information disorder? why this specific formula? and who invited the logarithms to this party? After checking several sources, I wasn't very convince by any explanations. Until I went to the original source: Shannon paper published in 1948, _"A Mathematical Theory of Communication"_

So let's start by dissecting the equation:

<p align="center"><img src="/tex/a732669b3b57f5ae74ecd7068fefff40.svg?invert_in_darkmode&sanitize=true" align=middle width=132.74918085pt height=36.6554298pt/></p>

### Shannon unit of information
First of all we should note about the term **<img src="/tex/ac7b5d6269a2c23be76e2fa2b9e9ef5c.svg?invert_in_darkmode&sanitize=true" align=middle width=34.548219749999994pt height=22.831056599999986pt/>**. It might seems weird to have a logarithm of a probability and indeed it is but remember, Shannon was a genius so there must be something behind it. Let me just give you the dogmatic answer: the term represents **conveniently** quantity of information.
Not satisfy? Do you want proves and reasons? You are not a good believer. But hold on, I will convert you to the Shannon church. 

Imagine that you had a communication system where the number of messages would be finite and each option would be equally likely to be chosen. This number can be regarded as a measurement of the amount of information transmitted every time a message is sent. 

GRAFICA con 3 mensajes. Equally likely. 

Every time that a message is sent, 3 units of information are transferred. Now what happen if the probabilities were not equal?

GRAFICA con 3 mensajes unbalanceados. 

The first message, 'yes', is sent half percent of the times or in other words, 1 out of 2 times. On the other hand, 'no' and 'maybe' are sent one fourth of the times. Following with the already defined measurement, the first message generate 2 units of information while the latter two 4. The messages with lower probability encode more information, because they are removing more uncertainty. Let's say that we had a machine that tells you every 5 minutes if the sun has exploded or not. A negative answer is what you expect, does not contain much information. The opposite will blow you mind, it will tell you muuuuuch more(for at least 8 minutes).

Good, now we can measure quantity of information based on probabilities. The magic comes with logarithms. In practice we can apply any monotonic function to _N_, and will still be a valid measurement as will maintain the same hierarchy i.e. <img src="/tex/e6eb2220a17b77c1f215341d7133e5c3.svg?invert_in_darkmode&sanitize=true" align=middle width=155.45260499999998pt height=22.831056599999986pt/>. But look at this. Let's plug directly the probabilities in the logarithms, instead of the clumsy ratio.

<p align="center"><img src="/tex/e72e2a0d95a22650fc02af57061db0fa.svg?invert_in_darkmode&sanitize=true" align=middle width=234.38474234999998pt height=32.990165999999995pt/></p>
<p align="center"><img src="/tex/dfcd66d1c3a121b97f56c80206f1d4fa.svg?invert_in_darkmode&sanitize=true" align=middle width=226.16553134999998pt height=32.990165999999995pt/></p>

With the logarithms we can use the directly the probabilities, and maintain the the hierarchy in the information scale. Congratulations, you are an initiated in Shannon church. This is the so called, shannon unit of information

<p align="center"><img src="/tex/b1b592e241b3efc21a7a2b6cccc3cd38.svg?invert_in_darkmode&sanitize=true" align=middle width=266.03651579999996pt height=14.611878599999999pt/></p>

The advantages of using logarithms is not merely being able to use probabilities. The logarithmic is nearer to the intuitive feeling as a measurement. In general, the number of possibile states of a system tend to vary linearly with the logarithm of the parameters. For example, if we encode information using thebinary system every time we add a new bit we are doubling the possible messages we can send. The number of possible messages grows exponentially. **maybe here using a more interesting exmple**

![Exponential vs linear growth](logvsexp.png)

### Tie everything together

Having a measure of quantity of information for a single message the only thing left is to measure the amount of information produced by the whole system. For example, imagine a weather station which is producing every day a prediction. Imagine that the only possible scenarios are _sun_, _rain_, _snow_, and _cloudy_. And now imainge that the weather station is in Malaga. The probabilities for each case will look like 

GRAFICA 

I wonder if it has ever snow in Malaga. Actually I have just googled it. There is an article talking about _"that time when it snowed in Malaga in 1954"_. So yes, I guess 0,1 percent is actually too much. For each scenario the radio station tansmits different amount of information: 

<p align="center"><img src="/tex/114f4f4bd9b3366121d84abe9e09c727.svg?invert_in_darkmode&sanitize=true" align=middle width=193.70815034999998pt height=14.611878599999999pt/></p>
<p align="center"><img src="/tex/81b444f9299c187af86d0188b5dbc18a.svg?invert_in_darkmode&sanitize=true" align=middle width=208.77668294999998pt height=14.611878599999999pt/></p>
<p align="center"><img src="/tex/baea564fd83883a6ce55a61a334b5123.svg?invert_in_darkmode&sanitize=true" align=middle width=174.75828315pt height=14.611878599999999pt/></p>
<p align="center"><img src="/tex/7307dbfc35313c35c1352d5d7bc2553a.svg?invert_in_darkmode&sanitize=true" align=middle width=195.0779853pt height=14.611878599999999pt/></p>

As expected the _Snow_ case is much more informative for the Malaga citizens while _Sunny_ is their everyday bread and butter. But how much information does the station transmits on average? That is the entropy.

<p align="center"><img src="/tex/3b5cffda4a3b14b35ff0a29ff8d0e132.svg?invert_in_darkmode&sanitize=true" align=middle width=150.92261084999998pt height=36.6554298pt/></p>
<p align="center"><img src="/tex/365456d2315e925bfa8ad10a8681fc2b.svg?invert_in_darkmode&sanitize=true" align=middle width=515.7307617pt height=16.438356pt/></p>

1,136 bits of information are produced on average. That is what the entropy means if we put in words _"amount of transsmited information of the system on average"_. Now you may wonder, is it Malaga radio station a entropic system? If you did so, that would be weird. But let's keep that example, let's move to Copenhaguen. I bet that weather is station is busy. There is a saying in Denmark, _"don't leave home without your swimming suit, your coat and your umbrella"_. I might have just invented that, but, yeah, the weather is definetly entropic. Let's assume the following.

<p align="center"><img src="/tex/e1e1abd0babe3d3d61e86da750ffc856.svg?invert_in_darkmode&sanitize=true" align=middle width=169.96384845pt height=14.611878599999999pt/></p>
<p align="center"><img src="/tex/20da1fe325e4525d814d7f2ef50ca7f1.svg?invert_in_darkmode&sanitize=true" align=middle width=200.55747359999998pt height=14.611878599999999pt/></p>
<p align="center"><img src="/tex/dd63d8ab29b51e6700cfda35ce68aab7.svg?invert_in_darkmode&sanitize=true" align=middle width=159.2331906pt height=14.611878599999999pt/></p>
<p align="center"><img src="/tex/56f90ac5ccd67f95a07190ac775a3ce9.svg?invert_in_darkmode&sanitize=true" align=middle width=178.6395666pt height=14.611878599999999pt/></p>

Skipping the boring calucaltions the entropy amounts to **1,98 bits of information**. That is almost double. You see the amount of information for each scenario is almost the same. This an entropic system. It's a unpredictable system. It's chaotic. Let's see one more example. Consider the entropy in the case of two possibilities with <img src="/tex/2ec6e630f199f589a2402fdf3e0289d5.svg?invert_in_darkmode&sanitize=true" align=middle width=8.270567249999992pt height=14.15524440000002pt/> and <img src="/tex/6d6e973017fe8ad2e0aef068f4e2ffa3.svg?invert_in_darkmode&sanitize=true" align=middle width=66.42668504999999pt height=21.18721440000001pt/>

<p align="center"><img src="/tex/e111fdf190299671abe83d625c743941.svg?invert_in_darkmode&sanitize=true" align=middle width=189.457422pt height=16.438356pt/></p>

![Entropy of the system](Hpq.png)

Here the advantages of this metric are even more prominent. First of all the highiest peak occurs at <img src="/tex/bd4963b405fa99e5e2432efaed7e4b6c.svg?invert_in_darkmode&sanitize=true" align=middle width=81.03855869999998pt height=21.18721440000001pt/>. This is naturally the case of highiest disorder, where nothing is more predictable than anything else. It then intutively correct to associate with the moment of maximum entropy.

Similarly, another great property is the lowest entropy points at <img src="/tex/61d5974753c6aba73418ea29b31f7808.svg?invert_in_darkmode&sanitize=true" align=middle width=38.40740639999999pt height=21.18721440000001pt/> or <img src="/tex/3d05cd6211f427db37bac406f3f2bd81.svg?invert_in_darkmode&sanitize=true" align=middle width=38.06492744999999pt height=21.18721440000001pt/>. This is the extreme, where the outcome is predictable with no room for doubt. Then, again, it makes sense that the entropy is zero.

### Summing up

Entropy is just a measure of information. A very good one indeed, and we can understand it as an average of information provided by 
need to be finish


use http://worrydream.com/Tangle/ for ilustrations