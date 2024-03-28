As with all measures, the process is reliant on LAs accurately capturing fields as per the relevant specification defined lists. Any fields that are invalid as per the CLD specification are removed from the analysis – source data will not be corrected and invalid field entries cannot be mapped to the specification.  All invalid field entries are flagged and captured in the Data Quality Reports received by LAs to highlight areas to be corrected in future submissions. 

Interrupted services may be recorded differently across the country so whilst the methodology tries to mitigate for this by considering continuous activity, not just services with a start date over 12 months ago, some cases may not be captured. 

Because the collection was not mandatory before 1st April 2023, this measure will use events beginning on or before 1st April 2023 (rather than 31st March 2023) as a proxy for any services/continual long term activity open for 12 months or more.

There are instances arising in CLD where Clients have conflicting PSR entries for otherwise identical records. In these cases, any record where PSR is known will be brought forward over a duplicate entry with an Unknown PSR. If conflicting records are still present after this step, the latest submitted row will be brought forward. After this process any remaining duplicate events with conflicting PSRs will be recorded as Unknown PSR in the final table. 

As delivery mechanism is not mandatory, some delivery mechanisms previously captured in SALT (e.g. CASSR commissioned support, CASSR managed personal budget) may not aways be populated in CLD. As such, full completeness across columns previously in LTS001c may not be possible. 

For the purposes of replicating SALT tables, which are typically disaggregated into 18-64 and 65 and over age bands, where a client has missing age information, they would not be included in these tables as they cannot be mapped to an age band.

Age in the SQL code is a proxy derived from the Birth Month and Birth Year fields, as these were the fields available to NHS England in the CLD Database. Accurate age fields can replace these if user has access to these fields

‘Latest Submission’ procedure at the beginning of the code takes the last submission (date and time) for each Local Authority within the relevant period of interest. This is used on the understanding that the last data submitted by each Local Authority in each quarterly window is the latest, complete picture to date. If a Local Authority submits a partial return or a top-up of a specific cohort as their last submission before the submission deadline, this will cause under-counting and inaccurate reporting for the LA in question. 

NHS Number is used as a unique identifier for each Client wherever possible. Where NHS number is not populated the Local Authority unique ID is used instead, if this can be done without compromising accuracy. In instances where no ID can be attributed to an event row without introducing the risk of either double-counting or incorrect allocation of identifiers to individuals, these event rows will be removed from the headcount (see Glossary of key concepts for further information). 

Code is written as at Q3 for 2023/24, the latest submission as per time of creation. Date filters can be amended as needed

Any Reference Data tables needed for the process are built as temporary tables in the script. These can alternatively be built as permanent tables if the environment the code is being run in allows. These Reference tables should periodically be checked against the Client Level Data Specification to ensure the Defined Lists haven’t changed and labels are still up-to-date