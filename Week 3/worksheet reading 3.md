# Paper reading worksheet

## Questions

### What is the **main research question/goal**? _(there may be more than one, but usually there is an overarching research question/goal.)_

They wan to revisit the relationship between the code ownership and software quality.

### Why is this paper **important**?

They were able to show that code reviewing activity provides an important perspective that contributes to the code ownership concept. Future approximations of code ownership should take code reviewing activity into account in order to more accurately model the contributions that developers make to evolve modern software systems.

### What is the **methodology** used to answer the research question(s) or reach the goal?

In a first step, they linked code changes to reviews. Once this was done, they measured review coverage for each module (directory). Then they removed modules that do not have 100% review coverage from their datasets in order to control for the confounding effect that a lack review coverage may have.
In a second step, they computed code ownership heuristics. To estimate the code ownership of a developer for a module, they first identified code changes that the developer has authored using the owner field recorded in Gerrit. They then identified the code changes that the developer has reviewed using the
review comments that the developer posted. Next, they estimatee code ownership using the traditional, review-specific, and review-aware code ownership heuristics for every developer who was involved with the development of each module.
In a last step they calculated module metric:.
- For the product metrics, they measured the size of the source code in a module at the time of a release by aggregating the number of lines of code in each of its files.
- For the process metrics, they used churn and entropy to measure the change activity that occurred during the development cycle of a studied release.

### What **data** does the paper use?

They used the review datasets that are provided by Hamasaki et al., which describes patch information, reviewer scoring, the involved personnel, and review discussion. They used the code dataset for the Qt system provided by their prior work, which describes the recorded commits on the release branch of the Qt VCSs during the development and maintenance of each studied Qt release. They also expanded the code dataset for the OpenStack system using the same approach as their prior work. In order to produce the datasets that are necessary for their study, they linked the review and code datasets, and compute the code ownership heuristics.

### If there is a **statistical model**, what is the product, behavior, or process being modeled? What are the key characteristics of the model?

They analyzed descriptive statistics of the number of developers who contribute by authoring or reviewing code changes to modules. They used one-tailed Mann-Whitney U tests to detect whether there is a statistically significant difference among the defective and clean modules in terms of the proportion of developers in the different expertise categories

### What are the **limitations** of using this methodology on the results?

- They focused their study on two open source systems. Thus, their results may not generalize to all software systems.
- Their analysis is focused on the code review activity that is recorded in the code review tools of the studied systems. There are likely cases where developers perform code reviews through other communication media,

### What is **the answer** to the research question? _(in case of a goal: What is the contribution of the paper towards that goal?)_

Their results suggest that future approximations of code ownership should take code review activity into consideration in order to more accurately model the contributions that developers have made to evolve software systems and to identify defect-prone modules.

### What did you **not understand** of this paper?

Nothing, it was very understandable.

