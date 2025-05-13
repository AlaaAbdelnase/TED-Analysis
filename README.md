TED-Analysis
Cracking the YouTube Code:  What Makes a TED Talk Go Viral?

📥 Step 1: Pulling TED Data Using the YouTube API
Using the YouTube Data API, I extracted:
Video title, Description, Publish date, Category, Duration, View count, Like count, Comment count 

🧹 Step 2: Data Cleaning
I converted YouTube ISO 8601 durations into a human-readable format and removed rows with missing or inconsistent metadata.
Key preprocessing steps:
Convert publish date → year/month features
Convert duration to total minutes
Drop or fill missing values
Encode video categories



🧠 Step 3: Training and Testing a Regression Model
Using scikit-learn, I trained a regression model to predict view counts using the following features:
Duration, Category (encoded), Publish month/year

Models tested:
Linear Regression, Random Forest Regressor, Gradient Boosting

<img src="imgs/test.png" alt="test" width="600"/>

📈 Step 4: Visualizing Results in Power BI
To understand trends and outliers, I exported the data to Power BI to create a dynamic dashboard:

Views by Category,
Most Popular Months,
Trend of TED views over time,
The most viewed month for each category

<img src="imgs/dashboard.png" alt="dashboard" width="600"/>




