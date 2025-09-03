# Airbnb NYC 2023 – Exploratory Data Analysis

## Project Overview

This project analyzes the 2023 Airbnb dataset for New York City to understand market dynamics and provide actionable recommendations.  
The analysis covers neighborhood popularity, pricing trends, host activity, availability patterns, and guest reviews.  
The objective is to not only describe patterns but also deliver **data-driven, prescriptive insights** for travelers, hosts, and the Airbnb platform.

---

## Business Problem

Airbnb operates in a competitive short-term rental market where pricing, availability, and reviews directly impact customer experience and host revenue.  
This project addresses the following key questions:

1. Which neighborhoods and boroughs are the most popular and profitable for Airbnb rentals?  
2. How do prices and availability differ across neighborhoods and room types?  
3. What host and listing characteristics drive higher guest engagement and reviews?  
4. How can findings be translated into clear recommendations for stakeholders?  

---

## Dataset Description

The dataset consists of Airbnb listings in New York City for 2023.  
It contains approximately **42,930 records across 18 variables**, including:

- `neighbourhood_group`: The borough (Manhattan, Brooklyn, Queens, Bronx, Staten Island)  
- `neighbourhood`: Specific neighborhood name  
- `room_type`: Type of accommodation (Entire home/apt, Private room, Shared room, Hotel room)  
- `price`: Price per night in USD  
- `availability_365`: Number of days the listing is available in a year  
- `number_of_reviews`, `reviews_per_month`: Indicators of guest engagement  
- `host_id`, `host_name`: Host details  

Note: The `license` column was dropped as it contained null values for nearly all records. Outliers in `price` and `minimum_nights` were also treated to ensure reliable results.

---

## Methodology

The analysis followed a structured approach:

### 1. Data Cleaning
- Removed irrelevant and null-heavy columns (`license`).  
- Handled missing values in `reviews_per_month` and `last_review`.  
- Detected and treated extreme outliers in `price` and `minimum_nights`.  

### 2. Exploratory Data Analysis (EDA)
- Explored price distributions across boroughs and room types.  
- Analyzed availability and seasonal trends.  
- Investigated host activity, such as single vs. multiple listings.  
- Examined review frequency and its correlation with listing attributes.  

### 3. Statistical Testing
- Conducted **t-tests** to compare means across room types.  
- Applied **ANOVA** to assess differences across boroughs.  

### 4. Visualization
- Created barplots, scatterplots, and heatmaps to reveal neighborhood-level patterns.  
- Added descriptive titles and captions to ensure clarity for non-technical audiences.  

### 5. Results Interpretation
- Combined descriptive results with prescriptive recommendations tailored for travelers, hosts, and Airbnb.  

---

## Results and Insights

- **Neighborhoods:** Manhattan has the highest listing concentration but at premium prices. Brooklyn is more affordable and offers better availability.  
- **Pricing:** Most listings fall under $300 per night. Outliers inflate averages, making the median a more reliable measure.  
- **Availability:** Listings cluster at 0 days or 365 days, showing that some hosts either do not actively manage their calendars or treat listings as fully commercial operations.  
- **Hosts:** While most hosts manage only one property, a few professional hosts dominate the market with many listings.  
- **Reviews:** Consistently available and competitively priced listings attract more reviews, indicating higher guest trust and engagement.  

---

## Recommendations

### For Travelers
- Choose Brooklyn and Queens for affordable stays with strong availability.  
- Avoid listings that are overpriced or have no guest reviews.  

### For Hosts
- Manhattan hosts should emphasize quality and service to stand out in a saturated market.  
- Brooklyn hosts can leverage affordability while improving listing descriptions and ratings to attract more guests.  
- Regularly updating availability calendars improves visibility and reduces the risk of being flagged as inactive.  

### For Airbnb (Platform)
- Downrank or remove inactive or overpriced listings to maintain user trust.  
- Promote borough-specific “value for money” filters.  
- Incentivize guest reviews to improve transparency and market credibility.  

---

## Tech Stack

- Python: pandas, numpy, seaborn, matplotlib, scipy  
- Jupyter Notebook: analysis and visualization  
- Dataset: Airbnb NYC 2023 CSV  

---

