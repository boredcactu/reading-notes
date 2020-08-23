# Game of Greed 1

## Random Module in Python
---
  > ***Overview:***

  In this post, I would like to describe the usage of the random module in Python. The random module provides access to functions that support many operations. Perhaps the most important thing is that it allows you to generate random numbers.

  >***When to use it?***

  We want the computer to pick a random number in a given range Pick a random element from a list, pick a random card from a deck, flip a coin etc. When making your password database more secure or powering a random page feature of your website.

  ### Random functions:
  The Random module contains some very useful functions, and i will mintion some of them:

  1- ***Randint***

  If we wanted a random integer, we can use the randint function Randint accepts two parameters: a lowest and a highest number. Generate integers between 1,5. The first value should be less than the second.

  ```
    import random
    print random.randint(0, 5)

  ```

  For example, a random number between 0 and 100:

  ```
    import random
    random.random() * 100
  ```

  2- ***Choice***

  Generate a random value from the sequence sequence.
  ```
    random.choice( ['red', 'black', 'green'] ).
  ```
  The choice function can often be used for choosing a random element from a list.

  ```
    import random
    myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
    random.choice(myList)
  ```

  3- ***Shuffle***

  The shuffle function, shuffles the elements in list in place, so they are in a random order.

  ```
    from random import shuffle
    x = [[i] for i in range(10)]
    shuffle(x)

    Output:
    # print x  gives  [[9], [2], [7], [0], [4], [5], [3], [1],  [8], [6]]
    # of course your results will vary
  ```
  4- ***Randrange***
  
  Generate a randomly selected element from range(start, stop, step)
  ```
    random.randrange(start, stop[, step])
    import random
    for i in range(3):
    print random.randrange(0, 101, 5)
  ```
---




## Risk Analysis

---

  The probability of any unwanted incident is defined as Risk. In [Software Testing](https://www.edureka.co/blog/what-is-software-testing/), risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test. After that, the process of assigning the level of risk is done. The categorization of the risks takes place, hence, the impact of the risk is calculated.

  ### Why use Risk Analysis?

  In any software, using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks. When a test plan has been created, risks involved in testing the product are to be taken into consideration along with the possibility of the damage they may cause to your software along with solutions.

  ### Risk Identification

  There are different sets of risks included in the risk identification process. Those are as follows:

  * Business Risks: This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.

  * Testing Risks: You should be well acquainted with the platform you are working on, along with the software testing tools being used.

  * Premature Release Risk: a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required

  * Software Risks: You should be well versed with the risks associated with the software development process.

  After identifying the risks associated with your software, the next step is to assess the risks; i.e, Risk Assessment.

  ### Risk Assessment

  In the risk analysis process, these steps prove to be the most important one. It is said that this step is way too complex and should be tackled with the utmost care. After risk identification, assessment has to be dealt programmatically. There are a few perspectives on risk assessment. Read on!

  ### The perspective of Risk Assessment
  There are three perspectives of Risk Assessment:

  * Effect
  * Cause
  * Likelihood
 
  ### How to perform Risk Analysis?
  There are three steps:

  * Searching the risk

  * Analyzing the impact of each individual risk

  * Measures for the risk identified

With this I have reached towards the end of this blog, I hope that the content explained added value to your Java knowledge. We will keep exploring the Java world together. Stay tuned!
---

## ***references:***
1. [Random Module](https://www.pythonforbeginners.com/random/how-to-use-the-random-module-in-python)
1. [Risk Analysis](https://www.edureka.co/blog/risk-analysis-in-software-testing/#RiskIdentification)


Done
---
 
[home](../README.md) | [About me](../about-me.md) | [contact me](../contact-me.md)