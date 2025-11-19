# SkillMinds AI Classes
🧩 Project Overview

SkillMinds AI is an AI-driven learning and upskilling platform designed to empower students, professionals, and organizations through personalized learning paths, AI mentorship, and certification-based career advancement.

The platform operates on a freemium-to-paid model, providing users free access to foundational courses and chatbot-based support, while offering paid access to advanced certifications, mentor sessions, and career dashboards.

This project analyzes user engagement behavior, satisfaction, and conversion patterns to uncover the key drivers that influence free-to-paid subscription transitions.

🎯 Project Objectives 

Analyze churn drivers among paid and free users.

Explore satisfaction patterns across user segments.

Simulate business recommendations to improve retention and monetization.

🧠 Key Business Questions

What is the overall conversion rate from free to paid users?

Which user segments (student, business, job seeker, etc.) show the highest engagement and growth?

How do AI chatbot interactions correlate with satisfaction and conversion?

What is the churn rate among different countries and plans?

How can the platform increase paid conversions and reduce churn?

💻 Dataset Description

A synthetic dataset of 50,000 user records was generated to simulate realistic EdTech behavior.

Feature	Description
user_id	Unique identifier for each user
user_segment	Category of learner (Student, Job Seeker, Developer, Business User, General User)
country	User’s country of access
subscription_type	Free / Paid
signup_date	Date of registration
churn_status	Whether user churned (Yes/No)
satisfaction_score	Average feedback score (1–10)
prompt_count	Number of chatbot interactions
course_completion_rate	Percentage of completed courses
duration_in_days	Duration of platform usage
conversion_flag	Indicates if user upgraded to paid plan
🧩 Tools & Technologies
Tool	Purpose
Power BI	Data modeling, DAX calculations, dashboard visualization
Python (Pandas, Matplotlib, Seaborn)	Data cleaning, EDA, feature exploration
Excel / CSV	Dataset generation and preprocessing
DAX	Time intelligence (YTD, YoY Growth), churn, conversion measures
📈 Key Metrics
Metric	Definition
Total Users	Total number of registered users
Paid Users	Users who upgraded to paid plans
Free Users	Users using freemium version
Churn Rate	% of users who discontinued usage
Conversion Rate	% of free users who converted to paid
Satisfaction Score	Average rating from feedback forms
YoY Growth %	Year-over-year user growth across countries
📊 Power BI Dashboard Highlights

Dashboard Name: SkillMinds AI – Churn & Conversion Analysis

Key Visuals:

Total users by subscription type

Churn rate by paid vs. free users

User segmentation by purpose (student, job seeker, etc.)

YoY growth % by country and plan

Churn rate by country

Prompt count by quarter (engagement analysis)

Drill-through by user segment & region

Filters:

Prompt Category

Country

🔍 Insights & Findings

User Distribution:
85% free users vs. 15% paid users, indicating a strong freemium base with conversion potential.

Churn Insights:
11.5% overall churn; slightly higher among free users, suggesting engagement drop-off post-trial.

Engagement Patterns:
Higher chatbot prompt activity correlates with increased satisfaction and conversion.

Segment Insights:
Students and business users show the highest engagement, while developers and job seekers have strong growth potential.

Geographic Insights:
India, Germany, and Canada exhibit strong YoY user growth (>900%), indicating markets worth scaling.

Satisfaction Analysis:
Average satisfaction of 7.1 across both free and paid users opportunity to enhance AI mentor quality.

💡Business Recommendations

Conversion Strategy: Introduce personalized discount offers for highly engaged free users.

Retention: Implement AI-driven reactivation prompts for inactive users.

Pricing Optimization: Introduce regional pricing and career bundles for students/job seekers.

Product Enhancement: Increase AI chatbot guidance in advanced courses to boost satisfaction.

Marketing Focus: Target high-growth countries (India, Germany, Canada) with localized campaigns.

🧮 Sample DAX Measures
Total Users = COUNT('User Data'[user_id])

Paid Users = CALCULATE(COUNT('User Data'[user_id]), 'User Data'[subscription_type] = "Paid")

Free Users = CALCULATE(COUNT('User Data'[user_id]), 'User Data'[subscription_type] = "Free")

Churn Rate = DIVIDE(
    CALCULATE(COUNT('User Data'[user_id]), 'User Data'[churn_status] = "Yes"),
    [Total Users]
)

Conversion Rate = DIVIDE(
    CALCULATE(COUNT('User Data'[user_id]), 'User Data'[conversion_flag] = "Yes"),
    CALCULATE(COUNT('User Data'[user_id]), 'User Data'[subscription_type] = "Free")
)

📈 Executive Summary

The SkillMinds AI Conversion Analysis explores the behavioral and engagement patterns of 50,000 simulated users to understand how a freemium learning platform can optimize its growth and monetization strategy.

Freemium to Premium Conversion Analysis (New Section)

## A major focus of this project was understanding how effectively free users transition into premium subscribers - a crucial KPI for any freemium-based EdTech product.

Here’s what the conversion analysis revealed:

🔹 1. High-intent users convert quickly, often within the first 7–10 days.
Users who explore multiple courses or interact with the AI mentor early on demonstrate significantly higher willingness to purchase. This suggests that onboarding and early value delivery play a critical role in driving upgrades.

🔹 2. Engagement depth is a stronger predictor of conversion than engagement frequency.
It’s not about how often users log in — it’s about how meaningfully they engage (course completion, assessments taken, mentor interactions). Shallow interactions rarely lead to upgrades.

🔹 3. Free users who complete at least one full module are 3–4× more likely to subscribe.
Completion creates a sense of momentum and increases trust in the platform’s quality. This makes “module completion nudges” a powerful conversion lever.

🔹 4. Price sensitivity varies strongly by user segment.
Students and job seekers respond better to lower-tier plans or flexible micro-credentials, while working professionals show higher readiness to pay for career-advancing certifications.

🔹 5. Certain geographies show naturally higher conversion rates.
Regions with higher digital learning adoption convert at above-average rates, suggesting scalable opportunities for localized and targeted premium offerings.

Key outcomes:

A 14.9% conversion rate from free to paid users highlights a strong engagement foundation.

11.5% churn rate suggests improving onboarding and engagement strategies could retain more users.

Satisfaction score of 7.12 across both free and paid users signals healthy but improvable user experience.

Geographic and segment analysis identifies India, Germany, and Canada as emerging user bases.

AI-driven personalization, targeted pricing, and user retention initiatives could significantly enhance revenue and user lifetime value.

The project demonstrates a complete analytics cycle from data preprocessing and visualization to business storytelling showcasing how data can guide strategic decisions in SaaS and EdTech environments.
