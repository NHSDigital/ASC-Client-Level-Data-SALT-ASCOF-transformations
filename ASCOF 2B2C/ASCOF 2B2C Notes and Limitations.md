
As with all measures, the process is reliant on LAs accurately capturing fields as per the relevant specification defined lists. Any fields that are invalid as per the CLD specification are removed from the analysis – source data will not be corrected and invalid field entries cannot be mapped to the specification.  All invalid field entries are flagged and captured in the Data Quality Reports received by LAs to highlight areas to be corrected in future submissions. 

Age in the SQL code is a proxy derived from the Birth Month and Birth Year fields, as these were the fields available to NHS England in the CLD Database. Accurate age fields can replace these if user has access to these fields

For the purposes of disaggregating the measure into 2B and 2C, age information is required. Where a client has missing age information, they would not be included in either of the ASCOF measures.

Identifying if an admission is brand new is predicated on historical data being available since a new event can legitimately be created every time there is a change (even if the residential stay itself is long-standing) so there may be some over-counting compared with the current methodology 

The specification does not differentiate between permanent and temporary nursing and residential stays, and as this methodology is dependent on central transformation, without local triangulation, temporary admissions may be included going forwards. 

As part of a process to find the latest edition of each Event within the historical data, a new ‘EVENT ID’ is created within the script. This is used to avoid old versions of Events (from previous submissions) still showing as open and thus potentially falling in scope of the period of interest when a later version of the record has been marked as closed and NOT in scope of the period of interest. The newly-created EVENT ID uses a concatenation of numerous fields within CLD, where rows with a complete match indicate the same Event. This logic has been found to be more robust when applied across all LAs than the Event Reference Number (ERN) within CLD.

NHS Number is used as a unique identifier for each Client wherever possible. Where NHS number is not populated the Local Authority unique ID is used instead, if this can be done without compromising accuracy. In instances where no ID can be attributed to an event row without introducing the risk of either double-counting or incorrect allocation of identifiers to individuals, these event rows will be removed from the headcount (see Glossary of key concepts for further information). 

Code is written as at FY 2023/24, the latest submission as per time of creation. Date filters can be amended as needed

