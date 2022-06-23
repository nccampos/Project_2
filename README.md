# ETL: Electric Cars

## Purpose
To see ownership of electric vehicles by state, and whether there is a correlation between vehicle speed and ownership.


## Data Sources

-Quickest Electric Cars
https://www.kaggle.com/datasets/kkhandekar/quickest-electric-cars-ev-database
(Kaggle)

-EV Vehicle Registrations by State
https://www.atlasevhub.com/materials/state-ev-registration-data/
(Atlas EV Hub, Open Vehicle Registration Initiative)

*Note: Due to the large file size of several datasets used in this project, we were unable to upload those original files to this repository.
When trying these programs yourself, please make sure to download the following files:

- ca_ev_registrations_public.csv (Atlas EV Hub)
- ny_ev_registrations_public.csv (Atlas EV Hub)
- wa_ev_registrations_public.csv (Atlas EV Hub)

...and place them within the 'Resources' folder.*


## Process

For the state registration data, we decided to limit the data to the top ten states with the most data.
We downloaded all the csv files, and imported them into Python using pandas.

We then cleaned the data with the following processes:
- Deleted null values
- Renamed columns across all dataframes
- Added new columns for state abbreviations
- Deleted superfluous columns
- Separated columns listing both make and model of cars into two
- Found total amounts of each unique make and model, and grouped into new dataframes

Once all the data was cleaned, we exported the results to SQL, using sqlalchemy and PostGRE SQL.


## Insights

Fastest car is in the brand name “Lucid”
Brand vs acceleration in sec
![image](https://user-images.githubusercontent.com/37030745/175138545-e7379574-4668-4897-906a-7496584d9996.png)

 
2) Which has the highest efficiency?
Byton have the highest efficiency
Brand Vs Efficiency
 ![image](https://user-images.githubusercontent.com/37030745/175138933-028d0248-0d22-484a-befb-91b909eb8a27.png)

3) Does a difference in power train effect the range, top speed, efficiency?

![image](https://user-images.githubusercontent.com/37030745/175140122-035b1a25-ac90-4577-96a7-0d17be89a1fa.png)
![image](https://user-images.githubusercontent.com/37030745/175139546-5021af0c-008f-4435-bc48-9710385f4846.png)
![image](https://user-images.githubusercontent.com/37030745/175141384-6723ea46-97cb-46ec-882c-a58ec963b45b.png)

  
4) Which manufacturer has the greatest number of vehicles?
Tesla produces most number of vehicles
5) How does price relate to rapid charging?

![image](https://user-images.githubusercontent.com/37030745/175141204-e5fd3e43-5be8-46fc-a958-8433d012e3da.png)

Cars having rapid charge are more costly
 
Conclusion:

Lucid brand have car which is fastest accleration time. 
AWD is dominating every segment (.i.e Range,SpeeD,Efficiency). 
Byton having most efficient car. 
Tesla is producing most car every year. 
Car having Rapid charge are most costly.
