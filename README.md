# TripAdvisor Data Acquisition and Management

### Data Source
TripAdvisor website content.

### Methodology
- Downloads the page to the local file system, download the page of each available hotel in Los Angeles in TripAdvisor.
- Reads the saved file and parses the downloaded page and returns the data points: hotel name, vendors and prices, overall score, bubble rating of location, cleanliness, service, and value, hotel description, hotel star, number of room, number of reviews, and url of the hotel page for each hotel. Notice that the url of the hotel page comes from url of the 2nd page of review.
- Since each page in Tripadvisor only has 5 reviews, so we parse first 10 reviews of each hotel. For those have less than 10 reviews, we just parse 5 reviews which are displayed in the first page of that hotel.

### Database

![pic1](/TripAdvisorERD.png)

- Connect to SQL. Create a database and name it "tripadvisor". 
- Dump dataframe to tables in mysql database directly using sqlalchemy package.
