# Statistical Hypothesis Testing

### Team Members
Sarah Smith, Catherine Wolk
***

- [Data](#Data)
- [EDA](#eda)
- [Hypotheses Testing](#model)
- [Results](#results)
- [Next Steps](#future) 


## Project Goals
The motivation is to investigate trends in Album ratings on [Pitchfork](https://pitchfork.com) with the following questions in mind:
1. Is there a difference between ratings depending on the month an album was released?
1. Is there a difference between ratings depending on the genre of an album?
1. Is there a difference in average rating between different writers?

## Data <a name="Data"></a>
We scraped album ratings from [Pitchfork](https://pitchfork.com) and ended up with a dataset of 6,943 with the following features:
- Album Name
- Artist
- Rating Score
- Release Date
- Reviewer
- Reviewer Position

## EDA <a name="eda"></a>

We started by looking at how the overall ratings are distributed:

![ratings distribution](https://github.com/ssmithie/flatiron_mod3_project/images/dist_ratings "ratings distribution")

We then visualised the box and whisker plots broken down by both genre and month:
![genre distribution](https://github.com/ssmithie/flatiron_mod3_project/images/dist_genre "genre distribution")

![month distribution](https://github.com/ssmithie/flatiron_mod3_project/images/dist_month "month distribution")


## Hypotheses Testing <a name='model'></a>

The three hypotheses we will test are:
1.  Ho: There is no significant difference in average rating between months

    Ha: There is a significant difference in average rating between months
    
1.  Ho: There is no significant difference in average rating between genres

    Ha: There is a significant difference in average rating between genres

1.  Ho: There is no significant difference in average rating between writers

    Ha: There is a significant difference in average rating between writers
    
***
### Method
We performed One Way ANOVA tests for each of our hypotheses.
For our tests we chose an alpha of 0.01 due to our large dataset size.

For the first question, is there a difference between the average overall rating by month released, we found the following:
From the one way ANOVA we had an F-value of 2.04 and a p-value of 0.02.
In this case we failed to reject the null hypothesis and determined that there is no statistical difference in rating over the months released.
We also ran a Tukey's HSD pairwise comparison that further confirmed our result.

For the second question, is there a difference between the average overall rating by genre, we found the following:
From the one way ANOVA we had an F-value of 24.4 and a very low p-value.
In this case we also checked for effect size, and found that with a significantly low value we must fail to reject the null.
When we checked the Tukey's HSD pairwise comparison we saw that while overall we must reject the null, there are some genres that might be statistically different from each other.

### Conclusions
- There is no statistical differnce between ratings between months
- Some genres have a small difference in average rating than others, but overall there is no significant difference.
- While there are minor differences, reviewers have the same statistical review average.
