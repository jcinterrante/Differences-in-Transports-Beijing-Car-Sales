# Differences-in-Transports-Beijing-Car-Sales
Only individuals with Beijing license plates are allowed to drive within city limits. The intent of the policy is to limit traffic and pollution in Beijing. Since January 2011, the government has held lotteries to distribute these license plates. Therefore, those awarded the license plate comprise a random sample of applicants; and by extension, lottery winners are a random subset of car buyers.

Daljord et al. (2021) theorizes there is a black market for license plates. Since the license plates were valuable, lottery winners sometimes sell the license plates to wealthy people. This would result in a larger share of wealthy individuals obtaining license plates. Policymakers would like to know the scale of this black market, but have traditionally been unable to do so because the transactions are under the radar.

However, we know a likely outcome of this black market: if lower income people are selling their license plates to wealthier people, we would expect that more expensive cars will be sold than we would expect based on parallel trends in other cities.

That is precisely the analysis I carry out. I use the Diftrans package (https://github.com/omkarakatta/diftrans) to compare the distribution of car prices in Beijing to that in Tianjin, which did not have a lottery.

The transport estimator method compares two distributions and quantifies the difference between them. This difference is referred to as the "transport cost" -- as in the "cost" needed to "transport" the mass of one distribution to make its shape match with another. Diftrans attempts to find the minimal cost neeeded to transport the mass of one distribution such that it has the same shape as another distribution. It also corrects for trends over time, similar to a difference-in-differences estimator.

My analysis replicates a simplified version of Daljord et al.'s analysis and finds strong evidence that the theorized black market is real, and finds a lower bound for its size.
