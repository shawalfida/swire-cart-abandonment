# **Swire Cart Abandonment Prediction**

This repo contains my individual analytics work for the Swire Coca-Cola case study. It includes exploratory data analysis (EDA), feature engineering, and modeling designed to predict cart abandonment early in the order window so Swire can intervene and recover revenue.

---

## **1. Business Problem and Objective**

Swire loses revenue when customers start building a cart but do not complete the purchase before the order window closes.
The goal of this project is to:

**Predict whether a customer will abandon their cart within the first 30% of the order window**, giving Swire time to send a reminder (email/text) and recover the order before the window closes.

---

## **2. Group Solution Overview**

As a team, we worked with GA event logs and ordering data to:

* Analyze abandonment patterns across customer types, fulfillment modes, and shipping conditions
* Engineer early-window behavioral features from GA events
* Build classification models focused on **recall**, since the objective is to identify as many risky carts as possible
* Avoid data leakage by restricting all model features to the first 30% of the order window
* Develop a simple intervention strategy where predicted high-risk carts receive a reminder to complete their order

This solution enables Swire to act proactively rather than after revenue has already been lost.

---

## **3. My Contribution**

I led three main parts of the project:

### **A. Visualizations**

I created the key charts used to explain:

* Abandonment rates by segment (restaurants, stores, hotels)
* Drop-off patterns across distribution modes
* Event behavior leading up to abandonment
* Financial impact of different recovery scenarios

### **B. Intervention Strategy**

I proposed the 30%-window intervention framework, including:

* Early identification of likely abandoned carts
* Simple reminders (email/text) to nudge customers before cutoff
* Benchmark recovery targets (5%, 10%, 15%) and their revenue implications
* Future use of customer clustering for more targeted outreach

### **C. Modeling**

My modeling work included:

* Cleaning and preparing GA event sequences
* Handling inconsistencies, duplicates, and missing events
* Preventing data leakage by filtering post-cutoff activities
* Training models with a recall-first approach
* Testing different probability thresholds and visualizing their impact

---

## **4. Business Value**

This approach gives Swire:

* A predictive signal before abandonment occurs
* A low-cost intervention method that can recover meaningful revenue
* Better support for high-risk or high-value customers
* Insight into which customer behaviors signal drop-off
* A framework for ongoing operational decision-making

Even small improvements in recovery (5–15%) produce significant financial gains.

---

## **5. Challenges Encountered**

During the project, we faced several data and modeling challenges:

* **GA event inconsistencies** across customers
* **Missing or duplicated events** in the raw logs
* **Confusion around order window timing** and how GA events map to it
* **Data leakage risks** when late-window events revealed the outcome
* **Irregular event sequences** requiring custom preprocessing

These issues required careful cleaning, validation, and redesign of feature logic.

---

## **6. What I Learned**

This project strengthened my skills in:

* Working with messy event-level behavioral data
* Detecting and preventing data leakage in time-based prediction tasks
* Building visual explanations for executive and operational audiences
* Prioritizing model metrics that align with business goals (recall vs accuracy)
* Designing a predictive workflow that integrates with real operational processes

