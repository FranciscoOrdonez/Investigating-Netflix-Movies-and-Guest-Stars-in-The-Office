# Investigating-Netflix-Movies-and-Guest-Stars-in-The-Office
This is a guided project from DataCamp with some changes


1. Use our friend's data to create a dictionary. To do so, you will need to perform the following steps: Create a list of years from 2011 to 2020 and a list durations of the average movie lengths our friend provided (103, 101, 99, 100, 100, 95, 95, 96, 93, and 90), create a dictionary movie_dict, with the keys "years" and "durations" and the values set to your lists years and durations and print and inspect the dictionary to ensure it was created correctly. View code [here](coding/create_dict)

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

4. Loading the rest of the data from a CSV
Well, it looks like there is something to the idea that movie lengths have decreased over the past ten years! But equipped only with our friend's aggregations, we're limited in the further explorations we can perform. There are a few questions about this trend that we are currently unable to answer, including:

What does this trend look like over a longer period of time?
Is this explainable by something like the genre of entertainment?
Upon asking our friend for the original CSV they used to perform their analyses, they gladly oblige and send it. We now have access to the CSV file, available at the path "datacamp/DATA/netflix_data.csv". Let's create another DataFrame, this time with all of the data. Given the length of our friend's data, printing the whole DataFrame is probably not a good idea, so we will inspect it by printing only the first five rows. View code [here](coding/load_csv):

 
![image](https://user-images.githubusercontent.com/53232113/170372373-43702ba6-a33c-48f2-a1cb-b0139e94578e.png)

5. Filtering for movies!
Okay, we have our data! Now we can dive in and start looking at movie lengths.

Or can we? Looking at the first five rows of our new DataFrame, we notice a column type. Scanning the column, it's clear there are also TV shows in the dataset! Moreover, the duration column we planned to use seems to represent different values depending on whether the row is a movie or a show (perhaps the number of minutes versus the number of seasons)?

Fortunately, a DataFrame allows us to filter data quickly, and we can select rows where type is Movie. While we're at it, we don't need information from all of the columns, so let's create a new DataFrame netflix_movies containing only title, country, genre, release_year, and duration. View code [here](coding/filter).

Let's put our data subsetting skills to work!

The result is:

![image](https://user-images.githubusercontent.com/53232113/170392974-4ac7cf7b-2c3f-4fa5-95e1-5f574778cbf9.png)

6. Creating a scatter plot
Okay, now we're getting somewhere. We've read in the raw data, selected rows of movies, and have limited our DataFrame to our columns of interest. Let's try visualizing the data again to inspect the data over a longer range of time.

This time, we are no longer working with aggregates but instead with individual movies. A line plot is no longer a good choice for our data, so let's try a scatter plot instead. We will again plot the year of release on the x-axis and the movie duration on the y-axis. View code [here](coding/scatter).

The plot:

![image](https://user-images.githubusercontent.com/53232113/170395324-42d17c86-979e-437e-bb9d-3979f10d08cf.png)


