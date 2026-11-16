# UST → Hang Hau Advisor

Bus, minibus or taxi? A COMP1945 (HKUST) Group 23 prototype that predicts whether the **KMB 91M bus**, the **GMB 11M minibus** or a **taxi** gets you from HKUST North to Hang Hau MTR Station in time.

- Enter your target arrival time and how many people are ahead of you in each queue.
- The page reads live arrival times (KMB and Transport Department ETA APIs) and weather (Hong Kong Observatory) from DATA.GOV.HK.
- Waiting and ride times come from linear regression models trained in KNIME. A KNN "nearest past trips" estimate is shown as a second opinion.

**Data:** 53 real trips collected by the team at the HKUST North stop between 19 Oct and 13 Nov 2026 (32 on the 91M, 21 on the 11M). Trained on the first 42 trips and tested on the last 11. On those 11 trips the waiting-time model's error is about ±5.9 min, about the same as a simple "vehicles × gap between buses" rule. Treat every time as roughly ± 6 minutes and keep a safety margin.

Files: `index.html` (the whole app) and `model_data.csv` (the real trips, used for the KNN comparison).
