# Power-Allocation-in-NOMA-using-Machine-Learning


##INTRODUCTION

The major purpose of our project is the allocation of power to the users from
multiple base stations relying on the position of the user from the nearby base station
as well as the signal strength of that user. To achieve our goal, we will use a machine
learning algorithm for power division and reduce the overhead of CSI. In this project,
we have created a base station and allocated power to two users depending on their
signal strength.This was done by finding the outage probability that is number
of outage per iteration. Machine learning algorithms such as Linear Regression,
Support vector machine and Decision tree were used for power allocation. Support
vector machine gave us suitable results. Outage probability was found based on
these predictive models. Comparison was made with the fixed power outage and
predictive power outage. Outage probability of predictive model was lesser which
means user fairness was achieved.


##PROBLEM STATEMENT

Providing Power Allocation in NOMA Using Machine Learning techniques to Achieve
User Fairness. We are using Machine learning to decrease overhead caused due to
CSI collection of a massive number of users. For this project, we are considering two
users and one base station for tractability. Later on, this model can be generalized
for more number of base stations and/or users.

##METHODOLOGY

The main topics of this work were NOMA, interference suppression, silicon carbide,
NOMA simulation, NOMA detector, signal coding, two-segment signal shift keying, and DPC. Nonorthogonal multiple access (NOMA) systems that offer extended
potential have detection problems because of person interference in uplink (UL)
conditions. Inter-consumer interference (IUI) or inter-antenna interference (IAI)
is caused by successive interference cancellation (SIC) mistakes while transmitting
and receiving signals from a couple of antennas. SIC uses an inverse permutation
technique to reduce its IUI, while dirty Paper Coding (DPC) minimizes IAI by using diagonalizing the channel matrix. In this painting, the use of known channel
kingdom statistics, a blended His DPC-OSIC detector is proposed for performance
evaluation of UL-NOMA-MIMO (CSI) structures. All constellations observe to the
user with the lowest channel gain, whilst its QR-based OSIC lowers its IUI. The
proposed joint DPC-OSIC is considered through the joint performance of DPC-ZF
and DPC-ML. Simulation consequences verify that the proposed detector achieves
near maximum likelihood (ML) performance with enormously low complexity. Maximum chance statistics approximately the channel nation became received by means
of simulation, which additionally reduced the SIC blunders. This test additionally
meets the channel gain requirement.

For finding the outage probability of fixed power user, we used terminologies which
are given below
• Transmitted SNR <br>
• Received SNR for cell-center user (CCU) and cell-edge user (CEU) <br>
• Fading <br>
• Total Channel gain <br>
• Outage of CCU and CEU <br>

### Collecting Data
  For this work, we created a synthetic data set in which we assumed there is one
user, one base station, and a different scenario of it. The data set contains around
109 observations with 6 different attributes. A single word (row) corresponds to one
user scenario, and the attributes are variables in the data set about obstacles that
are in between the user and the base station. If trees are coming between them then
the value of the tree is 1 otherwise zero. Similarly, for cars, humans, and buildings
if they are coming user and base station, then values of them as one, otherwise zero.
In this dataset, there is one attribute which is coverage. If the user is within the
coverage of the base station, then the value of coverage is one, otherwise, it will be
zero. Target data is power. So, we will predict power for new data.

###NOMA Techniques
  In this NOMA concept, we are going to distribute power to the user which is connected to the base station. In between some users and base stations, there are some
obstacles are there. That’s why it may affect network connectivity.
First, we are going to find fading and total fading for each user

                         Fading = random exponential value
                         Total fading = Fading * (distance)−3

Where distance = distance between the base station and user And 3 = path lost
variable. Now we got the total fading to each user.
We will find outage probability for cell center user and cell edge user.
                      
                        Transmit SNR = power / noise = rho
                        cell-center SNR = rho*power*channel gain of cell center user
                        cell-edge SNR = rho*power*channel gain of cell edge user/ 1 + (rho*power*channel gain of CEU)
After finding SNR now we are going to check outage is occurring or not.

                        If ( log(1+SNR) is less than 0.1 ) then outage occurred
                        If ( log(1+SNR) is greater than 0.1 ) then outage not occurred
                                                                Where 0.1 bits/sec = target rate.

                        Outage probability = no.of outage occurred / total number of iterations

###Machine Learning
  So basically, in this scenario we have defined user is strong or weak now, it’s time
to use some machine learning algorithm to allocate the required power to each user
The model should allocate low power to the strong user and high power to the
weak user
That is how we use different methods in this project NOMA technique will define
strong users and weak users and machine learning is for allocating sufficient power
to the user.

