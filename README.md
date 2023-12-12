# Influenza Season - Staffing

## Project Overview

- Motivation: The United States has an influenza season where more people than usual
suffer from the flu. Some people, particularly those in vulnerable populations, develop
serious complications and end up in the hospital. Hospitals and clinics need additional
staff to adequately treat these extra patients. The medical staffing agency provides this
temporary staff.
- Objective: Determine when to send staff, and how many, to each state.
- Scope: The agency covers all hospitals in each of the 50 states of the United States, and
the project will plan for the upcoming influenza season.

**Possible ML or predictive analytics ideas**:

1. **Classification**:  Create various buckets for level of staffing required— low, medium, high. Predict which class each State/Province/County will fall into at a specific time
2. **Regression**: Predict how many staff members are to be assigned to a State/Province/County at a specific time. 
3. **Clustering**: Create entirely new groups from dataset based on distribution of data. Examples could include unvaccinated and dead from influenza, vaccinated and dead from influenza, well-staffed but major fatalities…etc


## Data Overview

## 1. Population data by geography US Census data

### 1.1 Summary of the data
#### Data source:
- External data, owned by the US government - more specifically the US Census
Bureau, is therefore highly trustworthy
#### Data collection method:
- Administrative data, collected automatically
- time lag may exist due to differences in data transfer of local entities to the overall
data set
#### Data content:
- data contains the absolute population numbers per county of every state for each
year from 2009-2017, further differentiated into the total amount of men and women
and the absolute numbers of individuals per age group, starting from ti years, in ti-
year-steps, until 8ti years (over 8ti years is not further differentiated) – hence,
demographics of the counties focusing gender and age

### 1.2 Potential Limitations/Biases:
- Counties may differ in data collection and transformation methodology, or the quality
of both may differ across time due to technical evolution/ digitalization
- At some point, the data was probably manually entered (for example by an employee
at the resident registration office), but errors are rather unlikely because the data is
highly relevant
- Some counties/states may hold higher numbers of unregistered individuals, i.e. such
close to the border
- Bugs in office sobware may contribute to errors, but this is rather unlikely and should
be noticed

### 1.3 Data Relevance
The data contains information regarding population numbers, which is important to define
the staffing plan for each state following the objective. It also entails information on age
proportions for each state, which is important for to define the amount of vulnerable groups
and hence, for the hypotheses targeting age groups.
• County, State: highly relevant regarding the objective – where to send staff, staffing plan
considers each state
• Year: highly relevant because we want to conduct a historical analysis to define the future
trends in influenza seasons for planning purposes
• Total population: highly relevant as baseline number of population
• Male Total population & Female Total population: both not relevant as we do not plan
gender-specific analyses (may be useful if there are differences in vulnerability between
genders)
• Age groups from ti to 8ti and older in ti-steps: highly relevant for conducting analyses
regarding vulnerable groups as in my hypotheses 1,3,4 (see above)

## 2. Influenza Laboratory Tests and Patient Visits data sets
### 2.1 Summary of the data
#### Data source:
- External data, owned by the Center for Disease Control and Prevention, Influenza
Division
- Virologic surveillance provided by U.S. World Health Organization (WHO)
Collaborating Laboratories System and the National Respiratory and Enteric Virus
Surveillance System (NREVSS)
- Information on outpatient visits to health care providers for respiratory illness
referred to as influenza-like illness [ILI) is collected through the U.S. Outpatient
Influenza-like Illness Surveillance Network (ILINet)
- ILINet consists of outpatient healthcare providers in all ti0 states, Puerto Rico, the
District of Columbia, and the U.S. Virgin Islands.
- Survey data for monitoring flu season on a nationwide level, is highly important for
governmental decisions on health care, therefore highly trustworthy

