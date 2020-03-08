# Future of NBA Three Pointer
Otis Jones, Yerem Istanboulian, Danny Baerman, Ryan Quon, Sonali Mayer

# Abstract:
Our project focuses on finding the optimal percentage of shots taken from 3 in an NBA game given the current rules. We took data of field goal percentage from .csv files on basketballreference.com, the data was of field goal percentage for different regions on the court and different defender distances. The closer the defender is to the shooter the worse the field goal percentage. We developed a stochastic model in python to find the optimal percentage of shots to take from 3. We sampled 2 pointers and 3 pointers from the data we had and allowed the offense and defense to adjust their strategies. Eventually we found an equilibrium between shooting twos and threes.

# Motivation:
The NBA shoots more three pointers each year. Starting around 2012 the number of 3 point Attempts per 100 possesions has been rapidly increasing. The expected value of the 3 pointer did not drop significantly even though there have been more attempts. This raises the question when will the percentage of 3 point shots plateau.

Expected Value             | Attempts
:-------------------------:|:-------------------------:
<img width="442" alt="Screen Shot 2020-03-08 at 2 07 50 PM" src="https://user-images.githubusercontent.com/46733087/76171242-3bf8fd80-6146-11ea-9d48-ed6bc17a1942.png"> |  <img width="326" alt="Screen Shot 2020-03-08 at 2 07 56 PM" src="https://user-images.githubusercontent.com/46733087/76171252-59c66280-6146-11ea-83bb-63941ee6fe6d.png">

# Methodology - Data:
We gathered basketballreference.com and nba.com data

## Methodology - Data Analysis:
Since the introduction of the three point shot in 1979 the number of three point attempts steadily increased until roughly 2010 when there was a sudden dramatic rise in three point attempts which has continued to this day.To examine why three point attempts have been on the rise, we first looked at the expected value of both threes and twos over time using data from Basketball Reference. We cross-referenced these plots with a list of rule changes to see what trends could be explained by new rules. 

## Methodology - Simulation:
We developed a Stochastic simulation based on the data of 3 point and two point shots based on defender distance. The simulation is of a series of plays between the offense and defense. Using the defender distance data we have the probiblity of making a 2 or 3 pointer given the distance of the defender. We have turned this into a linear model of the probibility of making a shot given effort of the defense. In the simulation the defender can partician its efforts in different ways to effect two and three pointers. If the three pointer is wide open then the offense will make its three point shots 38% of the time. If the defense has all of its efforts on the 3 pointer then they will make the shot 24% of the time. If the defense gives half of its efforts on gaurding the three pointer the offense will make its threes 38-((38-24)/2) = 31% of the time. The same thing is happening with two pointers but with different numbers.
  The simulation simulates a bunch of plays where the offense either shoots a two or a three depending on a random number generator. In the begining the offense has a 10% chance to shoot a 3 and a 90% chance to shoot a 2. Initially the defense is initially focusing 90% of its efforts on the 2 pointer and 10% on the 3 pointer. After 1000 plays the offense and defense both update their strategies. If the expected value of the three pointer is greater than the expected value of the two pointer then the offense will shoot slightly more three pointers and vice versa. If the expected value of the three pointer is greater than the expected value of the two pointer then the defense will put slightly more of their effort on guarding the three pointer and vice versa. If the two expected values are very close the offense and defense will only slightly change their strategies but if the expected values are far apart they will change their strategies more aggresively. So eventaully the offense will find its best strategy and the defense will find its best strategy and there will be an equilibrium.
  
## Methodology - Time Series: 
klj;j;lj

# Key Results:
## Key Results - Simulation:
This is a graph with the number of plays on the x-axis and the fraction of shots from three on the y-axis. We can see that it seems to be converging to shooting around 42% of the shots from three.
<img width="460" alt="Screen Shot 2019-12-24 at 2 42 20 PM" src="https://user-images.githubusercontent.com/46733087/76170755-1ff35d00-6142-11ea-8c5c-fed41c0ec076.png">

We see the offense and defense are in a kind of dance where the offense overadjusts and then the defense adjusts and gets pulled back down and on and on. 

## Key Results - Data Analysis:

![image](https://user-images.githubusercontent.com/47067688/76171194-cbea7780-6145-11ea-8226-7e18b76a2d8e.png)

The number of three-point attempts per 100 possessions went up dramatically from 1994-1996. This can be attributed in part to the rule change that occured in the 1994-95 season, where the three-point line was shortened to a uniform 22 feet around the basket. In 1997, the number of three-point attempts decreased. This can most likely be attributed to the rule change that occured in the 1997-98 season, where the three-point line was lengthened to its original distance of 23 feet, nine inches, except in the corners, where the distance remained 22 feet. 


![image](https://user-images.githubusercontent.com/47067688/76171198-d3118580-6145-11ea-836b-b834adcfef22.png)


By looking at these two plots we noticed two key points:

1.The expected value of threes since about 1995 has been between 1.0 and 1.1 points per attempt whereas the expected value of twos has remained under 1 point per attempt for much of the past 30 years, making the three point shot the more efficient shot by points per attempt.

2. While the expected value of a 3pt shot has remained fairly consistent since around 2000, the expected value of a 2pt shot has fluctuated dramatically.The apparent drop in the expected value of two-point shots during the year 2000 can partially be attributed to the NBA lock-out that occurred in 1999. During the lockout, the players did not attend training camp, which undoubtedly negatively affected the points scored per 100 possessions and the expected value of a 2-point shot. The expected value of the two point shot has been increasing quite rapidly since about 2011, the same time period where we see the dramatic rise of three point attempts start to take place.

Based on these observations we hypothesize that a shift from the current strategy of taking more threes might take place when the expected value of a 2pt shot exceeds the expected value of a 3 pt shot. To further illustrate this point, the ratio of the expected value of 3pt shots to the expected value of 2pt shots is plotted below with a value over one representing the three point shot having a higher expected value.

![image](https://user-images.githubusercontent.com/47067688/76171201-da389380-6145-11ea-84af-16ce44a4bf36.png)

## Key Results - Time Series:
kjjlk;jl;jl;j

# Summary:
For our project we wanted to analyize the role that the three point shot plays in the modern NBA. We used a Stochastic model to simulated a basketball plays and allowed the offense and defense to find the best strategy, it looks like shooting 42% of your shots from 3 is the best strategy. 


# Future Work:
Do further work looking at the convergence of the Stochastic Model.

