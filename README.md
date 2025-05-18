# Security-risk-assessment-tool
Here's a breakdown of the code:

#Data Preparation:

A dictionary data is created containing information for five companies: 'Alpha Corp', 'Coursera', 'Prodigy InfoTech', 'Delta Ltd', and 'CodSoft'.
The data includes 'Num Employees', 'Has Security Training (Yes=1,No=0)', 'IT Infrastructure Complexity (1-5)', 'Number of Past Incidents', and 'Data Sensitivity Level (1-5)'.
A pandas DataFrame df is created from this data.

#Risk Score Calculation:

A function calculate_Risk_score is defined to compute a risk score for each company based on the specified criteria and weights.
The weights are applied to 'Num Employees', 'Has Security Training', 'IT Infrastructure Complexity', 'Number of Past Incidents', and 'Data Sensitivity Level'.
The apply function is used on the DataFrame to calculate the 'Risk Score' for each row (company) and add it as a new column.

#Risk Category Assignment:

A function Risk_category is defined to categorize the calculated risk score into 'Low', 'Medium', or 'High' based on predefined thresholds (scores < 3 are Low, scores < 6 are Medium, and scores >= 6 are High).
This function is applied to the 'Risk Score' column to create a new column 'Risk_category'.

#Visualization:

A dictionary colors is defined to map each risk category to a specific color ('Low' to green, 'Medium' to orange, 'High' to red).
A bar chart is created using matplotlib.pyplot to visualize the 'Risk Score' for each company.
The bars are colored according to their assigned 'Risk_category' using the colors dictionary.
The chart is given a title, x-axis label ('Company'), and y-axis label ('Risk Score').
A legend is added to explain the color mapping for the risk categories.
The y-axis limit is set to start from 0 and extend slightly above the maximum risk score for better visualization.
plt.show() displays the generated plot.

#Display DataFrame:

The final DataFrame df, now including 'Risk Score' and 'Risk_category', is displayed using display(df).
