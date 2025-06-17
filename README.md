# 📻 Ad Spot Rating Data Cleaning using Excel

A hands-on Excel-based data cleaning and transformation project that maps radio ad spot logs to accurate listenership ratings by matching ad station, time band, and day of the week with a reference Planning Table. Over 2 days of work involving heavy data wrangling, unpivoting, identifier coding, VLOOKUP logic, and station reconciliation. Demonstrates mastery of Excel data prep, auditing, and structured documentation.

---

## 📚 Table of Contents

- [🎯 Objective](#-objective)
- [🛠️ Data Cleaning Process](#-data-cleaning-process)
- [📂 Files in this Repository](#-files-in-this-repository)
- [📈 Key Skills Demonstrated](#-key-skills-demonstrated)
- [🪄 Future Suggestions](#-future-suggestions)
- [👩‍💻 Author](#-author)

---

## 🎯 Objective

To assign a listenership rating to each ad spot in the **Adcluster Table**, using corresponding information from the **Planning Module**, based on:
- The **Radio Station**
- The **Day of the Week**
- The **Time Band** (e.g., 6:00 AM–6:15 AM)

Example:  
If an ad played on *WAZOBIA FM ABUJA* at *6:10 AM* on *Jan 1*, the goal was to fetch the appropriate audience rating from the Planning Table and assign it to that entry.

---

## 🛠️ Data Cleaning Process

I spent over **2 days** cleaning and aligning these datasets.

### 🗂️ Step-by-step Actions Taken

1. **Removed Irrelevant Rows**  
   - Deleted ~12,340 rows in the Planning Table that had **0 ratings** from Monday to Sunday.

2. **Unpivoted Days into Rows**  
   - Converted day columns (Mon–Sun) into single rows to normalize the structure.

3. **Created and Applied Unique Identifiers**  
   - Time Bands: `T1`–`T96`  
   - Days: `D1`–`D7`  
   - Stations: `S1`–`S320`

4. **Cleaned and Standardized Station Names**  
   - Applied `=TRIM(CLEAN())` in Excel  
   - Sorted and matched station names  
   - Replaced mismatches in the Adcluster table (**colored red**)  

5. **Used Excel Formulas for Rating Mapping**
   - Example formula:
     ```excel
     =VLOOKUP(TRIM(CLEAN(W2)), A:I, 7, FALSE)
     ```

6. **Audited the Process**
   - Counted rows removed for transparency  
   - Validated distinct station names using the `Distinct` sheet

---

## 📂 Files in this Repository

| File Name                  | Description |
|---------------------------|-------------|
| `Adcluster_Analysis.xlsx` | The original Adcluster and Planning Module tables before cleaning |
| `ASSESSMENT.xlsx`         | Final cleaned dataset with mapped listenership ratings |
| `README.md`               | This documentation file |

---

## 📈 Key Skills Demonstrated

- Excel Data Cleaning  
- Data Normalization & Unpivoting  
- Lookup Logic (VLOOKUP, CLEAN, TRIM)  
- Data Reconciliation Across Tables  
- Auditability and Transparency  
- Documentation and Reporting

---

## 🪄 Future Suggestions

- Automate with **Power Query**, **Python (pandas)**, or **SQL**
- Visualize trends across stations and time bands
- Add a dashboard for deeper insights

---

## 👩‍💻 Author

**Olufunmilola Olaewe**  
[LinkedIn Profile](https://www.linkedin.com/in/olufunmilolaolaewe/)  
📧 olufunmilolaolapejuolaewe@gmail.com

---

📌 *Passionate about transforming raw data into meaningful insights, especially in media and advertising domains.*
