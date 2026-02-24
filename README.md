🕵️‍♂️ Data Forensics: Pick 3 Pattern Analysis
Project Overview
I’ve always been a fan of how the lottery works—Pick 3 is my go-to. I decided to use technology to test out some theories and have some fun with the numbers. This project uses Python and Pandas to transform raw, messy lottery data into structured insights.
+1

Note: This project is for educational purposes only. It’s a study on how Python can handle "noisy" data and identify historical patterns.

🛠 The Toolkit

Language: Python 


Library: Pandas (The industry-standard toolbox for data manipulation) 


Platform: Google Colab 

🔍 The Investigation Process
1. Opening the Vault (Data Loading)
The investigation begins by importing Pandas and bridging the gap between local storage and the cloud. We transform raw text into a structured DataFrame (df) to take a sneak peek at the evidence.
+1


df = pd.read_csv('filename.csv') 

2. Removing the Noise
Not all data is a signal. I discarded irrelevant columns (the "red herrings") like GreenBall or DoubleDraw to focus purely on the core numbers.


df.drop(columns=columns_to_remove, axis=1, inplace=True) 

3. The Deep Clean (Data Standardization)
Messy input like "Error" strings or missing values (NaNs) are potholes that can crash calculation scripts.
+1


Standardization: Iterating through columns to force inconsistent decimals into clean integers.


Coercion: Forcing non-numeric garbage into a "Safe State" (NaN) so it doesn't break the system.
+1


Patching: Strategically filling voids with 0 to maintain structural integrity.

4. Row-Wise Sorting (The Magic Line)
In a "Box" win, 1-5-9 and 9-1-5 are the same result, but computers see them as different. I applied a Lambda function to sort numbers across the row to normalize the chaos.
+2


.apply(lambda row: sorted(row.values)) 

5. Frequency & Combinatorics

Frequency Analysis: Flattening the dataset using .stack() to count the total frequency of digits 0-9.
+1


Finding Pairs: Using itertools.combinations to uncover hidden correlations and identify which numbers appear together as "accomplices" most often.
+2

📂 Securing the Evidence
Once the data is cleaned and the patterns are obvious, the cycle is complete: Raw Data -> Clean -> Insight -> Saved Asset.


df.to_csv('cleaned_data.csv', index=False) 


Strategic Insight: Data is only powerful if you know the right questions to ask. Python allows us to see patterns the human eye would miss.
+1


Case Status: CLOSED
