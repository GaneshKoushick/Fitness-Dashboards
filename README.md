# Fitness Dashboard — Power BI Project

![Dashboard Screenshot]((https://drive.google.com/file/d/1Dg56R3PIBUAL4y_E3SIjs1wY0aigHFyz/view?usp=sharing))

## 📖 Overview
This project is a **Power BI dashboard** built using a single Excel dataset (`Dataset.xlsx`).  
It tracks **fitness memberships, monthly activity, revenue, expenses, and profit**.  
All calculations are implemented using **Power BI measures** on top of the dataset.

---

## 📂 Repository Structure
/
├─ README.md ← project documentation
├─ data/
│ └─ Dataset.xlsx ← raw dataset (Excel file)
├─ dashboard/
│ └─ FitnessDashboard.pbix ← Power BI report file
├─ assets/
│ └─ dashboard.png ← dashboard screenshot

markdown
Copy code

---

## 📊 Key Metrics in Dashboard
- **Revenue**: 4.1M  
- **Expenses**: 1.2M  
- **Profit**: 2.9M  
- **Clients**: 100  
- **Trainers**: 20  
- **Memberships**:  
  - Platinum → 18 Active, 15 Expired  
  - Gold → 15 Active, 20 Expired  
  - Silver → 11 Active, 21 Expired  

---

## ⚙️ Power BI Measures
The following DAX measures were created to drive insights:

- **Revenue** = SUM(`Dataset[Revenue]`)  
- **Expenses** = SUM(`Dataset[Expenses]`)  
- **Profit** = [Revenue] - [Expenses]  
- **Active Clients** = COUNTROWS(FILTER(`Dataset`, `Dataset[Status]` = "Active"))  
- **Expired Clients** = COUNTROWS(FILTER(`Dataset`, `Dataset[Status]` = "Expired"))  
- **Active %** = DIVIDE([Active Clients], [Total Clients], 0)  
- **Expired %** = DIVIDE([Expired Clients], [Total Clients], 0)  

*(adjust measure names if you used different naming)*  

---

## 📈 Visuals in the Dashboard
- KPI Cards → Revenue, Expenses, Profit  
- Pie/Donut Chart → Active vs Expired memberships  
- Membership Breakdown → Platinum / Gold / Silver  
- Monthly Trend → Bar chart of members across Jan–Dec  
- Client Membership Table → Username, Status, Progress %  

---

## 📥 Download Dataset & Assets
Dataset (`Dataset.xlsx`) and background image are available here:  
🔗 [Google Drive Folder](https://drive.google.com/drive/folders/1XPkFLSo0CLMDmpgqJ0OwxU_toEAir9uk?usp=sharing)

---

## ▶️ How to Open
1. Clone/download this repository.  
2. Download the dataset and background image from the Google Drive link above.  
3. Open `dashboard/FitnessDashboard.pbix` in Power BI Desktop.  
4. Ensure the dataset path is updated if needed (`data/Dataset.xlsx`).  
