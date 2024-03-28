LTS003 SQL script only produces high-level total numbers of Carers, by Support Provided, as per the SALT Table 1a. Further development would be needed to produce these figures at a further level of granularity.

As with all measures, the process is reliant on LAs accurately capturing fields as per the relevant specification defined lists. Any fields that are invalid as per the CLD specification are removed from the analysis – source data will not be corrected and invalid field entries cannot be mapped to the specification.  All invalid field entries are flagged and captured in the Data Quality Reports received by LAs to highlight areas to be corrected in future submissions. 

As delivery mechanism is not mandatory, some delivery mechanisms previously captured in SALT (e.g. CASSR commissioned support, CASSR managed personal budget) may not aways be populated in CLD. As such, full completeness across columns previously in LTS003 may not be possible. 

Age in the SQL code is a proxy derived from the Birth Month and Birth Year fields, as these were the fields available to NHS England in the CLD Database. Accurate age fields can replace these if user has access to these fields

‘Latest Submission’ procedure at the beginning of the code takes the last submission (date and time) for each Local Authority within the relevant period of interest. This is used on the understanding that the last data submitted by each Local Authority in each quarterly window is the latest, complete picture to date. If a Local Authority submits a partial return or a top-up of a specific cohort as their last submission before the submission deadline, this will cause under-counting and inaccurate reporting for the LA in question. 

NHS Number is used as a unique identifier for each Carer wherever possible. Where NHS number is not populated the Local Authority unique ID is used instead, if this can be done without compromising accuracy. In instances where no ID can be attributed to an event row without introducing the risk of either double-counting or incorrect allocation of identifiers to individuals, these event rows will be removed from the headcount (see Glossary of key concepts for further information). 

Code is written as at Q3 for 2023/24, the latest submission as per time of creation. Date filters can be amended as needed

Any Reference Data tables needed for the process are built as temporary tables in the script. These can alternatively be built as permanent tables if the environment the code is being run in allows. These Reference tables should periodically be checked against the Client Level Data Specification to ensure the Defined Lists haven’t changed and labels are still up-to-date.

Carers information is mapped into 'Support Provided' categories using a CASE statement (see SQL code annotation in the script for more info). Care should be taken to ensure any CLD Spec wording changes are incorporated into this syntax to ensure it continues to work as intended.

There are some instances where Event Outcome may be invalid or may not accurately reflect the outcome reached. This may lead to under-reporting of the ‘Information and Advice’ cohort and ‘No Direct Support Provided to Carer’ cohort 