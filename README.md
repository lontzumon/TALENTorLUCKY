# introduction

It's often said that individuals with high IQs find it easier to succeed in their careers. However, on the other hand, we frequently see in the news that many people's affluent lifestyles stem from their large family businesses. How does one become wealthy? Is it due to innate talent or is it about seizing opportunities? This project aims to design a small-scale social simulation to test the primary reasons for becoming wealthy. Additionally, there's a common notion that 20% of the world's wealthy control 80% of the wealth. This experiment will also investigate the validity of this claim.

# Experiment Design

To investigate whether intelligence or luck has a deeper impact on acquiring wealth, we design a 2-dimensional square area as the overall environment. Individuals and events are randomly generated within this area. Below are detailed descriptions of the settings and interactions regarding individuals and events:

## Events:
1. There are two types of events: good events and bad events (each with a 50% chance of being selected randomly).
2. The location of events randomly changes every year.

## Individuals:
1. Each individual has a different level of intelligence (selected randomly from a normal distribution, and then normalized within the range of 0 to 1).
2. Each individual initially selects a random location within the area and remains there.
3. Each individual starts with $100.
4. If an individual encounters a bad event during the year (within 1 grid coordinate of the event), their money is halved.
5. If an individual encounters a good event, their intelligence serves as a probability value. The higher the intelligence, the more likely the individual is to seize the opportunity. If successful, their money doubles.

## Other Considerations:
1. Regarding the normalization of intelligence within the range of 0 to 1: Due to the infinite nature of the x-axis in the normal distribution, it's not straightforward to restrict the range to [0, 1]. However, according to the 68-95-99.7 rule, values beyond 3 standard deviations are extremely rare. Thus, for safety, we retain values within 5 standard deviations from the mean and adjust values beyond or below this range to the mean plus/minus 5 standard deviations. This approximation yields a distribution that closely resembles [0, 1] for a normal distribution.


# Experimental Results

## Intelligence Distribution

![image](https://github.com/lontzumon/TALENTorLUCKY/assets/100392818/50e7e5ff-a840-4756-bfe0-ab474439904c)
Figure 1: Distribution of intelligence among individuals, highlighting the highest/lowest intelligence.

## Wealthiest Individuals vs. Poorest Individuals

![image](https://github.com/lontzumon/TALENTorLUCKY/assets/100392818/d53630d7-65d6-4b44-b9f9-96f8501388ba)
Figure 2: Information about the wealthiest individuals: money, intelligence, number of events encountered.

![image](https://github.com/lontzumon/TALENTorLUCKY/assets/100392818/92006f9c-e039-45bc-90c7-8403640d6b45)
Figure 3: Number of events encountered by the wealthiest individuals each year.

![image](https://github.com/lontzumon/TALENTorLUCKY/assets/100392818/1ce176d9-20b2-403c-8755-e7427f078ffe)
Figure 4: Wealth changes of the wealthiest individuals over time.

![image](https://github.com/lontzumon/TALENTorLUCKY/assets/100392818/caa27cef-c3fe-40f4-826e-b3179f0a7dec)
Figure 5: Information about the poorest individuals: money, intelligence, number of events encountered.

![image](https://github.com/lontzumon/TALENTorLUCKY/assets/100392818/5e30f1b9-c596-4965-b9ec-2cc54ed820ef)
Figure 6: Number of events encountered by the poorest individuals each year.

![image](https://github.com/lontzumon/TALENTorLUCKY/assets/100392818/bfcc3fc1-2ce4-4615-aa93-fd7b8f61eb7c)
Figure 7: Wealth changes of the poorest individuals over time.

## Highest Intelligence Individuals vs. Lowest Intelligence Individuals

![image](https://github.com/lontzumon/TALENTorLUCKY/assets/100392818/92c19f01-7135-4053-ab5a-e3a0f5840d61)
Figure 8: Number of events encountered by the most intelligent individuals each year.

![image](https://github.com/lontzumon/TALENTorLUCKY/assets/100392818/58757bf8-4d86-4210-9295-e380fb3dcd09)
Figure 9: Wealth changes of the most intelligent individuals over time.

## Wealth and Population Changes after 40 Years

![image](https://github.com/lontzumon/TALENTorLUCKY/assets/100392818/160f8fc5-6574-44d1-b4e5-c083cf491595)
Figure 10: Changes in wealth after 40 years.

![image](https://github.com/lontzumon/TALENTorLUCKY/assets/100392818/7eed4b8b-1b4b-4c61-aa6c-a0925be6574e)
Figure 11: Distribution of wealth after 40 years, comparing the top 20% wealthiest individuals with the bottom 80%.
