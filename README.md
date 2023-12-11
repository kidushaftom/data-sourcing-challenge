Movie Review Data Collection and Analysis
This repository contains a Python script for collecting and analyzing movie reviews from The New York Times API and movie details from The Movie Database API. The collected data is then merged, cleaned, and exported for further analysis.

Setup
1. Import Required Libraries and Set Up Environment Variables
Ensure you have the necessary dependencies installed by running the following command:

bash
Copy code
pip install requests pandas python-dotenv
The script uses the dotenv library to load environment variables from a .env file. Make sure to create a .env file in the root directory with the following content:

plaintext
Copy code
NYT_API_KEY=your_nyt_api_key
TMDB_API_KEY=your_tmdb_api_key
Replace your_nyt_api_key and your_tmdb_api_key with your actual API keys.

2. Access the New York Times API
The script accesses the New York Times API to retrieve movie reviews. It filters for reviews with "love" in the headline, related to movies, and within a specified date range.

3. Access The Movie Database API
The Movie Database API is used to obtain additional details about the movies mentioned in the reviews. The script queries the API with movie titles obtained from the New York Times reviews.

Execution
Execute the Jupyter Notebook cells in order to run the script. The script will make API requests to both The New York Times and The Movie Database, so be mindful of API rate limits.

Output
The final merged and cleaned dataset is exported to a CSV file named moview_review.csv in the output directory.

Note
Ensure your API keys are kept confidential and not shared publicly.
The script includes sleep intervals between API requests to avoid rate-limiting issues.
Review the code comments for detailed explanations of each step.
Feel free to customize the script based on your specific requirements or use it as a starting point for movie-related data analysis.