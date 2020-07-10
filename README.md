# allergies
## Data Sources and Considerations

1. Daily Temperature data (via NOAA API): 
	* Daily minTemp data was collected for each city from 1950-2020
	* Seasons were classified using the following definitions:
		* Spring = Months 3-5
		* Summer = Months 6-8
		* Fall = Months 9-11
		* Winter = Months 12-2
	* “Frost season” length was calculated by determining the difference between the first day in fall and last day in spring with temperature <= 32°F; “Growing season” length was calculated by subtracting “Frost Season” from 365
	* 1995 Stockton, and several years in McAllen had no days in which the temperature was <= 32°F; these years were given a “growing season” value of 365

2. Practicing allergist data (via Medicare Provider Utilization data)
	* Provider practice data filtered by whether or not provider is an allergist
	* Used address to determine which county provider practices in
	* CMS data was joined with census population estimates to determine number of allergists per 100k people in county

3. Air pollution data (via CACES)
	* particulate matter (≤2.5 μm)
	* concentrations are listed as the variable "pred_weight"; units are micrograms per cubic meter for PM2.5
	* Data available from 1999-2015

4. Asthma prevalence data (via CDC)
	* Asthma prevalence data are self-reported by respondents to the National Health Interview Survey (NHIS). 
	* From 1997-2000, a redesign of the NHIS questions resulted in a break in the trend data as the new questions were not fully comparable to the previous questions. Data exists for 1980-96 and 2001-18.
	* 1980-96 source: Moorman JE, Akinbami LJ, Bailey CM, et al. National Surveillance of Asthma: United States, 2001 -2010. National Center for Health Statistics. Vital Health Stat 3 (35). 2012.
	* 2001-18 source: NHIS prevalence tables

5. Ranking of most challenging places to live for people with allergies (via AAFA 2020 report)
	1. Richmond, Virginia
	2. Scranton, Pennsylvania
	3. Springfield, Massachusetts
	4. Hartford, Connecticut
	5. McAllen, Texas
	6. New Haven, CT
	...
	95. Milwaukee, WI
	96. Stockton, California
	97. Salt Lake City, Utah
	98. Seattle, Washington
	99. Provo, Utah
	100. Durham, North Carolina
