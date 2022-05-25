# Investigating-Netflix-Movies-and-Guest-Stars-in-The-Office
Investigating Netflix Movies and Guest Stars in The Office
Use our friend's data to create a dictionary. To do so, you will need to perform the following steps: Create a list of years from 2011 to 2020 and a list durations of the average movie lengths our friend provided (103, 101, 99, 100, 100, 95, 95, 96, 93, and 90), create a dictionary movie_dict, with the keys "years" and "durations" and the values set to your lists years and durations and print and inspect the dictionary to ensure it was created correctly. View code [here](coding/create_dict)

The dictionary movie_dict looks like:

{'years': [2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019, 2020],
 'durations': [103, 101, 99, 100, 100, 95, 95, 96, 93, 90]}

2. Creating a DataFrame from a dictionary
To convert our dictionary movie_dict to a pandas DataFrame, we will first need to import the library under its usual alias. We'll also want to inspect our DataFrame to ensure it was created correctly. View code[here](coding/create_df):

![image](https://user-images.githubusercontent.com/53232113/170366165-66bbebff-fe09-48e7-8605-4108233a7b8a.png)

3. A visual inspection of our data
Alright, we now have a pandas DataFrame, the most common way to work with tabular data in Python. Now back to the task at hand. We want to follow up on our friend's assertion that movie lengths have been decreasing over time. A great place to start will be a visualization of the data.

Given that the data is continuous, a line plot would be a good choice, with the dates represented along the x-axis and the average length in minutes along the y-axis. This will allow us to easily spot any trends in movie durations. There are many ways to visualize data in Python, but matploblib.pyplot is one of the most common packages to do so. View code [here](coding/visual_inspection):

![image](https://user-images.githubusercontent.com/53232113/170365285-2e04f716-1148-410a-9de8-b970fce13c88.png)


