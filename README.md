# Pymaceuticals_Medication_Analysis

 it's crucial to understand the number of mice involved as they serve as subjects for experimentation. Two methods have been proposed to calculate the total count of mice, providing insights into the dataset's scale and ensuring accuracy in subsequent analyses.

Option 1 utilizes the value_counts() function to tally the occurrences of each unique mouse ID within the 'Mouse ID' column of the merged_studies dataset. This approach yields a comprehensive count of individual mouse IDs, providing a detailed breakdown of the dataset's composition.

Alternatively, Option 2 employs the nunique() function directly on the 'Mouse ID' column. This method efficiently determines the number of unique mouse IDs present in the dataset without the need for tallying occurrences. It offers a straightforward approach to obtaining the total count of mice involved in the study.

Both options aim to achieve the same objective of quantifying the total number of mice in the study. However, Option 2 presents a more streamlined and direct method for obtaining this information, offering a concise count of unique mouse IDs.

The analysis reveals that there are [mice_count] mice recorded in the merged studies dataset, ensuring clarity and accuracy in subsequent analyses and interpretations.

To maintain data integrity and ensure accurate analysis, it's imperative to identify and address any duplicate entries within our dataset. The data is uniquely identified by Mouse ID and Timepoint, where each combination should represent a distinct observation.

Firstly, I have identified duplicates by querying the merged_studies dataset based on the 'Mouse ID' and 'Timepoint' columns. Any rows with identical 'Mouse ID' and 'Timepoint' values are considered duplicates. This allows us to capture instances where the same mouse is recorded at the same timepoint multiple times.

Next, I isolated the unique Mouse IDs associated with these duplicate entries. By doing so, we can pinpoint the specific mice for which duplicate observations exist. This step facilitates further investigation and remediation of the duplicate entries.

The identification of duplicate entries ensures data consistency and reliability in subsequent analyses. Addressing these duplicates is crucial for accurate interpretation and drawing meaningful conclusions from the dataset.

I aimed to analyze the tumor volume across different drug regimens by generating a comprehensive summary statistics table. To achieve this, I utilized the powerful capabilities of Pandas' groupby function along with summary statistical methods.

The summary statistics table provides valuable insights into the distribution of tumor volumes for each drug regimen, allowing for a thorough comparison of their efficacy. 

In the bar chart, I aimed to visualize the distribution of the total number of rows (representing Mouse ID/Timepoints) for each drug regimen using both Pandas and Matplotlib's pyplot library.

Using Pandas, I first grouped the data by drug regimen and calculated the count of Mouse ID within each group to determine the total number of rows. This information was then sorted in descending order to facilitate better visualization.

The resulting bar plot generated using Pandas showcases the total number of rows for each drug regimen, with drug regimens represented along the x-axis and the corresponding number of rows on the y-axis. The visualization provides a clear comparison of the distribution of rows across different drug regimens, aiding in understanding the dataset's composition.

Followed, replicated the same visualization using Matplotlib's pyplot library, sorting the data and created a bar plot, this time using the plt.bar() function. The resulting plot is similar to the one generated using Pandas, displaying the total number of rows for each drug regimen in a visually appealing manner.

Overall, these visualizations allow for quick and easy comparison of the total number of rows across different drug regimens, enabling researchers to identify patterns or discrepancies in the data and make informed decisions based on the findings.

For the quartiles, I nvestigated the tumor volume data across four specific treatment regimens: Capomulin, Ramicane, Infubinol, and Ceftamin. The goal was to calculate the interquartile range (IQR) and identify any potential outliers within each regimen.

To accomplish this, I have iterated through each treatment regimen using a for loop, extracting the tumor volume data and performing calculations to determine the IQR and detect outliers.

For each regimen,  calculated the lower quartile, upper quartile, median, and IQR of the tumor volume distribution. The IQR, which represents the range of the middle 50% of the data, provides insights into the spread of tumor volumes within each regimen.

I also computed the lower and upper bounds to identify potential outliers. Any data points falling below the lower bound or above the upper bound were considered potential outliers and flagged for further investigation.

The analysis revealed valuable insights into the distribution of tumor volumes for each treatment regimen. By identifying potential outliers, gaining a better understanding of the variability and consistency of treatment outcomes within each regimen, aiding in decision-making and further analysis of the dataset.

Overall, this thorough examination of tumor volume data across different treatment regimens provides researchers with critical information to assess treatment efficacy and guide future research efforts.

Finally for the correlation between scatter plot and data, I first calculated the correlation coefficient between mouse weight and average tumor volume. The correlation coefficient indicates the strength and direction of the linear relationship between two variables. For the Capomulin regimen, I found a correlation coefficient of [correlation coefficient value], indicating a [positive/negative] correlation between mouse weight and average tumor volume.

To create the regression line, I constructed a linear regression to quantify the relationship between mouse weight and tumor volume. Our linear regression analysis yielded a regression equation of [linear regression equation], where 'y' represents the tumor volume and 'x' denotes the mouse weight. The slope of the regression line indicates the rate of change in tumor volume per unit change in mouse weight.

Finally, To visually represent the relationship between mouse weight and tumor volume, I created a scatter plot with mouse weight on the x-axis and average tumor volume on the y-axis. Additionally, we plotted the regression line on the scatter plot to illustrate the linear relationship between the variables. The plot clearly demonstrates the trend between mouse weight and tumor volume, with the regression line providing a visual representation of the predicted tumor volume based on mouse weight.

