# Future of NBA Three Pointer
Otis Jones, Yerem Istanboulian, Danny Baerman, Ryan Quon, Sonali Mayer

# Abstract:
Our project focuses on finding the optimal percentage of shots taken from 3 in an NBA game given the current rules. We took data of field goal percentage from .csv files on basketballreference.com, the data was of field goal percentage for different regions on the court and different defender distances. The closer the defender is to the shooter the worse the field goal percentage. We developed a stochastic model in python to find the optimal percentage of shots to take from 3. We sampled 2 pointers and 3 pointers from the data we had and allowed the offense and defense to adjust their strategies. Eventually we found an equilibrium between shooting twos and threes.

# Motivation:
The NBA shoots more three pointers each year. Starting around 2012 the number of 3 point Attempts per 100 possesions has been rapidly increasing. The expected value of the 3 pointer did not drop significantly even though there have been more attempts. This raises the question when will the percentage of 3 point shots plateau.

# Methodology - Data:
We gathered basketballreference.com data

# Methodology - Data Analysis:
Since the introduction of the three point shot in 1979 the number of three point attempts steadily increased until roughly 2010 when there was a sudden dramatic rise in three point attempts which has continued to this day.To examine why three point attempts have been on the rise, we first looked at the expected value of both threes and twos over time using data from Basketball Reference. We cross-referenced these plots with a list of rule changes to see what trends could be explained by new rules. 

# Methodology - Simulation:
We developed a Stochastic simulation based on the data of 3 point and two point shots based on defender distance. The simulation is of a series of plays between the offense and defense. Using the defender distance data we have the probiblity of making a 2 or 3 pointer given the distance of the defender. We have turned this into a linear model of the probibility of making a shot given effort of the defense. In the simulation the defender can partician its efforts in different ways to effect two and three pointers. If the three pointer is wide open then the offense will make its three point shots 38% of the time. If the defense has all of its efforts on the 3 pointer then they will make the shot 24% of the time. If the defense gives half of its efforts on gaurding the three pointer the offense will make its threes 38-((38-24)/2) = 31% of the time. The same thing is happening with two pointers but with different numbers.
  The simulation simulates a bunch of plays where the offense either shoots a two or a three depending on a random number generator. In the begining the offense has a 10% chance to shoot a 3 and a 90% chance to shoot a 2. Initially the defense is initially focusing 90% of its efforts on the 2 pointer and 10% on the 3 pointer. After 1000 plays the offense and defense both update their strategies. If the expected value of the three pointer is greater than the expected value of the two pointer then the offense will shoot slightly more three pointers and vice versa. If the expected value of the three pointer is greater than the expected value of the two pointer then the defense will put slightly more of their effort on guarding the three pointer and vice versa. If the two expected values are very close the offense and defense will only slightly change their strategies but if the expected values are far apart they will change their strategies more aggresively. So eventaully the offense will find its best strategy and the defense will find its best strategy and there will be an equilibrium.

# Key Results:
This is a graph with the number of plays on the x-axis and the fraction of shots from three on the y-axis. We can see that it seems to be converging to shooting around 42% of the shots from three.
<img width="460" alt="Screen Shot 2019-12-24 at 2 42 20 PM" src="https://user-images.githubusercontent.com/46733087/76170755-1ff35d00-6142-11ea-8c5c-fed41c0ec076.png">


# Summary:


# Future Work:


