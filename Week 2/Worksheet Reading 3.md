# Paper reading worksheet #3: Testing

## Questions

### What is the **main research question/goal**? _(there may be more than one, but usually there is an overarching research question/goal.)_

But the main goal of this paper is to "observe how CI happens in the wild on a large basis of influential OSS projects."

### Why is this paper **important**?

Developers need to know the state of the art of how CI is done in the OSS community. Especially maintainers of and newcomers to CI,
whether they join an established project or plan to introduce CI, will benefit from knowing what they can expect from it.

### What is the **methodology** used to answer the research question(s) or reach the goal?

- Find out which projects use TRAVIS CI (TravisPoker)
- Aggregate detailed information about a project’s TRAVIS CI build history (TravisHarvester)
- Build Linearization And GITHUB Synthesis. To assess the status of the project at the moment each build was triggered, they extracted information from two sources: the project’s GIT repository and its corresponding entry in the GHTORRENT database.
- The language-agnostic BUILDLOG ANALYZER reads-in a build log, splits it into the different build phases, and analyzes the build status and runtime of each phase
- For Java, they supported the three popular build tools MAVEN, GRADLE, and ANT
- They needed to make a connection between the builds performed on TRAVIS CI and the repository which contains the commits that triggered the build. We call this build linearization and commit mapping, as we need to interpret the builds on TRAVIS CI as a directed graph and establish a child-parent relationship based on the GIT commits that triggered their execution.


### What **data** does the paper use?

For the first research question they used the GHTORRENT database as a source of projects to examine and apply filtering to select the most appropriate ones. For the second and the third research question they filtered their recived the data set fropm TRAVIS CI and used just the Java and the Ruby projects because those two languages enjoy wide popularity among developers and have a strong testing tradition. After that they again filtered out the projects which did not use TRAVIS CI and kept only the ones which used it. Then they combined the both data sources in the newly implemented TRAVISTORRENT.

### If there is a **statistical model**, what is the product, behavior, or process being modeled? What are the key characteristics of the model?

They regarded results as significant at a 95% confidence interval (a = 0.05). For each test, they first performed a Shapiro-Wilk Normality test.

Since all the distributions significantly deviate from a normal distribution according to Shapiro-Wilk, they used non-parametric tests: for testing whether there is a significant statistical difference between two distributions, they use the non-parametric Wilcoxon Rank Sum test. 

Regarding effect sizes, they reported Vargha-Delaney’s Â12, a non-parametric effect size for ordinal values. The Â12 measure has an intuitive interpretation: its ratio denotes how likely distribution A outperforms B.

### What are the **limitations** of using this methodology on the results?

- They only considered Ruby and Java projects, so their findings only fit for those two programming languages.
- There are bigger projects that use their own CI, therefore those prejects could not be considered although they are usign CIs.

### What is **the answer** to the research question? _(in case of a goal: What is the contribution of the paper towards that goal?)_

Testing is configured as a crucial factor to the success of the build, but exceptions are made on an individual level. They found that testing on the CI is highly dependent on the language, and that a dynamically typed language like Ruby has up to ten times more tests and leads to a higher build breakage rate due to tests than a statically typed language like Java.

### What did you **not understand** of this paper?

Why did they exactly pick ruby projects? Python is also dynamically typed and it is used much more than Ruby ergo there would have been more data available to analyze...
