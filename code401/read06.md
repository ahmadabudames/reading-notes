## How to use the Random Module in Python
#### Overview
***In this post, I would like to describe the usage of the random module in Python. The random module provides access to functions that support many operations. Perhaps the most important thing is that it allows you to generate random numbers.***

> When to use it?
***We want the computer to pick a random number in a given range Pick a random element from a list, pick a random card from a deck, flip a coin etc. When making your password database more secure or powering a random page feature of your website.***

> Random functions
***The Random module contains some very useful functions.***

> Randint
***If we wanted a random integer, we can use the randint function Randint accepts two parameters: a lowest and a highest number. Generate integers between 1,5. The first value should be less than the second.***

> import random
***print random.randint(0, 5)***

***This will output either 1, 2, 3, 4 or 5.***

> Random
***If you want a larger number, you can multiply it.***


> Shuffle
***The shuffle function, shuffles the elements in list in place, so they are in a random order.***


> Randrange
***Generate a randomly selected element from range(start, stop, step)***

***random.randrange(start, stop, step)***

import random
for i in range(3):
    print random.randrange(0, 101, 5)
Why use Risk Analysis?
In any software, using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks. When a test plan has been created, risks involved in testing the product are to be taken into consideration along with the possibility of the damage they may cause to your software along with solutions.

Now, you might think what could be the possible risks that you could encounter? Well here is a list:

- Use of new hardware

- Use of new technology

- Use of new automation tool
The sequence of code
Availability of test resources for the application
Now, you must know there are certain risks that are unavoidable. I am enumerating them below:

The time that you allocated for testing

A defect leakage due to the complexity or size of the application

Urgency from the clients to deliver the project

Incomplete requirements

In such cases, you have to tackle the situation with care. Following points can be taken care of:

Conduct Risk Assessment review meeting

Use maximum resources to work on high-risk areas

Create a Risk Assessment database for future use

Identify and notice the risk magnitude indicators: high, medium, low.

Now, what are these risk magnitude indicators? Well, here is an explanation.

- High: means the effect of the risk would be very high and non-tolerable. The company might face loss.

- Medium: it is tolerable but not desirable. The company may suffer financially but there is a limited risk.

- Low: it is tolerable. There lies little or no external exposure or no financial loss.


