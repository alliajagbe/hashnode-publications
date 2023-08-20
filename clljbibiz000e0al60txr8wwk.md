---
title: "From Chaos to Clarity: Ensuring Quality in Data Collection"
seoTitle: "Ethical Data Collection: Navigating Responsibility"
seoDescription: "Explore the intricacies of ethical data collection, from strategies to biases. Learn how responsible practices shape insights in the digital landscape."
datePublished: Sun Aug 20 2023 10:41:02 GMT+0000 (Coordinated Universal Time)
cuid: clljbibiz000e0al60txr8wwk
slug: from-chaos-to-clarity-ensuring-quality-in-data-collection
cover: https://cdn.hashnode.com/res/hashnode/image/stock/unsplash/xuTJZ7uD7PI/upload/6a992e1e71a4a03feae36cb6aed8a4e2.jpeg
tags: data, data-science, data-analysis, data-analytics, data-analytics-course

---

In our world today, data collection is at the beating heart of innovation. Every click, app download, purchase, and website interaction among many others contributes to a diverse set of insights that inform the way we navigate our world. In this article, I will discuss data collection, from the technical intricacies to the ethical considerations that guide us as humans. Specifically, I will shed light on how data is collected, discuss some key terminologies, types of data bias, data types, data collection considerations, identifying good data sources and ethics relating to data collection. My knowledge of this topic is informed mainly by the [Google Data Analytics Course](https://www.coursera.org/google-certificates/data-analytics-certificate?).

---

# Data Collection

As a data enthusiast, gaining a comprehensive grasp of the data collection process is paramount. In the realm of reality, datasets aren't always conveniently available for download from platforms like Kaggle or other public data repositories. This paves the way for data collection strategies.

| Data Collection Strategies | Use Case(s) | Example(s) |
| --- | --- | --- |
| Interviews | Gathering in-depth qualitative insights directly from people. They are mostly used in exploring personal experiences, opinions and emotions. They also help in uncovering detailed information such as in-depth customer feedback and expert opinions. | Given an instance where you are researching the challenges faced by remote workers, you might want to conduct some interviews to understand varieties of personal experiences when it comes to working remotely. |
| Observations | Systematically watching and recording behaviours, actions, and events in their natural settings without your intervention. | Studying customers' behaviours in a supermarket. Noting how they navigate the space, which aisles they visit, how much time they spend in each section, and how they interact with products. |
| Forms & Questionnaires | Collecting structured data from a large number of participants. | You just launched a new product and you want to know how well your product is thriving in the market via user feedback. To do this, you distribute an online questionnaire with questions about how well the users are using the product and their willingness to recommend it to their friends via social media and email campaigns. |
| Surveys | Collating quantitative and qualitative data by administering a set of questions to a group of respondents. They are usually employed in social research, customer satisfaction analysis, and opinion polling. | You need to understand people's opinions on climate change. Hence, you design a survey with questions regarding the public's awareness of climate issues, and their willingness to adopt sustainable practices. |
| Cookies | Collecting data on user interactions and other information that relay the usage of the platform (websites/mobile apps). | Imagine running an e-commerce website, you could use cookies to understand and track user behaviour. You can leverage the cookie data to gain insights relating to the products users view, add to their carts and eventually purchase. |

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Each data collection strategy has its own strength and weakness, making them optimal for different scenarios. The choice of strategy usually depends on the task at hand, available resources and the nature of the data needed. In some instances, it is possible to use a combination of different strategies to gain a more comprehensive view of the subject/topic of study.</div>
</div>

---

# Some Terminologies

### Types of Data

<table><tbody><tr><td colspan="1" rowspan="1"><p>Discrete Data</p></td><td colspan="1" rowspan="1"><p>Data that is counted and has a limited number of values. e.g. 45</p></td></tr><tr><td colspan="1" rowspan="1"><p>Continuous Data</p></td><td colspan="1" rowspan="1"><p>Data that is measured and can have an infinite number of values. e.g. 13.57922344</p></td></tr><tr><td colspan="1" rowspan="1"><p>Nominal Data</p></td><td colspan="1" rowspan="1"><p>Qualitative data categorized without a set order e.g. names of people, and animals.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Ordinal Data</p></td><td colspan="1" rowspan="1"><p>Qualitative data categorized in a set order. e.g. classes and ranks.</p></td></tr></tbody></table>

### Sampling & Bias

<table><tbody><tr><td colspan="1" rowspan="1"><p>Population</p></td><td colspan="1" rowspan="1"><p>All possible data values in a dataset.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Sample</p></td><td colspan="1" rowspan="1"><p>A subset of a population that is representative of the population.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Bias</p></td><td colspan="1" rowspan="1"><p>A preference in favour or against something, causing unfairness.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Sampling Bias</p></td><td colspan="1" rowspan="1"><p>This occurs when some entity has a greater likelihood of getting selected into the sample, relative to other entities within the population.</p></td></tr></tbody></table>

### Data Types & Formats

<table><tbody><tr><td colspan="1" rowspan="1"><p>Structured Data</p></td><td colspan="1" rowspan="1"><p>Data organized in rows and columns. e.g. csv and tsv files.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Unstructured Data</p></td><td colspan="1" rowspan="1"><p>Data not organized in a certain format. e.g. audio and video files.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Metadata</p></td><td colspan="1" rowspan="1"><p>Data about data; usually included for easy interpretation.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Wide Data</p></td><td colspan="1" rowspan="1"><p>Data in which every data subject has a single row with multiple columns to hold the values of various attributes of the subject.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Long Data</p></td><td colspan="1" rowspan="1"><p>Data in which each row is a one-time point per subject, so each subject will have data in multiple rows. This could be thought of as the "transpose" of wide data.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Data Elements</p></td><td colspan="1" rowspan="1"><p>Pieces of information within a dataset such as names, numbers etc.</p></td></tr></tbody></table>

### Data Management

<table><tbody><tr><td colspan="1" rowspan="1"><p>First-party Data</p></td><td colspan="1" rowspan="1"><p>Data collected using own resources.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Second-party Data</p></td><td colspan="1" rowspan="1"><p>Data collected from an audience and sold to another.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Third-party Data</p></td><td colspan="1" rowspan="1"><p>Data collected from outside sources who did not collect it directly.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Internal Data</p></td><td colspan="1" rowspan="1"><p>Data within a company's systems.</p></td></tr><tr><td colspan="1" rowspan="1"><p>External Data</p></td><td colspan="1" rowspan="1"><p>Data outside a company's systems.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Data Governance</p></td><td colspan="1" rowspan="1"><p>Formal management of a company's data assets.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Data Interoperability</p></td><td colspan="1" rowspan="1"><p>Ability of data systems to connect and share data.</p></td></tr></tbody></table>

### Data Quality & Validation

<table><tbody><tr><td colspan="1" rowspan="1"><p>Range</p></td><td colspan="1" rowspan="1"><p>Collection of cells within a spreadsheet.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Cross-field Validation</p></td><td colspan="1" rowspan="1"><p>Ensuring conditions for multiple fields are met.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Data Constraints</p></td><td colspan="1" rowspan="1"><p>Criteria set for determining data cleanliness and validity.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Incomplete Data</p></td><td colspan="1" rowspan="1"><p>Data missing important fields.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Inconsistent Data</p></td><td colspan="1" rowspan="1"><p>Data with non-uniform data format.</p></td></tr><tr><td colspan="1" rowspan="1"><p>Incorrect Data</p></td><td colspan="1" rowspan="1"><p>Complete but inaccurate data.</p></td></tr></tbody></table>

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">These lists are definitely not exhaustive but they provide an intuitive understanding of how key terms that are data-related are used in the data collection process.</div>
</div>

---

# Understanding Biases in Data Collection

In the world we live in today where vast amounts of data are being collected every unit of time, lies a critical factor that can shape outcomes in ways often unnoticed - bias. Much like a subtle current beneath the surface, bias can quietly influence how data is collected, interpreted, and harnessed. Whether through the lens of human observation or the algorithms of machines, bias can propagate its way right from the data collection down to the point where critical decisions have to be made. Hence, understanding bias and effectively tackling it are the compasses guiding us toward accurate, ethical, and well-informed conclusions.

| Data Biases | Explanation | Example | Potential Fix |
| --- | --- | --- | --- |
| Observer/Experimenter/Research Bias | The tendency for different people to observe things differently. It occurs when people unconsciously allow their beliefs/expectations to influence their observations and consequently, their interpretation of data. | A clinical researcher expecting a drug trial to come out positive might unintentionally notice only positive effects and not necessarily the potential side effects. | Double-blind studies where both the observers and the participants are unaware of certain information that could reinforce pre-existing beliefs or expectations. |
| Confirmation Bias | The tendency to search for or interpret information in a way that confirms pre-existing beliefs, leading to a neglect of opposing data points. | A political researcher seeking only evidence that reinstates their beliefs and disregards those that present counterarguments. | Cross-validation tests/techniques to ensure that findings hold true when tested against opposing data points. |
| Interpretation Bias | The tendency to always interpret ambiguous situations in a positive or negative way. | A school teacher believing a student is uninterested in his subject might interpret the student's neutral facial expressions as signs of disengagement in class activities. | Standardized criteria for interpreting data, focusing on objectivity. Diversified checks to collectively analyze data and arrive at a more balanced interpretation. |
| Sampling Bias | This happens when the sample being collected for a study is not representative of the larger population, leading to inaccurate generalizations. | Conducting a survey about challenges mothers face exclusively among those who are married. | Random sampling to ensure that all segments of the population are equally represented and all participants have the same probability of getting selected. If certain groups are underrepresented, employ stratified or oversampling techniques to address the class imbalances. |

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Recognizing and actively addressing bias is a continuous process that promotes ethical research practices and ensures the trustworthiness of data-driven conclusions.</div>
</div>

---

# Data Collection Considerations

### How the Data will be Collected

Deciding on the methodology and techniques for data collection is instrumental to any data-based project. Choose between methods like surveys, interviews, observations, or digital tracking based on the nature of the project. Succinctly vet the pros and cons of each strategy and opt for the one that best suits your objectives and target audience.

### Choosing the Data Sources

Determine whether you will be using first, second, or third-party data. Thoroughly assess your sources to ensure they align with your research goals and provide trustworthy information. For public data, websites like [data.gov](http://www.data.gov) are a rich source. To identify a good source, you can ask yourself these questions:

1. How reliable is this source?
    
2. Is this source original?
    
3. Is this data source comprehensive?
    
4. How current is the data from this source?
    
5. Is this data cited?
    

### Deciding which Data to Use

Prioritize data that directly align with your research goals. Including extraneous or irrelevant data might cloud your analysis. Ensure you are clear on your research objectives to make informed decisions about the data to include.

### How Much Data to Collect

Collecting too little data might lead to unreliable conclusions. At the same time, collecting too much can be overwhelming and time-consuming. Determine the optimal sample size or dataset volume based on statistical considerations. Your choice of confidence level and margin of error can help you decide the right sample size to get statistically significant results. You can use this simple [sample size calculator](https://docs.google.com/spreadsheets/d/1s19JyNYRCWI5bdpmcybKsuFkXlqUoMJnxm8kGU0APtc/edit?usp=sharing).

### Selecting the Right Data Type

Choose between qualitative, quantitative, structured, unstructured, or different data type combinations based on the project. Depending on the type of data selected, the analysis techniques change to achieve a desirable outcome.

### Determining the Time Frame

Decide whether you need historical data, current information, or data collected over a specific time period for your analysis. This consideration ensures the temporal relevance of your analysis.

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Clearly define your research objectives to guide your data collection process, and develop a data collection plan that outlines the methodology, sources, and timeline. Be transparent about your data collection procedures to enhance the credibility of your findings.</div>
</div>

---

# Pointers on Data Ethics

During data collection, a key aspect to always check for is **Ethics**. Ethics provide us with a set of moral principles that steer our actions and decision-making, ensuring that we operate with respect for individuals' rights. As regards **Data Ethics**, it is a vital branch that sets the stage for how data is collected, shared and utilized.

### Aspects of Data Ethics

* **Ownership**
    
    Individuals are the primary owners of the raw data they provide and they have control over how it is used, processed, and shared. Understanding this ensures that individuals retain agency over their personal information, preventing unauthorized exploitation.
    
* **Transaction Transparency**
    
    Data preprocessing activities and algorithms should be transparent and understandable to the individuals providing their data. This promotes trust and helps individuals make informed decisions about sharing their data, fostering a sense of accountability among data collectors.
    
* **Consent**
    
    Individuals reserve the right to know the details of how and why their data will be used before they agree to provide it. Consent ensures that data collection practices are conducted with informed consent from the providers of the data being used.
    
* **Currency**
    
    People should be made aware of any financial transactions resulting from the use of their personal data and the scale of these transactions. This prevents undisclosed profit-making at the expense of the individual's data.
    
* **Privacy**
    
    Preserving the privacy of a data subject's information and activities is paramount, safeguarding their identity and sensitive details. This helps maintain trust and prevent potential harm or misuse of their data.
    
* **Openness**
    
    Data should be made accessible, shareable, and usable with minimal restrictions, encouraging collaboration and innovation.
    

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Ensuring that data ethics are upheld at all stages of data collection, analysis and usage, not only upholds the rights of individuals but also contributes to the creation of a more ethical and equitable digital landscape. Incorporating these aspects of ethics into data practices demonstrates a commitment to ethical conduct and the promotion of data-driven insights that benefit society as a whole.</div>
</div>

---

# Final Note

Data Collection remains salient in the world we live in today, especially with lots of information being generated every second. Employing the right collection strategy, addressing biases and ensuring no violation of data ethics, remain paramount than ever before.

To read more from my notes on data collection, analysis, and visualization, you can check out this [link](https://github.com/alliajagbe/data-analytics/tree/master/notes).

Thanks for reading!