#### Data collection method:
- Survey data
- Lab tests data provided by approximately 100 public health and approximately 300
clinical laboratories located throughout all ti0 states, Puerto Rico, Guam, and the
District of Columbia that participate in virologic surveillance for influenza through
either the U.S. WHO Collaborating Laboratories System or NREVSS
- Influenza visits provided by ILINet, consist of outpatient healthcare providers in all ti0
states, Puerto Rico, the District of Columbia, and the U.S. Virgin Islands.
- collected manually
- There is no time lag, as the data in the data sets is only reported until 201ti or 2019,
respectively. However, reporting period for each influenza season begins during
Morbidity and Mortality Weekly Report (MMWR) week 40 and ends week 39 of the
following year. MMWR weeks refer to the sequential numbering of weeks (Sunday
through Saturday) during a calendar year. This means that the exact start of the new
influenza surveillance season varies slightly from season to season. “Flu season” also
varies from season to season, is said to have started aber consecutive weeks of
elevated flu activity is registered in the various CDC influenza surveillance systems.
So, time variables are not exactly comparable across the years.

####  Data content:
- Influenza Visits tracks the percentage of visits for influenza-like illness reported by
3,500 outpatient healthcare providers
- It contains the number of visits, number of providers, and total patients seen by week
and state from late 2010 to early 2019
- Lab Tests counts the number of positive influenza laboratory tests by week and state
from late 2010 to early 201ti as reported by 100 public health providers and over 300
clinical laboratories located throughout the United States and its territories, also
separated for the influenza virus subtypes

### 2.4 Potential Limitations/Biases:
- Data was probably manually entered following the patient’s report – errors could
occur
- Data from surveys, patients report voluntarily: bias in who reports, maybe depended
on well-being considering that patients have to report its data by Tuesday abernoon
of the following week the positive influence test occurred – the ones more affected
may not report
- Differences in demographics of the region may contribute to likelihood of patients
reporting (i.e., social status, education level may influence willingness to participate
in scientific study) – bias in representation of states
- Bugs in sobware may contribute to errors, but this is rather unlikely and should be
noticed

### 2.5 Data Relevance
- The data contains information regarding patient visits to a medical provider for
influenza, and numbers of positive influenza laboratory tests by week and state
across the years which is important to define the staffing plan for each state following
the objective. The data sets are also important to test hypotheses 3,4 and 6 with
visits for influenza-like-illness and flu infection rates as target variables.
 
## 3.Children Flu Shots data set

### 3.1 Summary of the data
#### Data source:
- External data, owned by National Immunization Surveys (NIS), University of Chicago
runs the surveys on behalf of the Centers for Disease Control (CDC)
- Data from a random sampling of parents, demographics self-reported, might be
inaccurate if parents conceal information due to various reasons, for example
mistrust in data protection
- flu shot information is verified with health providers, can be considered accurate
- Data is collected by the University of Chicago, for CDC, data collection and ETL
therefore highly trustworthy
#### Data collection method:
- Survey data collected through telephone interviews with parents in all states and U.S.
territories
- Collected manually
- No time lag, but data only available for 2017
#### Data content:
- data contains flu shot data for children 19-23 months, 24-29 months, 30-35 months
- categorized by geographic state, contains various family demographics including
poverty level, race, and parent marital status

### 3.2 Potential Limitations/Biases:
- Data was probably manually entered following the patient’s report – errors could
occur
- Data from surveys, patients report voluntarily: bias in who is willing to report
- Parents that do not let children vaccinate may be underrepresented, might be less
willing to participate
- Differences in demographics of the region may contribute to the likelihood of patients
reporting (i.e., social status, education level may influence willingness to participate
in scientific study) – bias in representation of states
- Who is at home at what time and can answer the phone may also produce biases
(stay-at-home parent, or unemployed parents)

### 3.3 Data Relevance
- Data set only contains data only for 2017 and only for children up to 35 months. The
data set can help to answer hypotheses ti and 6 but is limited to the year 2017
regarding the number of vaccinated children as the independent variable. Not
particularly helpful in terms of the objective, hence, to define the staff plan –
vaccination information across a broader age range, more vulnerable groups, medical
staff, etc. would have been more helpful

