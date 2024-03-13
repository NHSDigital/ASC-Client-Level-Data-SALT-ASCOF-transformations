This script uses a series of logic designed to remain as true to the principles of SALT as possible. The ST-Max events that the code uses is taken from the 
cohort fed directly from the STS001 (New Client Requests) table, where sequel to Request for support was identified as ST-Max. The STS001 cohort will need 
creating first, this can be done by running the accompanying STS001 SQL script and following the instructions.

The methodology used by the SQL script is to find completed ST-Max episodes within the period of interest and then search through the subsequent 
Event activity for the Client in question, to ascertain what followed the ST-Max episode. See Transformation Principles document for high level 
step-by-step methodology.

Invalid Event Outcomes (as per CLD spec) may affect the performance of the script and the accuracy of the sequel allocation. Especially NULL values 
in the Event Outcome field – these will lead to some joins not working correctly when code is left joining a NULL value to a NULL value

This code in current form produces sequels to ST-Max events, by SALT category (as per STS002a) and LA. To produce the further breakdowns
by Route Of Access, Primary Support Reason and Ethnicity for Tables 1-4, the relevant fields will need to be added to the SELECT field list of table 
build #ST_MAX_BUILD and pulled through into subsequent table builds after this

Full Early cessation of service is not possible to derive from CLD (as per the guidance) and as such these categories will not be fully represented 
in the sequel outputs
