# AI-ML-Hostel-Mess-Food-Analysis
A python code written inorder to conduct an analysis on a dataset. It is meant to analyse the satisfaction of students with hotel mess food and represent it in easy-to-understand graphical representation like graphs and tables. 
 Explanation of the Python Code:-
 
 
 The program begins by importing the required Python libraries. pandas is used for loading and manipulating the dataset, numpy helps with numerical operations, and matplotlib.pyplot is used to create graphs and visualizations. The display function from IPython.display is imported to neatly show tables inside Google Colab. These libraries together allow the program to clean, analyze, and visualize feedback data effectively.

Next, the code uploads a CSV file using Google Colab’s files.upload() function. This allows the user to manually upload the dataset named mess_feedback_10000_with_dates.csv. Once uploaded, the file is read into a pandas DataFrame using pd.read_csv(). The first five rows of the dataset are displayed using df.head() so that the user can quickly understand the structure of the data and verify that it has loaded correctly.

After loading the data, the program performs data inspection to identify missing values. The df.isnull().sum() command checks each column and counts how many missing values are present. This step is important because missing data can affect calculations and visualizations if not handled properly.

In the data cleaning section, duplicate rows are removed using df.drop_duplicates() to ensure that repeated feedback entries do not bias the results. Missing numeric values are then filled using the mean (average) of their respective columns with df.fillna(). The code also ensures that all rating values remain within a valid range of 1 to 5 by using the clip() function. These ratings are converted to integers to maintain consistency in the dataset.

The statistical summary section uses the describe() function to generate key statistics such as count, mean, minimum, maximum, and standard deviation for each rating column. This provides an overall understanding of how students rated different aspects of the mess, such as food quality and cleanliness.

Next, the code calculates the average satisfaction score for each feedback category using the mean() function. These average scores are displayed and then visualized using a bar graph. The bar chart clearly compares different feedback parameters and shows which aspects received higher or lower ratings.

The program then analyzes how overall satisfaction changes over time. The Date column is converted into a datetime format so it can be used for time-based analysis. Monthly average ratings are calculated using the resample() function, and a line graph is created to show trends in overall satisfaction across months. This helps identify improvements or declines in feedback over time.

A histogram is also created by grouping feedback data into monthly time bins. This visualization shows how overall ratings are distributed over time, providing insight into periods with higher or lower satisfaction levels.

Finally, a box plot is generated for all rating categories. The box plot shows the distribution, spread, and variability of ratings, including median values and potential outliers. This helps compare consistency across different feedback parameters and understand how varied student opinions are.
