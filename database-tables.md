# Database table list

**hose_prod_instruments_answer**  
Responses submitted by participants
	
**hose_prod_instruments_event**  
Interactions between participant and surveys, including all the times a participant stopped and restarted a survey
	
**hose_prod_instruments_instrument**  
Links questions, answers, and the frequency in which the survey is displayed to the participant. If there is no frequency set, the survey is supposed to be answered once.
	
**hose_prod_instruments_question**  
The survey questions, with its content and type of question (e.g. multi-select, number, slider, and text input).
	
**hose_prod_instruments_schedule**  
Scheduled survey instances. You will likely not need this table.
	
**hose_prod_materials_studymaterialinventory**  
Information about study materials registered, including barcode, label, description, and participant ID of the participant assigned to the material.
	
**hose_prod_materials_studymaterialrecord**  
Record of a study material scanned by a participant.
	
**hose_prod_measurements_appcategory**  
App categories retrieved from Android app stores
	
**hose_prod_measurements_measurement**  
GPS coordinates 
	
**hose_prod_measurements_mobility**  
Data derived from GPS, including travelled distance and radius of gyration.
	
**hose_prod_measurements_mobilityactivity**  
Identified activities from background geolocation (e.g. walking, in vehicle)  
	
**hose_prod_measurements_screentime**  
Time participants spend in apps, by app category. (Android only)
	
**hose_prod_stats_administrativedivision**  
Geographical/political divisions (e.g. country, state, cities, counties).
	
**hose_prod_stats_airquality**  
Air quality data by zip code, retrieved from airnowapi.org. Data is linked to hose_prod_stats_administrativedivision at the county level https://docs.airnowapi.org/docs/HourlyDataFactSheet.pdf
	
**hose_prod_stats_fitbitcredentials**  
Participant Fitbit credentials.
	
**hose_prod_stats_fitbitinfo**  
Metadata about the Fitbit account
	
**hose_prod_stats_fitbitintradayrecord**  
Fitbit data retrieved at seconds and minutes granularity, including heart rate, steps, distance travelled and calories. 

**hose_prod_stats_fitbitintradayrecord_v2**  	
See above
	
**hose_prod_stats_fitbitrecord**  
Data retrieved at a day granularity, including steps, calories, and heart rate. 
	
**hose_prod_stats_pollen**  
Pollen count from pollen.com
	
**hose_prod_stats_studyfitbitcredentials**  
Participant Fitbit credentials.
	
**hose_prod_stats_weather**  
Weather, temperature, and humidity data from openweathermap.org
	
**hose_prod_users_participanttype**  
User types within the study, such as Ambassador, Primary, etc.
	
**hose_prod_users_study**  
Table stores study names. You will always use the Whole Communities Whole Health study for queries. 
	
**hose_prod_users_studychildparticipant**  
Represents a child participant linked to a parent study participant.
	
**hose_prod_users_studyparticipant**  
Participants table. Each study participant is assigned a unique identifier 

**hose_prod_users_studyparticipant_types**
This table links participant IDs with type IDs
	
**hose_prod_users_user**  
Information about participant vs admin users. 
	
**research_demographics**  
Supplemental adult demographics. The most current demographc information comes from participant surveys
	
**research_demographics_child**  
Supplemental child demographics. The most current demographc information comes from participant surveys
	
**research_lena**  
LENA metadata
