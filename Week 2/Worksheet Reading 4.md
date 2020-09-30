# Paper reading worksheet #4: Apps

## Questions

### What is the **main research question/goal**? _(there may be more than one, but usually there is an overarching research question/goal.)_

- They are the first to conduct a study to understand the test automation culture in Android and Microsoft app development community.
- They analyze the extent to which Android apps are adequately tested by checking the presence of test cases and calculating coverage.
- They survey many Android and Microsoft app developers and collect their responses to understand testing tools used by them and challenges faced by these developers in testing their applications.

Research Questions:
- RQ1: Are Android applications well tested?
- RQ2: Do Android developers use automated testing tools to test their applications? What are the tools commonly used by Android developers and the challenges faced by them while testing their applications?
- RQ3: Do Microsoft developers use automated testing tools to test their applications? What are the tools commonly used by Microsoft developers and the challenges faced by them while testing their applications?

### Why is this paper **important**?

Despite the growing interest in the software testing and reliability research community to build tools that can automate and improve testing of mobile apps, there has been no study that investigates how developers test these applications in practice. This study is needed to understand the “pain points” that these developers face which can be used to motivate future research that addresses concerns that matters to mobile app developers.

### What is the **methodology** used to answer the research question(s) or reach the goal?

The study is divided into two parts:
- In the first one, they analyzed over 600 open-source Android apps to examine the current state of testing in the Android development community.
- In the second part, they replicated the above survey study with app developers from Microsoft. They improved their survey based on the responses of the first study and ask Microsoft developers about the type of testing they do, tools they use and the challenges they face during testing.

### What **data** does the paper use?

Part 1:
The dataset includes small apps to large and popular apps such as K- 9 Mail, FrostWire - Downloader/Player, OsmAnd Maps & Navigation and OI File Manager, which have more than 1,000,000 installs.

Part 2:
They surveyed over 600 developers and received 127 responses.

### If there is a **statistical model**, what is the product, behavior, or process being modeled? What are the key characteristics of the model?

- Test Cases: They counted the number of apps with and without test cases.
- Lines of Code (LOC): They counted the lines of code for all the apps in their dataset.
- Number of Developers: They wanted to analyse the number of developers involved in the development of an app. They used the information from git logs and collect unique e-mail addresses to count the number of developers.

### What are the **limitations** of using this methodology on the results?

- It is unclear if their findings would generalize to all Android applications. Their respondents might not be representative of the entire population of app developers and thus their results might not generalize to all app developers.
- They might miss some test files or mistakenly consider a file to be a test file when it is not.
- Furthermore, they manually analyse 89 apps which contain test files and calculate the coverage of test cases contained in these files. Out of the 89 apps, many failed to compile mainly due to missing dependencies

### What is **the answer** to the research question? _(in case of a goal: What is the contribution of the paper towards that goal?)_

- Only around 14% of the apps contain test cases and only around 9% of the apps that have executable test cases have coverage above 40%.
- Android app developers prefer using standard framework such as JUnit, but they also use Android specific testing tools such as Monkeyrunner, Robotium and Robolectric. However, many Android developers prefer to test their applications manually without the help of any testing framework or tools. Most Windows app developers make use of Visual Studio, Coded UI, Selenium, and Microsoft Test Manager to test their apps.
- Android and Windows app developers face numerous challenges in testing their apps and in using automated testing tools. These challenges include time constraints, compatibility issues, lack of exposure, cumbersome tools, emphasis on development, lack of organization support, unclear benefits, poor documentation, lack of experience, and steep learning curve.

### What did you **not understand** of this paper?
