# CricStats

## Initial Observations
- We need to use a lot more than just balls faced and total score to predict a batsman's runs, otherwise the prediction will just reflect the proportion of the innings played scaled by the runs. So I'm currently using innings runs, batting position, the team runs when batsman came in, and the overs when the batsman came in to predict their scores.
- Currently the difference between the predicted runs and the true runs is used to *rank* innings by how good they are

- Interesting, using a neural net for regression, the best and the worst innings by differences in predicted score and true score occured in the same partnership ([IPL Match 598027](https://www.espncricinfo.com/series/indian-premier-league-2013-586733/royal-challengers-bangalore-vs-pune-warriors-31st-match-598027/full-scorecard)). This kind of shows the limitations of these method since TM Dilshan's innings was a good innings given the context.