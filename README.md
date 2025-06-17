# Ad-Spot-Rating-Data-Cleaning
Cleaned and transformed Excel data to assign ad ratings by station, time band, and day of week. Used unpivoting, identifier matching, and Excel functions like VLOOKUP. Project took 2+ days to complete and shows strong data wrangling skills.
### A Media house Large dataset Data cleaning
-Completed a detailed Excel-based data transformation project where I matched thousands of ad spot logs with listenership ratings using structured data cleaning steps, unpivoting, station reconciliation, and formula logic (e.g., VLOOKUP, TRIM, CLEAN).

Over 2 days of effort went into transforming messy broadcast logs into actionable audience data — a great showcase of spreadsheet wrangling and documentation.
# 📻 Ad Spot Rating Data Cleaning using Excel

This project demonstrates a comprehensive data cleaning and standardization workflow in Excel to assign correct **listenership ratings** to ad spots based on **station**, **day of the week**, and **time band**. It showcases hands-on data wrangling using spreadsheet functions and logic.

---

## 🎯 Objective

To assign a listenership rating to each ad spot in the **Adcluster Table**, using corresponding information from the **Planning Module**, based on:
- The **Radio Station**
- The **Day of the Week**
- The **Time Band** (e.g., 6:00 AM–6:15 AM)

If an ad played on *WAZOBIA FM ABUJA* at *6:10 AM* on *Jan 1*, the goal was to fetch the appropriate audience rating from the Planning Table and assign it to that entry.

---

## 🔧 Data Cleaning Process

I spent over **2 days** cleaning and aligning these datasets.

### 🗂️ Step-by-step Actions Taken:

1. **Removed Irrelevant Rows**  
   - Deleted ~12,340 rows in the Planning Table that had **0 ratings** from Monday to Sunday (non-useful data).

2. **Unpivoted Days into Rows**  
   - Transformed day columns (Monday–Sunday) into single rows to allow matching based on `Day of Week`.

3. **Standardized Identifiers**  
   - Gave each category a unique code for easier matching:
     - Time Bands: `T1` to `T96`
     - Days: `D1` to `D7`
     - Stations: `S1` to `S320`

4. **Cleaned Station Names**  
   - Used `TRIM(CLEAN())` to clean station names.
   - Sorted stations A–Z in both tables.
   - Compared `Adcluster` station names with `Planning Table`, corrected mismatches.
   - Replaced unmatched stations – **colored in red** in the final sheet.

5. **Used Formulas for Matching**
   - VLOOKUPs were used to pull the right ratings:
     ```excel
     =VLOOKUP(TRIM(CLEAN(W2)), A:I, 7, FALSE)
     ```

6. **Audited the Process**
   - Counted filtered-out rows to validate logic.
   - Cross-verified distinct stations in both datasets (shown in `Distinct` sheet).

---[Uploading ASSESSMENT.xlsx…]()

[Uploading AdCluster test (1).xlsx…]()

## 📂 Files in this Repository

| File | Description |
|------|-------------|
| `Adcluster_Analysis.xlsx` | The Data before the data cleaning process |
| 'ASSESSMENT'| THE Dataset After the data cleaning process|
| `Readme` | Project documentation and explanation of process |

---

## 📈 Key Skills Demonstrated

- Advanced Excel Data Cleaning  
- Unpivoting and Normalization  
- Station Matching and Reconciliation  
- Logical Formulas (VLOOKUP, CLEAN, TRIM)  
- Documentation and Process Reporting  

---

## 🪄 Future Suggestions

- Automate this workflow using **Power Query**, **Python (pandas)** or **SQL**
- Add visuals and dashboards showing top-performing time slots/stations

---

## 👩‍💻 Author

**[https://www.linkedin.com/in/olufunmilolaolaewe/]**  
📧 [olufunmilolaolapejuolaewe@gmail.com]  
📌 *Committed to quality data work in media, advertising, and beyond.*
