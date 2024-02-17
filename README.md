# data-sourcing-challenge

# Goal of assignment 
The overall objective of this assigment is to generate a csv file which will aide in search effeciency for movies. This will be accomplished by extracting the information from the NYT and TMDB API's. 

# Extracting the NYT Information 
1. NYT API key must be accessed from its online data base with a registered key. However we are not just taking all information without first specifying what is needed. A filter query specifying movie reviews with love in their headline along with field list grabbing headline, url, snippets and other parts of the data are specified. All of the data wanted is between 2013 and 2023, so this information is specified aswell. After this a get request is made and json dumps is executed in order to visualize the data gathered aswell as open up its accesibalilty for cleaning.

2. The second portion of this program involves checking the data colected compared to the data desired and storing it in a list which being more user friendly will allow more effeciency when working. The program combs through 19 pages of data to find the selected filter query and returns whether the page has the desired information or does not and returns a statement on the info found. At this point the information is json dumped and normalized.

3. The last portion is making the data more readable which involves taking the data from the dataframe created and removing unwanted information in the "headline.main" column. After this a the keyword column is converted to a string from a list by creating a function to handle the action. The last part of this section is to create a list of titles from the previously created titles column for later use.


# Extracting the TMDB information
1. First the TMDB key must be accessed so we can pull the correct information. Luckily we already have been given the url format along with the TMDB API string. The ultimate goal of this program is to alert the user to if the title of the book was found and then create a dictionary to pull information from later. After this has been accolmplished the infomration is dumped and then normalized into a dataframe for further use. 

2. Second the data is merged with the NYT movie data aquired in the previous section. This dataframe gives us a more complete view of the desired movies and allows all information to be taken into account. From here the information is cleaned taking out all the undersirable characters and dropping duplicates. 

3. Finally all the work is compiled into a csv for all those who wish to view said movies.