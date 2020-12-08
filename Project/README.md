# Data Science in for Software Engineering

## Data Fitting
The data was gathered [here](https://bugzilla.mozilla.org/query.cgi?format=advanced) with the following settings:

![Settings](Docs/Images/Settings.JPG)

All the eight categories of severities were set here:

![Severities](Docs/Images/Severity.JPG)

There are eight Types of severites:

1. blocker
2. critical
3. major
4. normal
5. minor
6. trivial
7. enhancement
8. N/A

The following columns were chosen:

![Selected Columns](Docs/Images/Selected_Columns.JPG)

The amount of data items per type was according to the following table:

| Type | Training | Testing | Found Bugs Total |
| --- | --- | --- | --- |
| blocker | 2000 | 200 | 6442 |
| critical | 2000 | 200 | 10000 |
| major | 2000 | 200 | 10000 |
| normal | 2000 | 200 | 10000 |
| minor | 2000 | 200 | 10000 |
| trivial | 2000 | 200 | 6730 |
| enhancement | 40 | 5 | 45 |
| N/A | 1000 | 200 | 1509 |
| Total | 13045 | 1406 | 54726 |

The data was prepared as follows:
- Deleting of rows where the data was saved in more than one block (not suitable for input) and replacing them with further lines which were compliant.
- Quotation marks were deleted
- Bug Ids were deleted (because they are useless)

## Lists 

| Name | Purpose |
| --- | --- |
| training_list.csv | List with data for the training phase of the ML Algorithm |
| testing_list.csv | List with data for the testing phase of the ML Algorithm |
| bug_list.csv | List with data for the first test |