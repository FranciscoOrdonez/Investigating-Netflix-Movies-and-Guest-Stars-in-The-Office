# Investigating-Netflix-Movies-and-Guest-Stars-in-The-Office
Investigating Netflix Movies and Guest Stars in The Office
Use our friend's data to create a dictionary. To do so, you will need to perform the following steps: Create a list of years from 2011 to 2020 and a list durations of the average movie lengths our friend provided (103, 101, 99, 100, 100, 95, 95, 96, 93, and 90), create a dictionary movie_dict, with the keys "years" and "durations" and the values set to your lists years and durations and print and inspect the dictionary to ensure it was created correctly. View code [here](coding/create_dict)

The dictionary movie_dict looks like:

{'years': [2011, 2012, 2013, 2014, 2015, 2016, 2017, 2018, 2019, 2020],
 'durations': [103, 101, 99, 100, 100, 95, 95, 96, 93, 90]}

2. Creating a DataFrame from a dictionary
To convert our dictionary movie_dict to a pandas DataFrame, we will first need to import the library under its usual alias. We'll also want to inspect our DataFrame to ensure it was created correctly. View code[here](coding/create_df):

