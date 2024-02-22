# Adult Social Care Client Level Data

## What is Client Level Data?

#### Adult Social Care CLient Level  Data (CLD) is a data product is created from data submitted to NHS England by Arden & GEM (AGEM) who collect the data from local authorities on a quarterly basis. This is then transferred to NHS England where data is pseudonymised centrally and made available to request through the Data Access Request Service (DARS). It contains data relating to adults over 18 who are receiving social care services, informal carers and events where the care is provided or arranged by the local authority. 


#### Following a 12-month period of dual running in 2023/24, CLD will replace the Short and Long Term (SALT) collection in 2024/25. CLD is seen as an evolution of the SALT return, containing more granular detail and timeliness to allow for more flexible and broader analytical use.


## What is the purpose of these SQL codes?

#### The codes are intended to replicate (wherever possible) the metrics previously captured in the Short and Long Term Support (SALT) collection, using the Client Level Data, where there is an ongoing need for this insight. The code processes have been written to be as true to the original principles of SALT as possible and filter, process, de-duplicate and aggregate the data in a way that closest matches SALT.


## How to apply them

#### Database names, table names, field names etc will need to be changed to reflect those used locally. The codes were developed by NHS England using the access to the AGEM CLD Repository and as such the labels used reflect this. The principles of the base code should, however, be transferable once these adjustments are made.


## Known Limitations

#### As a new data collection, with a change in the underlying source, metrics derived from CLD are not expected to perfectly match those from SALT (and a small number of fields in SALT Reproducing SALT and ASCOF metrics from Client Level Data were not carried over to the CLD specification). However, the approach outlined is intended to stay in line with principles adopted by SALT. See the individual Limitations associated with each measure for more specific information

