# Paper reading worksheet

## Questions

### What is the **main research question/goal**? _(there may be more than one, but usually there is an overarching research question/goal.)_

They want to study how developers perform with changing work patterns., i.e. how the coounication and committing behaviours of developpers change with significant work rate increase.

### Why is this paper **important**?

It is important to know how developers perform with increasing work-rate because the quality of a product can be directly afffected by bad work caused by stress. This is especially important for a boss or for customers when they fix the deadline of the product to be handed in.

### What is the **methodology** used to answer the research question(s) or reach the goal?

They surveyed a set of ative and productive developers on GitHub, then they analyzed the GitHub activity data with regression modeling to model changes in developers' work patterns in terms of technical and social work-rates.

### What **data** does the paper use?

For the survey:
A set of active and productive developers with a timespan of five years from the first commit to the last commit and with at least 500 commits in 10 disticnt, non-forked repositories, the commits were done between 2008 and 2018. 20000 of those developers were surveyed with a set of 45 questions to be answered. 456 responses werwe obtained.

For the online activity trace data:
A set of 3000 developers randomly picked from the set for the survey. They just removed users which indicated to be bots before picking randomly.

### If there is a **statistical model**, what is the product, behavior, or process being modeled? What are the key characteristics of the model?

They modeled how developers’ committing and commenting behaviors change as a function of social and technical work-rate increases using hierarchical regression analyses. The key characteristics are different activities done by the developers such as commits, the average number of projects worked on per active day, the diversity if focus switches among projects worked on within a week etc. 

### What are the **limitations** of using this methodology on the results?

They used sentiment analysis tools which were not trained by themselves, so the outcome may not be entirely representative. 

### What is **the answer** to the research question? _(in case of a goal: What is the contribution of the paper towards that goal?)_

- Their survey showed that work-related activities, and especially increase in work responsibilities, lead towork-related stress. Developers noted their various reactions to stress and their coping mechanisms.
- Companies may communicate differently, so the data my be less representative since there is missing a (maybe) huge part of it.
- They collected developers’ information and activity from GHTorrent, so our data is limited by how completely GHTorrent captures developer data.

### What did you **not understand** of this paper?

I did not exactly understand for what reasons they used the Benjamini and Hochberg method.

