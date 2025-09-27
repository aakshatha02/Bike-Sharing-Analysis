# 🚲 Bike Sharing Analysis (2011–2012)

This project explores the **Bike Sharing Dataset** from Washington D.C. (2011–2012) to understand how bike rental demand changes over time, across seasons, and under different weather conditions.  

The goal of the analysis is to find simple, descriptive insights supported by data visualizations that can help **operators and city planners** manage resources and improve the bikeshare system.  

---

## 📂 Dataset

- **Source:** [UCI Machine Learning Repository – Bike Sharing Dataset](https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset)  
- **Period:** 2011–2012 (two years)  
- **Location:** Washington D.C., USA  
- **Files:**
  - `day.csv`: daily aggregated rentals (731 days)  
  - `hour.csv`: hourly aggregated rentals (17,379 hours)  

### Key Features
- `dteday`: date  
- `season`: 1 = spring, 2 = summer, 3 = fall, 4 = winter  
- `yr`: 0 = 2011, 1 = 2012  
- `mnth`: month (1–12)  
- `hr`: hour (0–23, only in `hour.csv`)  
- `holiday`: whether the day is a holiday  
- `weekday`: day of the week  
- `workingday`: 1 if not weekend/holiday, otherwise 0  
- `weathersit`: categorical weather situation  
  - 1 = Clear / Partly cloudy  
  - 2 = Mist / Cloudy  
  - 3 = Light Snow / Light Rain  
  - 4 = Heavy Rain / Thunderstorm / Snow  
- `temp`: normalized temperature (Celsius ÷ 41)  
- `atemp`: normalized “feels-like” temperature (Celsius ÷ 50)  
- `hum`: normalized humidity (÷ 100)  
- `windspeed`: normalized wind speed (÷ 67)  
- `casual`: count of casual users  
- `registered`: count of registered users  
- `cnt`: total rentals (casual + registered)  

---

## 🛠️ Tools Used

- Python  
- Pandas, Polars  
- Matplotlib, Seaborn  
- Databricks Community Edition  

---

## 🧹 Data Cleaning

- No missing values were found.  
- The `yr` column was mapped as `0 = 2011` and `1 = 2012`.  
- Columns like `season`, `weathersit`, `weekday`, and `mnth` were converted to categorical types to make analysis and grouping easier.  

---

## 📊 Analysis & Key Findings

1. **Overall Trends**
   - Bike rentals grew from 2011 to 2012, showing increasing popularity.  
   - Registered users consistently outnumbered casual users.  

2. **Seasonal & Weekly Patterns**
   - Rentals peak in summer and fall, drop in winter.  
   - Weekday rentals are steady, reflecting commuting patterns.  
   - Daily patterns show two strong peaks: **morning and evening rush hours**.  

3. **Weather Effects**
   - Rentals rise with warmer temperatures.  
   - Clear days have the highest rentals; rainy/snowy days show sharp declines.  
   - Registered users ride more consistently in bad weather, while casual users mostly ride in good weather.  

4. **Correlation Insights**
   - **Temperature** and **year** have strong positive correlations with rentals.  
   - **Weather situation**, **humidity**, and **windspeed** show negative correlations.  
   - Registered users are the main driver of overall demand.  

---

## ✅ Conclusion

- **Season and weather** strongly influence bike usage: more rentals in warm, clear conditions, fewer in cold or rainy weather.  
- **Registered users** provide steady demand year-round, while **casual users** bring seasonal spikes.  
- Daily rental peaks match commuting times, confirming bikeshare is an important transport mode.  
- Overall growth from 2011 to 2012 shows the increasing role of bikeshare in urban mobility.  

These insights can help bikeshare operators **forecast demand, manage inventory, and plan infrastructure** to better serve riders.  

---

## 📎 References

- Fanaee-T, Hadi, and Gama, João. "Event labeling combining ensemble detectors and background knowledge." *Progress in Artificial Intelligence* (2013).  
- Dataset: [UCI ML Repository – Bike Sharing Dataset](https://archive.ics.uci.edu/dataset/275/bike+sharing+dataset)  

