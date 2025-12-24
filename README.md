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



## 🌱 Crop Type and Farm Associations

**Key Findings:**

- Each crop type is associated with distinct farms.  
- **No farm grows multiple crop types.**

| Crop Type  | Farm IDs                                |
|-----------|----------------------------------------|
| Barley    | F016, F020, F025, F031, F033, F038, F049 |
| Carrot    | F002, F017, F032, F046                  |
| Cotton    | F001, F021, F027, F036, F039, F040, F043 |
| Maize     | F009, F018, F019                        |
| Potato    | F023, F030, F047, F048                  |
| Rice      | F008, F011, F014, F024, F041            |
| Soybean   | F007, F010, F035, F037, F044            |
| Sugarcane | F003, F006, F012, F015, F042            |
| Tomato    | F004, F005, F028, F034, F045, F050      |
| Wheat     | F013, F022, F026, F029                  |

**Insights:**  
- Crops like Barley, Cotton, Tomato appear in multiple farms.  
- Maize and Potato appear in fewer farms, possibly reflecting lower popularity or demand.  

**Visualization:** Pie chart for farm distribution by crop type.

---

## 🌾 Total Farm Area by Crop Type

| Crop Type  | Total Farm Area (acres) |
|------------|------------------------|
| Cotton     | 1,993.80               |
| Rice       | 1,845.24               |
| Barley     | 1,671.22               |
| Tomato     | 1,655.02               |
| Sugarcane  | 1,187.99               |
| Soybean    | 1,050.68               |
| Maize      | 978.53                 |
| Wheat      | 872.57                 |
| Carrot     | 765.90                 |
| Potato     | 727.24                 |

**Insights:**  
- Largest areas: Cotton, Rice, Barley  
- Medium areas: Tomato, Sugarcane, Soybean  
- Smallest areas: Carrot, Potato, Wheat, Maize  

**Visualization:** Pie chart for farm area distribution by crop type.

---

## 🌱 Crop and Soil Type Relationships

| Crop Type  | Soil Types                   |
|------------|-----------------------------|
| Barley     | Sandy, Silty, Clay, Loamy    |
| Carrot     | Peaty, Loamy, Clay           |
| Cotton     | Loamy, Clay, Sandy           |
| Maize      | Peaty, Loamy, Sandy          |
| Potato     | Loamy, Sandy, Silty          |
| Rice       | Silty, Clay, Sandy           |
| Soybean    | Sandy, Silty, Loamy          |
| Sugarcane  | Silty, Loamy, Clay, Peaty    |
| Tomato     | Silty, Clay, Loamy, Peaty    |
| Wheat      | Clay, Loamy, Silty           |

**Insights:**  
- **Loamy soil** → high yields for Barley, Carrot, Soybean, Sugarcane  
- **Sandy soil** → high yields for Cotton, Maize, Potato  
- **Clay soil** → high yields for Rice, Tomato  

**Visualization:** Pie charts for soil type distribution by crop type.

---

## 📅 Crop Season Distribution

| Crop Type  | Seasons            |
|------------|------------------|
| Barley     | Zaid, Kharif      |
| Carrot     | Kharif, Zaid, Rabi|
| Cotton     | Kharif, Rabi, Zaid|
| Maize      | Rabi, Zaid        |
| Potato     | Zaid, Kharif      |
| Rice       | Kharif, Zaid, Rabi|
| Soybean    | Rabi, Kharif, Zaid|
| Sugarcane  | Kharif, Zaid      |
| Tomato     | Zaid, Rabi, Kharif|
| Wheat      | Zaid, Rabi        |

**Insights:**  
- Multi-season crops: Carrot, Rice, Soybean, Tomato  
- Season-specific crops: Maize, Wheat, Sugarcane  
- Balanced crops: Tomato, Wheat  

**Visualization:** Pie charts for season distribution by crop type.

---

## 🌟 Soil Type vs Crop Yield

| Crop Type  | Highest Yield Soil | Yield (tons) | Lowest Yield Soil | Yield (tons) |
|------------|-----------------|-------------|-----------------|-------------|
| Barley     | Loamy           | 46.47       | Sandy           | 17.44       |
| Carrot     | Loamy           | 47.70       | Clay            | 27.95       |
| Cotton     | Sandy           | 28.82       | Loamy           | 13.48       |
| Maize      | Sandy           | 39.96       | Peaty           | 3.86        |
| Potato     | Sandy           | 31.47       | Silty           | 20.53       |
| Rice       | Clay            | 33.66       | Silty           | 4.23        |
| Soybean    | Loamy           | 40.15       | Sandy           | 28.98       |
| Sugarcane  | Loamy           | 38.18       | Clay            | 17.19       |
| Tomato     | Clay            | 43.28       | Loamy           | 12.92       |
| Wheat      | Silty           | 36.90       | Clay            | 18.07       |

**Insights:**  
- Loamy soil → high yields for many crops  
- Sandy soil → variable performance depending on crop  
- Clay soil → high yields for Rice and Tomato, but lower for some others 
---

