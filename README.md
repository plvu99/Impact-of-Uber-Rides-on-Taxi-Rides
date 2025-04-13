# 🚕 Impact of Uber Rides on Taxi Rides

## 🧠 Problem Statement

As ride-sharing services like Uber expand, it’s important to understand how they impact traditional transportation methods such as Yellow and Green taxis. Specifically, I aim to analyze the **elasticity of taxi demand with respect to Uber rides**—whether Uber acts as a substitute or complement to cab services in New York City.

Understanding this relationship is critical for policymakers, transportation planners, and ride-hailing platforms to assess how rider behavior shifts based on available alternatives.

## 🎯 Objective

_**1. Does an increase in Uber rides impact the number of taxi rides (Yellow + Green Cabs)?**_

_**2. Can Uber ride volume reliably predict taxi ride volume, even after controlling for external factors?**_

The project analyzes over **20 million records** drawn from **four distinct datasets**: Green Cab trips, Yellow Cab trips, Uber pickups, and daily precipitation data in June 2015. [Link](https://drive.google.com/drive/folders/1M_XjVQcMo5mZ2diriFbUzLNK6QD4A6dT?usp=sharing)

**June** typically sees higher ride volumes due to warmer weather and tourism, making it ideal for analyzing demand.

**NYC** is one of the largest and busiest urban transportation hubs in the U.S., with a high volume of both taxi and ride-share activity. **Manhattan**, the core service zone for both Uber and Yellow Cabs, has the highest ride volume, while Green Cabs restrictions from picking up passengers in much of Manhattan allows for clear comparisons across service types.

People may opt for rides over walking, biking, or public transport when it rains. Unlike other factors like fare changes or policy shifts, **precipitation** varies daily and can help capture transient changes in demand. It may explain spikes in both Uber and taxi demand, so controlling for it helps isolate the true relationship between Uber and taxi usage.

## 💡 Proposed Solution

**1. Data Processing**

- Filter taxi and Uber trip data for Manhattan in June 2015.
  
- Filter daily precipitation data for Manhattan in June 2015.
  
- Standardize and aggregate the data by date and location.

**2. Descriptive Analysis**

- Compare total and average daily trips across Green Cabs, Yellow Cabs, and Uber.

- Analyze trip patterns by day of the week.

**3. Regression Modeling**

- **Model 1:** Predict total taxi rides using Uber rides only.

- **Model 2:** Add precipitation as a control variable to assess its effect.

## 📊 Key Findings

**1. Total and Average Daily Trips in Manhattan**

| Service     | Total Trips | Average Daily Trips |
|-------------|-------------|---------------------|
| Yellow Cab  | 11.2M       | ~372,000            |
| Uber        | 2.0M        | ~66,000             |
| Green Cab   | 0.46M       | ~15,000             |

**Yellow Cabs** dominate in volume, but **Uber** shows significant market penetration. **Green Cabs** have the lowest presence in Manhattan, as expected given their service zone restrictions.

**2. Weekly Patterns**

**Uber and Yellow Cab rides** peak on **Tuesdays** and fall off on **Sundays**, suggesting strong weekday commuter usage. **Green Cabs** follow a similar but lower-volume trend.

**3. Regression Results**

**Model 1** (without controlling for precipitation) estimates that each additional Uber ride is associated with a 4.07 increase in combined Yellow + Green Cab rides. This is highly significant (t = 67.56, p < 0.001). R² = 0.525, meaning about 52.5% of the variation in taxi rides is explained by Uber rides alone.

**Model 2** includes precipitation as a second predictor. The coefficient on Uber rides drops slightly to 3.99, still significant (p < 0.001). Precipitation’s coefficient = 0.126, with p ≈ 0.062, which is marginally insignificant at the 5% level. The R² only increases from 0.525 to 0.526, suggesting that precipitation adds little explanatory power.

## 📌 Conclusion

Uber ride volume is a **strong predictor** of taxi demand in Manhattan, explaining over **52% of the variation** in daily taxi rides—even when accounting for weather. This supports the hypothesis that ride-sharing and taxis may respond to common demand patterns (e.g., commuting), rather than acting purely as substitutes or competitors.
