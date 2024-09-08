# Module 6 Challenge: python_api_challenge

# Part 1: WeatherPy

# Requirement 1: Create Plots to Showcase the Relationship Between Weather Variables and Latitude
	# Import dependencies and setup
	# Import the OpenWeatherMap API key
	# Import citipy to determine the cities based on latitude and longitude
	# Generate the Cities list by using the citipy Library
	# Create empty list for holding the latitude and longitude combinations
	# Create empty list for holding the cities names
	# Range of Latitudes and longitudes
	# Create a set of random lat and lng combinations
	# Print the city count to confirm sufficient count

	# Use the OpenWeatherMap API to retrieve weather data from the cities list generated in the started code
	# Set the API base URL
	# Define an empty list to fetch the weather data for each city
	# Print to logger
	# Create counters
	# Loop through all the cities in our list to fetch weather data
		# Group cities in sets of 50 for logging purposes
		# Create endpoint URL with each city
		# Log the url, record, and set numbers
		# Add 1 to the record count
		# Run an API request for each of the cities
			# Parse out latitude, longitude, max temp, humidity, cloudiness, wind speed, country, and date
			# Append the City information into city_data list
		# If an error is experienced, skip the city
		# Indicate that Data loading is complete
	# Convert the cities weather data into a Pandas Dataframe
	# Show record count
	# Display sample data
	# Export the City_data into a csv
	# Read and display saved data
 	# Create the Scatter Plots Requested
# Requirement 2: Compute Linear Regression for Each Relationship
	# Define a function to create linear regression plots
		# Perform linear regression
		# Calculate the regression line
		# Create equation of line string
		# Plot the scatter plot
		# Display the r-squared value
		# Show the plot
	# Create a Dataframe with the northern hemisphere data
	# Display sample data
	# Create a DataFrame with the southern hemisphere data
	# Display sample data
	# Temperature vs. Latitude Linear Regression plot
		# Linear regression on Northern Hemisphere
		# Linear regression on southern hemisphere
		# Discussion about the linear relationship: the linear regression shows that there is an inverse relationship between temperature and latitude in the Northern Hemisphere, where temperatures tend to decrease as latitude increases, moving away from the equator. In the Southern Hemisphere, a similar inverse relationship is observed, temperatures also decrease as latitude increases. The r-squared value indicates how well the data fits this linear model.
	# Humidity vs. Latitude Linear Regression Plot
		# Northern Hemisphere
		# Southern Hemisphere
		# Discussion about the linear relationship: The regression analysis shows a weak relationship between latitude and humidity. Similar to the Northern Hemisphere, the relationship between humidity and latitude also looks week. Humidity is influenced by a variety of factors, which may dilute the relationship.
	# Cloudiness vs. Latitude Linear Regression Plot
		# Northern Hemisphere
		# Southern Hemisphere
		# Discussion about the linear relationship: The 2 graphs suggest very week negative correlation between latitude and cloudiness, the slope indicates that latitude has a minimal impact on cloudiness, and other factors are likely more significant in determining cloud cover.
	# Wind Speed vs. Latitude Linear regression plot
		# Northern hemisphere
		# Southern hemisphere
		# Discussion about the linear relationship: The equation for northern Hemisphere indicates an extremely weak correlation between latitude and wind speed. The near-zero slope suggests that latitude has virtually no effect on wind speed, which is more likely determined by local geographic features and weather conditions. The southern hemisphere shows a slightly stronger but still weak negative correlation between latitude and wind speed, suggesting that as latitude increases, wind speed may decrease slightly, but the relationship looks very weak.

# Part 2: VacationPy

# Dependencies and Setup
# Import API key
# Load the CSV file created in part 1 into Pandas Dataframe
# Display sample data

# Step 1: Create a map that displays a point for every city in the city_data_df DataFrame. The size of the point should be the humidity in each city
	# Configure the map plot
	# Display the map
# Step 2: Narrow down the city_data_df DataFrame to find your ideal weather condition
	# Narrow down cities that fit criteria and drop any results with null values
	# Drop any rows with null values
#Step 3: Create a new DataFrame called hotel_df
	# Use the Pandas copy function to create Dataframe called hotel_df to store the city, country, coordinates, and humidity
	# Add an empty column, "Hotel Name" to the DataFrame to store the hotel found using the Geoapify API
	# Display sample data
# Step 4: For each city, use the Geoapify API to find the first hotel located within 10,000 metres of your coordinates.
	# Set parameters to search for a hotel
	# Print a message to follow up the hotel search
	# Iterate through the hotel_df DataFrame
		# Get latitude, longitude from the dataframe
		# Add filter and bias parameters with the current city's latitude and longitude to the params dictionary
		# Set base URL
		# Make an API request using the params dictionary
		# Convert the API response to JSON format
		# Grab the first hotel from the results and store the name in the hotel_df DataFrame
			# If no hotel is found, set the hotel name as "No hotel found"
		# Log the search results
	# Display sample data
# Step 5: Add the hotel name and the country as additional information in the hover message for each city in the map
	# Configure the map plot
	# Display the map

