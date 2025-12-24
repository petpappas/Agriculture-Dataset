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




##  Unique Values & Column Types

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


##  Exploratory Data Analysis (EDA)

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



##  Crop Type and Farm Associations

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

##  Total Farm Area by Crop Type

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

##  Crop and Soil Type Relationships

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

##  Crop Season Distribution

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

## Soil Type vs Crop Yield

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

| Crop Type | Highest Yield Soil | Yield (tons) | Lowest Yield Soil | Yield (tons) |
| --------- | ------------------ | ------------ | ----------------- | ------------ |
| Barley    | Loamy              | 46.47        | Sandy             | 17.44        |
| Carrot    | Loamy              | 47.70        | Clay              | 27.95        |
| Cotton    | Sandy              | 28.82        | Loamy             | 13.48        |
| Maize     | Sandy              | 39.96        | Peaty             | 3.86         |
| Potato    | Sandy              | 31.47        | Silty             | 20.53        |
| Rice      | Clay               | 33.66        | Silty             | 4.23         |
| Soybean   | Loamy              | 40.15        | Sandy             | 28.98        |
| Sugarcane | Loamy              | 38.18        | Clay              | 17.19        |
| Tomato    | Clay               | 43.28        | Loamy             | 12.92        |
| Wheat     | Silty              | 36.90        | Clay              | 18.07        |

**Insights:**

- Loamy soil generally supports the highest yields for many crops (Barley, Carrot, Soybean, Sugarcane).

- Sandy soil can provide high yields for some crops like Cotton, Maize, Potato, but may reduce yield for others like Barley and Soybean.

- Clay soil gives high yields for Rice and Tomato but lowers yields for some crops like Wheat.

- Soil-crop matching is crucial for optimizing yield
  
**2. Fertilizer Used per Soil Type**
| Crop Type | Highest Fertilizer Soil | Fertilizer Used (tons) | Lowest Fertilizer Soil | Fertilizer Used (tons) |
| --------- | ----------------------- | ---------------------- | ---------------------- | ---------------------- |
| Barley    | Loamy                   | 7.79                   | Sandy                  | 2.90                   |
| Carrot    | Loamy                   | 5.89                   | Peaty                  | 4.77                   |
| Cotton    | Loamy                   | 6.25                   | Sandy                  | 2.10                   |
| Maize     | Loamy                   | 4.91                   | Peaty                  | 0.57                   |
| Potato    | Loamy                   | 9.43                   | Sandy                  | 3.86                   |
| Rice      | Clay                    | 7.17                   | Sandy                  | 4.60                   |
| Soybean   | Silty                   | 8.57                   | Loamy                  | 1.18                   |
| Sugarcane | Loamy                   | 6.42                   | Clay                   | 1.90                   |
| Tomato    | Clay                    | 8.33                   | Loamy                  | 4.75                   |
| Wheat     | Clay                    | 6.11                   | Silty                  | 1.79                   |

**Insights:**

- Loamy soil often requires more fertilizer but rewards with higher yields.

- Sandy soil usually has low fertilizer use due to poor nutrient retention.

- Fertilizer requirements depend on crop-soil interaction, important for cost-effective farming.
  
**3. Water Usage per Soil Type**
| Crop Type | Highest Water Soil | Water Usage (m³) | Lowest Water Soil | Water Usage (m³) |
| --------- | ------------------ | ---------------- | ----------------- | ---------------- |
| Barley    | Loamy              | 93656.06         | Silty             | 39956.88         |
| Carrot    | Loamy              | 88301.46         | Peaty             | 68725.54         |
| Cotton    | Loamy              | 57761.24         | Clay              | 49551.67         |
| Maize     | Peaty              | 60202.14         | Loamy             | 18660.03         |
| Potato    | Sandy              | 86989.88         | Silty             | 5874.17          |
| Rice      | Sandy              | 78580.93         | Silty             | 9392.38          |
| Soybean   | Loamy              | 73646.55         | Silty             | 43610.21         |
| Sugarcane | Silty              | 75538.56         | Peaty             | 33615.77         |
| Tomato    | Clay               | 93718.69         | Peaty             | 37466.11         |
| Wheat     | Loamy              | 65838.40         | Silty             | 23208.04         |

**Insights:**

- Loamy soils generally require more water due to higher yields.

- Silty soils use less water, likely due to better moisture retention.

- Sandy soils can demand high irrigation for water-intensive crops.

- Highlights the importance of soil-aware irrigation strategies.
  
