# Marketing Analysis

> Guided practice project (Nov–Dec 2024), built by following Ali Ahmad's YouTube tutorial. "ShopEasy" and the data are from the tutorial.

An end-to-end marketing analysis for an online shop, "ShopEasy", using SQL, Python and Power BI.

## The problem
ShopEasy's customer engagement and conversions were falling, even though it was spending more on marketing. The goal was to find out why, and what to change.

## KPIs
- Conversion rate: the share of website visitors who buy
- Engagement: clicks, likes and views on marketing content
- Average order value
- Customer feedback score: the average review rating

## What I did
- **SQL Server:** restored the database and wrote 5 cleaning queries. For example: removed duplicate customer journeys with `ROW_NUMBER()` in a CTE, filled missing durations with an average, joined customers to their location, fixed extra spaces in review text, split a combined "views-clicks" column, and grouped products into price bands with `CASE`.
- **Python:** scored the sentiment of every review with pandas and NLTK's VADER, combined it with the star rating, and saved the result (1,363 reviews).
- **Power BI:** built a calendar table and 4 pages: Overview, Conversion details (with a funnel), Social media details and Customer review details.

## What I found
- Conversion bounced back to 10.34% in December, after falling to 5.08% in October.
- January had the highest conversion (19.61%), helped by ski boots; May had the lowest (4.48%).
- Engagement held steady, with a 15.45% click-through rate, even though social media views fell.
- Views dropped from August onwards; blog posts got the most views, especially in March and May.
- Reviews were mostly positive (275 positive vs 82 negative), and most ratings were 4 stars (140) or 5 stars (135).

## Tools
SQL Server, SQL, Python (pandas, NLTK), Power BI, DAX.

## Files
- `customers.sql`, `products.sql`, `customer_journey.sql`, `customer_reviews.sql`, `engagement_data.sql`: the cleaning queries
- `customer_reviews_enrichment.py`: the sentiment script
- `customer_reviews_enrich.csv`: the reviews with their sentiment scores
- `Marketing Analysis Dashboard.pbix` and `.pdf`: the Power BI report
- `Calendar DAX query.txt`: the calendar table
- `MarketingAnalytics.bak`: the database backup
- short screen recordings of each page
