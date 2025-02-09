
### 🏥 **Hospital Emergency Room Dashboard - Microsoft Excel Project**  

📊 **An End-to-End Dashboard Project in Excel using Power Query for Analyzing Hospital Emergency Room Performance**  

---

## 📌 **Project Overview**  
This project aims to create a **Hospital Emergency Room Analysis Dashboard** using **Excel and Power Query** to improve efficiency and provide useful insights. The dashboard enables stakeholders to **monitor, analyze, and make better decisions** for managing patients and improving healthcare services.  

---

## 🎯 **Purpose**  
- Provide a **data-driven approach** to analyze emergency room operations.  
- Help hospital administrators **optimize patient care** and **reduce wait times**.  
- Improve **resource allocation** and **service efficiency**.  

---

## 📊 **Key Performance Indicators (KPIs)**  
The dashboard includes the following key metrics:  

1. **Patient Admission Status** – Number of **admitted vs. non-admitted** patients.  
2. **Patient Age Distribution** – Categorizing patients into **age groups**.  
3. **Timeliness of Service** – Percentage of patients seen **within 30 minutes**.  
4. **Gender Analysis** – Distribution of patients **by gender**.  
5. **Department Referrals** – Identifies which **departments receive the most referrals**.  

---

## 🛠 **Data Processing & Formulas**  
### **📊 Data Handling with Power Query**  
- **Data Cleaning:** Removed duplicates, handled missing values, and standardized formats.  
- **Data Transformation:** Applied filters, created calculated columns, and grouped data for analysis.  
- **Data Loading:** Imported and refreshed data dynamically within Excel.  

### **📅 Calendar Table Formula**  
This formula generates a **date range** from **January 1, 2023**, for **731 days** (2 years):  
```DAX
= List.Dates(#date(2023,01,01),731,#duration(1,0,0,0))
```

### **🔢 DAX Formulas**  
1. **Age Group Classification**  
   ```DAX
   =IF([Patient Age]>=70,"70-79",
      IF([Patient Age]>=60,"60-69",
         IF([Patient Age]>=45,"45-59",
            IF([Patient Age]>=30,"30-44",
               IF([Patient Age]>=15,"15-29",
                  IF([Patient Age]>=5,"05-14","0-4"))))))
   ```  
   
2. **Patient Timeliness Status**  
   ```DAX
   = IF ([Patient Waittime] < 30, "Within Time", "Delayed")
   ```  

---

## 📊 **Final Dashboard**  
The final **Excel dashboard** includes multiple **visualizations and reports**, allowing users to:  
- **Monitor** patient admissions and wait times.  
- **Analyze** patient demographics.  
- **Identify** performance bottlenecks in emergency room services.
  ![Screenshot 2025-02-09 141107](https://github.com/user-attachments/assets/26ac4499-d780-4b6b-8755-9199c77ebfd4)


---

## 🛠 **Tools & Technologies Used**  
- **Excel** (for data storage and dashboard creation)  
- **Power Query** (for data transformation and processing)  
- **DAX (Data Analysis Expressions)** (for calculated columns and measures)  

---

## 🚀 **How to Use**  
1. **Download** the Excel file containing the dataset and Power Query transformations.  
2. **Open Excel** and navigate to the Power Query editor.  
3. **Refresh the data** to update insights dynamically.  
4. **Apply DAX formulas** for calculated metrics.  
5. **Visualize** insights using Excel charts and pivot tables.  

---

## 📌 **Future Enhancements**  
🔹 Integrate **real-time data sources** for live monitoring.  
🔹 Add **predictive analytics** for forecasting emergency room trends.  
🔹 Implement **automated reporting** for hospital administration.  

---

## 📜 **License**  
This project is **open-source** under the MIT License.  

---