Fertilizer Usage by Soil Type
Highest Fertilizer Used per Crop
Crop Type	Soil Type	Fertilizer Used (tons)
Barley	Loamy	7.79
Carrot	Loamy	5.89
Cotton	Loamy	6.25
Maize	Loamy	4.91
Potato	Loamy	9.43
Rice	Clay	7.17
Soybean	Silty	8.57
Sugarcane	Loamy	6.42
Tomato	Clay	8.33
Wheat	Clay	6.11
Lowest Fertilizer Used per Crop
Crop Type	Soil Type	Fertilizer Used (tons)
Barley	Sandy	2.90
Carrot	Peaty	4.77
Cotton	Sandy	2.10
Maize	Peaty	0.57
Potato	Sandy	3.86
Rice	Sandy	4.60
Soybean	Loamy	1.18
Sugarcane	Clay	1.90
Tomato	Loamy	4.75
Wheat	Silty	1.79

Observations:

Loamy soils often require more fertilizer but yield high outputs.

Sandy soils have low fertilizer usage due to poor nutrient retention.

Fertilizer needs vary by crop-soil combination—targeted nutrient management is key.

💧 Water Usage by Soil Type
Highest Water Usage per Crop
Crop Type	Soil Type	Water Usage (m³)
Barley	Loamy	93,656
Carrot	Loamy	88,301
Cotton	Loamy	57,761
Maize	Peaty	60,202
Potato	Sandy	86,990
Rice	Sandy	78,581
Soybean	Loamy	73,647
Sugarcane	Silty	75,539
Tomato	Clay	93,719
Wheat	Loamy	65,838
Lowest Water Usage per Crop
Crop Type	Soil Type	Water Usage (m³)
Barley	Silty	39,957
Carrot	Peaty	68,726
Cotton	Clay	49,552
Maize	Loamy	18,660
Potato	Silty	5,874
Rice	Silty	9,392
Soybean	Silty	43,610
Sugarcane	Peaty	33,616
Tomato	Peaty	37,466
Wheat	Silty	23,208

Observations:

Loamy soils consume more water for high yields.

Silty soils have lower water needs due to better moisture retention.

Sandy soils require high water for crops like Potato and Rice because of drainage.

💧 Water Usage by Soil & Irrigation Type
Highest Water Usage
Crop Type	Soil Type	Irrigation Type	Water Usage (m³)
Barley	Loamy	Drip	93,656
Carrot	Loamy	Manual	88,301
Cotton	Sandy	Flood	94,755
Maize	Peaty	Drip	60,202
Potato	Loamy	Rain-fed	93,407
Rice	Sandy	Flood	78,581
Soybean	Loamy	Manual	73,647
Sugarcane	Clay	Flood	88,977
Tomato	Clay	Sprinkler	93,719
Wheat	Loamy	Flood	65,838
Lowest Water Usage
Crop Type	Soil Type	Irrigation Type	Water Usage (m³)
Barley	Sandy	Flood	25,132
Carrot	Peaty	Manual	68,726
Cotton	Sandy	Rain-fed	12,008
Maize	Loamy	Rain-fed	18,660
Potato	Silty	Sprinkler	5,874
Rice	Silty	Drip	9,392
Soybean	Sandy	Manual	40,614
Sugarcane	Peaty	Rain-fed	33,616
Tomato	Peaty	Sprinkler	37,466
Wheat	Silty	Manual	23,208

Observations:

Water usage depends heavily on soil + irrigation combination.

Flood irrigation generally consumes more water.

Drip/Sprinkler efficiency is influenced by soil type and crop.

🌾 Crop Yield by Season & Irrigation
Highest Yield
Crop Type	Season	Irrigation Type	Yield (tons)
Barley	Zaid	Drip	46.47
Carrot	Zaid	Manual	47.70
Cotton	Zaid	Rain-fed	46.19
Maize	Zaid	Drip	39.96
Potato	Kharif	Drip	31.47
Rice	Kharif	Flood	35.01
Soybean	Rabi	Drip	44.93
Sugarcane	Zaid	Sprinkler	32.24
Tomato	Rabi	Flood	48.02
Wheat	Zaid	Manual	36.90
Lowest Yield
Crop Type	Season	Irrigation Type	Yield (tons)
Barley	Zaid	Flood	11.34
Carrot	Rabi	Flood	24.34
Cotton	Zaid	Flood	10.99
Maize	Rabi	Drip	3.86
Potato	Zaid	Drip	18.13
Rice	Kharif	Drip	4.23
Soybean	Kharif	Drip	17.25
Sugarcane	Kharif	Flood	20.76
Tomato	Rabi	Drip	12.92
Wheat	Zaid	Drip	5.44

Observations:

Drip irrigation can be associated with both high and low yields depending on season and crop.

Flood irrigation is inefficient for some crops but high yielding for water-intensive crops like Cotton & Rice.

Highest yields mostly occur in Zaid & Rabi seasons.

🐞 Pesticide Usage by Season
Highest Pesticide Usage
Crop Type	Season	Pesticide Used (kg)
Barley	Kharif	2.21
Carrot	Rabi	2.94
Cotton	Kharif	3.49
Maize	Rabi	2.85
Potato	Kharif	2.68
Rice	Rabi	3.45
Soybean	Zaid	2.89
Sugarcane	Kharif	1.66
Tomato	Zaid	4.42
Wheat	Rabi	3.03
Lowest Pesticide Usage
Crop Type	Season	Pesticide Used (kg)
Barley	Zaid	1.56
Carrot	Zaid	0.81
Cotton	Rabi	0.91
Maize	Zaid	1.31
Potato	Zaid	2.25
Rice	Zaid	1.77
Soybean	Rabi	2.45
Sugarcane	Zaid	1.42
Tomato	Kharif	0.66
Wheat	Zaid	2.81