**4.Water Usage per Soil & Irrigation Type**
| Crop Type | Highest Water Soil/Irrigation | Water Usage (m³) | Lowest Water Soil/Irrigation | Water Usage (m³) |
| --------- | ----------------------------- | ---------------- | ---------------------------- | ---------------- |
| Barley    | Loamy / Drip                  | 93656.06         | Sandy / Flood                | 25132.48         |
| Carrot    | Loamy / Manual                | 88301.46         | Peaty / Manual               | 68725.54         |
| Cotton    | Sandy / Flood                 | 94754.73         | Sandy / Rain-fed             | 12007.70         |
| Maize     | Peaty / Drip                  | 60202.14         | Loamy / Rain-fed             | 18660.03         |
| Potato    | Loamy / Rain-fed              | 93407.38         | Silty / Sprinkler            | 5874.17          |
| Rice      | Sandy / Flood                 | 78580.93         | Silty / Drip                 | 9392.38          |
| Soybean   | Loamy / Manual                | 73646.55         | Sandy / Manual               | 40614.40         |
| Sugarcane | Clay / Flood                  | 88976.51         | Peaty / Rain-fed             | 33615.77         |
| Tomato    | Clay / Sprinkler              | 93718.69         | Peaty / Sprinkler            | 37466.11         |
| Wheat     | Loamy / Flood                 | 65838.40         | Silty / Manual               | 23208.04         |

**Insights:**

- Flood irrigation often leads to highest water usage.

- Drip and Sprinkler can be efficient but soil and crop type affect usage.

- Choosing appropriate irrigation per soil type is key to efficiency.
  
**5. Yield per Season & Irrigation Type**
| Crop Type | Highest Yield Season/Irrigation | Yield (tons) | Lowest Yield Season/Irrigation | Yield (tons) |
| --------- | ------------------------------- | ------------ | ------------------------------ | ------------ |
| Barley    | Zaid / Drip                     | 46.47        | Zaid / Flood                   | 11.34        |
| Carrot    | Zaid / Manual                   | 47.70        | Rabi / Flood                   | 24.34        |
| Cotton    | Zaid / Rain-fed                 | 46.19        | Zaid / Flood                   | 10.99        |
| Maize     | Zaid / Drip                     | 39.96        | Rabi / Drip                    | 3.86         |
| Potato    | Kharif / Drip                   | 31.47        | Zaid / Drip                    | 18.13        |
| Rice      | Kharif / Flood                  | 35.01        | Kharif / Drip                  | 4.23         |
| Soybean   | Rabi / Drip                     | 44.93        | Kharif / Drip                  | 17.25        |
| Sugarcane | Zaid / Sprinkler                | 32.24        | Kharif / Flood                 | 20.76        |
| Tomato    | Rabi / Flood                    | 48.02        | Rabi / Drip                    | 12.92        |
| Wheat     | Zaid / Manual                   | 36.90        | Zaid / Drip                    | 5.44         |

**Insights:**

- Drip irrigation is versatile, giving both high and low yields.

- Flood irrigation is less efficient for some crops.

- Season matters: Zaid and Rabi often yield more, but depends on irrigation.
  
**6. Pesticide Used per Season**
| Crop Type | Highest Pesticide Season | Pesticide Used (kg) | Lowest Pesticide Season | Pesticide Used (kg) |
| --------- | ------------------------ | ------------------- | ----------------------- | ------------------- |
| Barley    | Kharif                   | 2.21                | Zaid                    | 1.56                |
| Carrot    | Rabi                     | 2.94                | Zaid                    | 0.81                |
| Cotton    | Kharif                   | 3.49                | Rabi                    | 0.91                |
| Maize     | Rabi                     | 2.85                | Zaid                    | 1.31                |
| Potato    | Kharif                   | 2.68                | Zaid                    | 2.25                |
| Rice      | Rabi                     | 3.45                | Zaid                    | 1.77                |
| Soybean   | Zaid                     | 2.89                | Rabi                    | 2.45                |
| Sugarcane | Kharif                   | 1.66                | Zaid                    | 1.42                |
| Tomato    | Zaid                     | 4.42                | Kharif                  | 0.66                |
| Wheat     | Rabi                     | 3.03                | Zaid                    | 2.81                |

**Insights:**

- Kharif and Rabi seasons generally require more pesticide.

- Zaid season often requires less pesticide due to lower pest pressure.

- Crop-specific patterns indicate targeted pest management can save costs.




##  Yield by Soil Type

| Crop Type | Highest Yield Soil | Yield (tons) | Lowest Yield Soil | Yield (tons) |
| --------- | ------------------ | ------------ | ----------------- | ------------ |
| Barley    | Loamy              | 46.47        | Sandy             | 17.44        |
| Carrot    | Loamy              | 47.70        | Clay              | 27.95        |
| Cotton    | Sandy              | 28.82        | Loamy             | 13.48        |
| Maize     | Sandy              | 39.96        | Peaty             | 3.86         |
| Potato    | Sandy              | 31.47        | Silty             | 20.53        |
| Rice      | Clay               | 33.66        | Silty             | 4.23         |
| Soybean   | Loamy              | 40.15        | Sandy             | 28.98        |
| Sugarcane | Loamy              | 38.18        | Clay              | 17.19        |
| Tomato    | Clay               | 43.28        | Loamy             | 12.92        |
| Wheat     | Silty              | 36.90        | Clay              | 18.07        |

**Insights:**

* Loamy soil supports higher yields but requires more inputs.
* Sandy and Peaty soils require careful water and fertilizer management.
* Clay soil provides moderate yields and resource usage.

---

