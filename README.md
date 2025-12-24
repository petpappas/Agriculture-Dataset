## Dataset Overview

This dataset contains detailed information on 50 farms and their crop production activities. It consists of 10 columns capturing farm characteristics, cultivation practices, and crop yield.


## Key Features

**Farm_ID**: Unique identifier for each farm.

**Crop_Type**: Type of crop being cultivated.

**Farm_Area (acres)**: Size of the farm, averaging 255 acres with considerable variability (std = 139 acres).

**Irrigation_Type**: Method of irrigation employed.

**Fertilizer_Used (tons)**: Fertilizer application, averaging 4.9 tons per farm.

**Pesticide_Used (kg)**: Pesticide usage, averaging 2.4 kg per farm.

**Yield (tons)**: Crop yield, averaging 27 tons.

**Soil_Type**: Type of soil on the farm.

**Season**: Season of cultivation.

**Water_Usage (cubic meters)**: Water consumption, averaging 56,724 cubic meters.



## Statistical Insights

- Farms vary widely in size and input usage, reflecting diverse cultivation practices.

- Fertilizer and pesticide application show moderate variability.

- Crop yields are reasonably consistent, and water usage is significant across farms.

- This dataset is ideal for analyzing the relationship between farm practices, resource usage, and crop productivity.




## 🔹 Unique Values & Column Types

### Numerical Columns
- `Farm_Area(acres)`, `Fertilizer_Used(tons)`, `Pesticide_Used(kg)`, `Yield(tons)`, `Water_Usage(cubic meters)`

### Categorical Columns
- `Farm_ID`, `Crop_Type`, `Irrigation_Type`, `Soil_Type`, `Season`

### Categorical Column Unique Values
- **Farm_ID:** F001 – F050  
- **Crop_Type:** Cotton, Carrot, Sugarcane, Tomato, Soybean, Rice, Maize, Wheat, Barley, Potato  
- **Irrigation_Type:** Sprinkler, Manual, Flood, Rain-fed, Drip  
- **Soil_Type:** Loamy, Peaty, Silty, Clay, Sandy  
- **Season:** Kharif, Zaid, Rabi


## 📊 Exploratory Data Analysis (EDA)

### Univariate Analysis of Numerical Columns
- **Farm Area:** Wide range (12.5 – 483.88 acres), slightly right-skewed.  
- **Fertilizer Used:** Average ~4.9 tons, moderate variability, a few high-value outliers.  
- **Pesticide Used:** Average ~2.4 kg, left-skewed, some high-value outliers.  
- **Yield:** Average ~27 tons, right-skewed distribution.  
- **Water Usage:** Wide range (5,869 – 94,754 m³), right-skewed, some high consumption outliers.

**Boxplots** and **summary statistics** were used to identify ranges, median values, and potential outliers.

---

### Categorical Column Analysis
- **Crop Type:** Cotton, Carrot, and Tomato are most common; Potato and Barley less frequent.  
- **Irrigation Type:** Sprinkler and Manual dominant; Drip and Rain-fed less common.  
- **Soil Type:** Loamy and Silty most common; balanced distribution overall.  
- **Season:** Kharif season is most prevalent, followed by Zaid and Rabi.

**Distribution plots** include counts and percentage pie charts for each category.




| Metric                     | Crop Type | Value       |
|----------------------------|-----------|------------|
| Highest Yield              | Tomato    | 48.02 tons |
| Lowest Yield               | Maize     | 3.86 tons  |
| Highest Fertilizer Used    | Cotton    | 9.96 tons  |
| Lowest Fertilizer Used     | Cotton    | 0.50 tons  |
| Highest Pesticide Used     | Rice      | 4.99 kg    |
| Lowest Pesticide Used      | Barley    | 0.14 kg    |
| Highest Water Usage        | Cotton    | 94,754.73 m³ |
| Lowest Water Usage         | Rice      | 5,869.75 m³ |
| Highest Farm Area          | Rice      | 483.88 acres |
| Lowest Farm Area           | Sugarcane | 12.50 acres |

**Insights:**
- **Yield:** Tomato is the most productive crop; Maize yields the least.  
- **Fertilizer:** Cotton shows the highest variation in fertilizer usage.  
- **Pesticide:** Rice uses the most pesticides; Barley the least.  
- **Water Usage:** Cotton is very water-intensive; Rice shows low usage (efficient practices).  
- **Farm Area:** Rice is cultivated on the largest farms, Sugarcane on the smallest.

These insights highlight variability in **resource usage, productivity, and farm size** across crop types, providing guidance for **optimized agricultural practices**.

---
