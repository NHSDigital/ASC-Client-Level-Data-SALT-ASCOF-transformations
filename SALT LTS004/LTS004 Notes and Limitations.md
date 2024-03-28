
As with all measures, the process is reliant on LAs accurately capturing fields as per the relevant specification defined lists. Any fields that are invalid as per the CLD specification are removed from the analysis – source data will not be corrected and invalid field entries cannot be mapped to the specification.  All invalid field entries are flagged and captured in the Data Quality Reports received by LAs to highlight areas to be corrected in future submissions. 

Data quality issues have been identified in a handful of cases with conflicting accommodation status/employment status for seemingly duplicate records with same event start date. In these cases, any record where accommodation/employment status is known will be brought forward over a duplicate entry with an unknown status. If conflicting records are still present after these steps, any remaining duplicate events with conflicting accommodation/employment status will be recorded as having an Unknown status in the final table

Table is for 18-64 year olds only. Some clients have an unknown age and are therefore not considered for inclusion in the code process. 

Age in the SQL code is a proxy derived from the Birth Month and Birth Year fields, as these were the fields available to NHS England in the CLD Database. Accurate age fields can replace these if user has access to these fields

‘Latest Submission’ procedure at the beginning of the code takes the last submission (date and time) for each Local Authority within the relevant period of interest. This is used on the understanding that the last data submitted by each Local Authority in each quarterly window is the latest, complete picture to date. If a Local Authority submits a partial return or a top-up of a specific cohort as their last submission before the submission deadline, this will cause under-counting and inaccurate reporting for the LA in question. 

NHS Number is used as a unique identifier for each Client wherever possible. Where NHS number is not populated the Local Authority unique ID is used instead, if this can be done without compromising accuracy. In instances where no ID can be attributed to an event row without introducing the risk of either double-counting or incorrect allocation of identifiers to individuals, these event rows will be removed from the headcount (see Glossary of key concepts for further information). 

Any Reference Data tables needed for the process are built as temporary tables in the script. These can alternatively be built as permanent tables if the environment the code is being run in allows. These Reference tables should periodically be checked against the Client Level Data Specification to ensure the Defined Lists haven’t changed and labels are still up-to-date

Code is written as at Q3 for 2023/24, the latest submission as per time of creation. Date filters can be amended as needed

