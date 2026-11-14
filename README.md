# UST → Hang Hau Advisor

Bus, minibus or taxi? A COMP1945 (HKUST) Group 23 prototype that predicts whether the **KMB 91M bus**, the **GMB 11M minibus** or a **taxi** gets you from HKUST North to Hang Hau MTR Station in time.

- Enter your target arrival time and how many people are ahead of you in each queue.
- The page reads live arrival times (KMB and Transport Department ETA APIs) and weather (Hong Kong Observatory) from DATA.GOV.HK.
- Waiting and ride times come from linear regression models trained in KNIME; a KNN "nearest past trips" estimate is shown as a second opinion.

**Data note:** the models were trained on 186 trips, of which 2 were observed and 184 were simulated from our real ETA and weather logger. Driving time is a typical value from our data, not live traffic.

Files: `index.html` (the whole app) and `model_data.csv` (trip data for the KNN comparison).
