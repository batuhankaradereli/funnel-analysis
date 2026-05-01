Mobile App Conversion Funnel Analysis

This project analyzes how users move through a mobile app's conversion funnel — from install all the way to repeat purchase. The goal was to identify where users drop off and quantify the loss at each stage.

Tools Used
- Python & Pandas — data simulation and analysis
- Matplotlib & Seaborn — funnel and drop-off visualizations
- SQLite — querying funnel metrics
- Power BI — interactive dashboard page

The Funnel Stages
1. App Install
2. Registration
3. Onboarding
4. First Purchase
5. Repeat Purchase

Key Findings
- Only 7.5% of users who install the app make a repeat purchase
- The biggest drop-off happens between Onboarding and First Purchase — 57% of onboarded users never buy
- Registration captures 65% of installs, which is a reasonable rate but leaves room for improvement
- Getting users past the first purchase is the biggest challenge — only 42% of first-time buyers return

SQL Query Used
```sql
SELECT 
    stage,
    users,
    conversion_rate,
    ROUND(100 - conversion_rate, 1) AS overall_drop_off
FROM funnel
ORDER BY users DESC
```

What I Learned
Funnel analysis is one of the most practical tools in a product analyst's toolkit. Even with simulated data, the process of identifying bottlenecks and quantifying drop-off rates is directly applicable to real mobile app analytics.