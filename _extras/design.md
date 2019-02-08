---
layout: page
title: "Lesson Design"
permalink: /design/
---
## Assumptions

* Audience
  * Librarians and library staff
  * Who interact with patron data and have a need to protect patron privacy
  * But need help:
    * Locating and identifying data that needs protecting
    * Taking the steps needed to effectively protect the data
* Constraints
  * One half-day
  * Learners use native installs on their own machines
    * May use VMs or cloud resources if available
    * But must keep native local install as an option
  * No explicit dependence on other Carpentry modules
    * In particular, does not require knowledge of shell or version control
    * However, previous exposure to programming in python would be helpful
    * This lesson is not intended as a comprehensive introduction to programming in python
  * Use the Jupyter Notebook
    * Experienced python programmers could run the examples as stand-alone scripts
    * Less experienced learners encouraged to use the notebook
* Data
  * Sample data provided for the various examples

## Learning objectives

* Find Personally Identifiable Information (PII) in the provided sample data
* De-identify, anonymize, and aggregate data to construct useful datasets that protect patrons' privacy
* Check the resulting datasets to evaluate the risk of re-identification
* Use python libraries to help do this work efficiently

## Lesson plan

### Summative Assessment
* Use the provided PII-containing datasets to construct a new aggregate dataset
* Include useful characteristics from the PII, de-identified & anonymized, as appropriate
* Evaluate the new dataset's risk of re-identification

### [Getting Started]({{page.root}}/01-introduction/) (2:00)
* Teaching: 15 min (because setup issues)
  * How to use the stickies
  * Launch the Jupyter Notebook, create new notebooks, and exit the Notebook.
  * Create Markdown cells in a notebook.
  * Create and run Python cells in a notebook.
* Challenges: 0 min (accounted for in teaching time - no separate exercise)
  * Creating lists in Markdown
  * What is displayed when several expressions are put in a single cell?
  * Change an existing cell from code to Markdown

### [Importing Data with the Pandas Library]({{page.root}}/02-importing_data/) (2:15)
* Teaching: 15 min
  * Explain what software libraries are and why programmers create and use them
  * Import the pandas library
  * Use the help function to see the built-in documentation
  * Use pandas to load a simple CSV data set
  * Get some basic information about a pandas DataFrame
* Challenges: 15 min
  * If `help(pd)` produces an error, what have you forgotten to do?
  * Read the circulation data and display its summary statistics
  * What do `.head` and `.tail` do?
  * What string(s) should you pass to `read_csv` to read files from other directories?
  * How can you *write* CSV data?

### [Working with Data as DataFrames]({{page.root}}/03-working_with_data/) (2:45)
* Teaching: 15 min
  * Select individual values from a pandas dataframe.
  * Select entire rows or entire columns from a dataframe.
  * Select a subset of both rows and columns from a dataframe in a single operation.
  * Select a subset of a dataframe by a single Boolean criterion.
  * Merge values from two sources into a single dataframe
* Challenges: 15 min
  * Read the patron data and select school, department and major into a new dataframe
  * Read the circulation data and select call numbers from checkouts into a new dataframe
  * Join the two dataframes into a single dataframe
  * Determine the size of the smallest group in your population
  * Is this a problem? Why or why not? What might be done, if it is?

### Break: 15 min (3:15) FIXME: link

### [PII and Other Risky Data]({{ page.root }}{% link _episodes/04-pii.md %}) (3:30)
* Teaching: 10 min
  * Define PII (Personally Identifiable Information)
  * Give examples of PII that might be found in library data
  * Point out other kinds of data that might warrant caution
  * Observe that data becomes more problematic when it can be matched with other data, such as from other sources (https://iapp.org/media/pdf/knowledge_center/PII_Risk_Level_Matrix.pdf)
  * Offer some strategies that might limit these risks, while still providing valuable insights
* Challenges: 10 min
  * Re-read the patron and circulation data, selecting all fields
  * If you receive error [FIXME], what might be the cause & solution?
  * Identify the PII within the data
  * Identify other data that might be problematic
  * What combinations of data present a greater risk to patron privacy?
  * What data from other sources could be matched with this data to present a greater risk to patron privacy?
  * List some strategies to limit the risks within this data

### [Parsing Data with Functions]({{page.root}}/05-functions/) (3:50)
* Teaching: 10 min
  * Explain and identify the difference between function definition and function call
  * Write a function to parse a call number manually
  * Write a function to parse a call number with PyCallNumber
  * Demonstrate how to apply this function to the rows in a dataframe
* Challenges: 10 min
  * Write a function to sort the checkouts into subject and subsection, excluding book number
  * If you receive error [FIXME], what might be the cause & solution?
  * Apply your function to the circulation data and save the result into a new dataframe
  * Save the result as checkouts_by_subject.csv

### [De-identification & Anonymization]({{page.root}}/06-deidentification/) (4:10)
* Teaching: 10 min
  * Distinguish between de-identification & anonymization
  * Point out that there is a spectrum of identifiable data and therefore a spectrum of techniques to protect it
    * https://fpf.org/wp-content/uploads/2017/06/FPF_Visual-Guide-to-Practical-Data-DeID.pdf
* Challenges: 10 min
  * Use a combination of filters and functions to de-identify data within the patron and circulation datasets
  * Save this de-identified data into a new dataset
  * Save the result as deidentified_circ_data.csv

### [Aggregation & Re-identification]({{page.root}}/07-aggregation/) (4:30)
* Teaching: 10 min
  * Observe that the purpose behind analyzing library data is not to learn about individual patrons, but to learn about our patrons as a population
  * Demonstrate how we can use pandas to summarize and aggregate the data we have about our patrons and their use of library resources
  * Emphasize the privacy benefits of saving these conclusions, rather than the raw data used for such analysis
  * Point out that such efforts do not provide adequate protection for outliers in the population
  * Note that with enough matching data from other sources, inadequately protected data can be re-identified to reveal information about individuals within the population
* Challenges: 10 min
  * Use the datasets we have been working with so far
  * Roll up data about individuals into aggregate data about the population
  * Save the result as a new dataframe, then into circ_report.csv
  * Evaluate the new dataset's risk of re-identification by looking at the size of the smallest sub-populations described
  * Consider what more might be done to protect these patrons. At what point might we determine that our analyzed data is still too risky? What would we do then?

### Wrap-Up (4:50) FIXME: link
* Teaching: 10 min
  * Share resources for further learning
  * Solicit feedback through one-up / one-down

### Finish (5:00)
