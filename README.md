# Star Wars Movie Ranking Analysis
## A survey containing over 1000 responses is used to determine which movie in the Star Wars series is considered the best among fans and nonfans. This project is from [DataQuest](https://github.com/dataquestio) coursework including guided steps and a solution notebook to assist in completion of the analysis.

# Question

Which movie out of the Star Wars series is considered the best of the six among self-proclaimed fans and nonfans respectively, and does viewcount play a role in their decision?

# Methods

## Data Cleaning

The dataset contains some difficult information to work with including typos, NaN values, and yes/no columns rather than boolean values, so the first step is to clean up some of the data we plan to utilize.

A simple str.replace method sufficed to remove the unwanted typo characters and replace them with correct information among the six Star Wars film names that will be used for analysis.

To convert yes/no columns into boolean values, a dictionary was created with "Yes" and "No" as keys and "True" and "False" as elements. This dictionary was mapped to columns in the dataset as a means to find and replace as needed.

An additional dictionary was created and mapped as a similar tool for survey respondent who wrote down the name of the movie if they saw it instead of yes/no or a boolean value.

Columns were renamed for the sake of clarity to properly reflect the number of the movie in the Star Wars series.

Finally, NaN values were omitted from analysis and columns with ranking numbers were converted to float data types.

## Comparing Average Movie Rankings and Familiarity

A [bar chart](https://github.com/quinnrad/Star-Wars-Movie-Ranking-Analysis/blob/main/star%20wars%20movie%20rankings.pdf) was produced using the mean values of each respondent's movie rankings. With 1 being the most favorable movie and 6 being the least favorable movie in the series, we can see that the fifth movie had the best average rating among all of the movies.

To take it a step further, the sum of respondents who had seen each movie was displayed in a [bar chart](https://github.com/quinnrad/Star-Wars-Movie-Ranking-Analysis/blob/main/star%20wars%20movies%20seen.pdf), showing us that the fifth movie is not only the favorite but also the most well known among respondents.

## Separating Fans and Nonfans

The dataframe was split into two based on each response to a particular question: "Do you consider yourself to be a fan of the Star Wars film franchise?"

This allowed for the comparison of self-proclaimed fans and nonfans to determine if a difference exists between their movie rankings and familiarity.

Despite separating the dataframe into two sets based on fan category, both sets of respondents ranked the fifth movie as the best and the third movie as the worst, albeit the nonfan movie rankings are much closer to one another than the fan rankings.

Now the fun part, we get to weed out the biased respondents based on which movies of the six they have or have not seen at least once.

Almost all of the fan respondents (552) had seen every movie. The third movie had the lowest views at around 450.

As for the [nonfans chart](https://github.com/quinnrad/Star-Wars-Movie-Ranking-Analysis/blob/main/star%20wars%20nonfan%20movies%20seen.pdf), the fifth movie had the most views at 230 out of 284 nonfan respondents. Other movies were not quite so well-known with the third movie at the lowest value of 100 nonfans who had seen it.

# Final Words

As a whole, it was unanimous among fans and nonfans alike that the fifth movie is the best while the third movie is the worst. This trend only becomes stronger when leaning into self-proclaimed fan data which represented notably higher values in terms of respondents who had seen each movie at least once. I guess even nonfans can tell which movie is the best... Even if they haven't seen all of them!