##  Yield, Fertilizer, Pesticide, and Water Usage by Season

**Observations:**

* **Kharif:** High yields and high resource usage (fertilizer, water, pesticide).
* **Rabi:** Moderate yields and moderate resource usage.
* **Zaid:** Lower yields and lower inputs; short-duration crops.

---

## Yield, Fertilizer, Pesticide, and Water Usage by Irrigation Type

**Observations:**

* **Drip Irrigation:** High yields with moderate inputs → efficient and sustainable.
* **Flood Irrigation:** High yields but high water and fertilizer usage → less efficient.
* **Sprinkler & Manual:** Moderate yields and inputs.
* **Rain-fed:** Lowest yields and inputs, traditional farming.

---

## Crop Yield and Resource Usage by Crop and Season

**Observations:**

* Kharif season: High yields for Rice, Cotton, Maize; high inputs.
* Rabi season: Moderate yields for Wheat, Barley; moderate inputs.
* Zaid season: Short season with generally lower yields and inputs, except for some vegetables.
* Crop-specific trends:

  * Rice & Cotton: High yields and resource demands during Kharif.
  * Wheat & Barley: Stable yields in Rabi.
  * Vegetables: Moderate yields and targeted input usage, adaptable across Rabi and Zaid.

---

##  Pair Plot Observations

* Positive correlation between Yield and Water/Fertilizer usage.
* Fertilizer and Pesticide show moderate positive correlation.
* Farm area impacts total production but not yield per unit area.

---

##  Distribution Insights by Soil Type

* **Loamy:** High productivity; high water, fertilizer, pesticide usage.
* **Sandy:** Requires careful water management; moderate inputs.
* **Clay:** Moderate-to-high productivity; balanced inputs.
* **Peaty:** Lower inputs and yields; naturally fertile.

---

##  Distribution Insights by Season

* Kharif: High resource usage and yield; pest and disease risk higher.
* Rabi: Balanced inputs and moderate productivity.
* Zaid: Low inputs and yields; less intensive crops.

---

## Conclusion

The analysis highlights how **soil type, season, and irrigation method** significantly affect crop yield and resource usage. Insights can help optimize farm management:

* Prioritize drip irrigation for efficiency.
* Adjust fertilizer and pesticide based on soil and season.
* Plan crops according to seasonal strengths and soil suitability.
  

## Soil Type Insights:

-**Loamy Soil:** Supports higher productivity with a broad range of fertilizer, pesticide, and water usage, reflecting intensive management to maximize yields.

-**Sandy Soil:** Requires careful input management, especially for water, due to quick drainage. Yields are moderate and input use is controlled.

-**Clay Soil:** Offers moderate-to-high productivity with balanced inputs, benefiting from its water and nutrient retention.

-**Peaty Soil:** Lower input usage and yields, reflecting natural fertility but limited productivity.

-**Silty Soil:** Shows consistent water retention and moderate input requirements, generally favoring stable yields.

## Seasonal Insights:

-**Kharif Season:** High inputs (fertilizer, water, pesticide) and high yields due to favorable monsoon conditions, but also higher pest risks.

-**Rabi Season:** Moderate inputs and stable productivity, benefiting from controlled irrigation and predictable conditions.

-**Zaid Season:** Lower inputs and yields; shorter season with less pest pressure and water needs, suitable for quick-growing crops.

## Irrigation Insights:

-**Drip Irrigation:** High efficiency, strong yields, moderate fertilizer and water usage.

-**Flood Irrigation:** High yields but very high water and fertilizer usage; can be inefficient and environmentally taxing.

-**Sprinkler Irrigation:** Moderate efficiency; pesticide usage may be slightly higher due to favorable pest conditions.

-**Manual and Rain-fed Irrigation:** Lower input usage overall, reflecting traditional practices but often lower yields.

## Crop-Specific Insights:

-**High-Yield Crops:** Carrot and Tomato show the strongest positive correlations with yield.

-**Rice and Cotton:** High yields and high resource demands, particularly in Kharif season.

-**Wheat and Barley:** Moderate yields during Rabi season; stable and predictable growth.

-**Vegetables (e.g., Tomato, Carrot):** Require targeted fertilizer and pesticide applications; can yield well in Rabi and Zaid seasons.

-**Potato:** Requires higher fertilizer inputs.

-**Cotton:** Lower average yield; negative correlation with yield observed.

## Input and Resource Insights:

-**Fertilizer Usage:** Weakly correlates with yield; its effectiveness depends on crop type and irrigation.

-**Water Usage:** Positive correlation with yield; crops need sufficient water for maximum productivity.

-**Pesticide Usage:** High use may negatively affect yield; season and crop-specific patterns are crucial.

-**Farm Size:** Larger farms show a weak positive correlation with yield; input usage does not scale linearly, indicating efficiency practices.

## General Observations:

-Loamy soil and Kharif season generally favor high yields.

-Manual and rain-fed irrigation positively influence yield, while flood irrigation may reduce efficiency.

-Input management should be crop-, soil-, and season-specific to optimize yields while minimizing costs and environmental impact.
