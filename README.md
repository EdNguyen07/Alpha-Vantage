Prerequisites:
1. Alpha Vantage API Key: You'll need to sign up for an API key from Alpha Vantage.
Salesforce Setup: Ensure you have permission to make HTTP callouts from Salesforce and that the necessary remote site settings are configured to allow calls to the Alpha Vantage API.
Steps:
Set Up Remote Site Settings in Salesforce:
Go to Setup in Salesforce.
Search for Remote Site Settings.
Click New Remote Site and enter a name and the Alpha Vantage base URL (https://www.alphavantage.co), then save it.
2. Create Apex Code for Real-Time and Historical Data
3.Explanation:
API_KEY: Replace 'YOUR_ALPHA_VANTAGE_API_KEY' with your actual Alpha Vantage API key.
BASE_URL: The base URL for Alpha Vantage API endpoints.
getRealTimeData(String symbol): This method constructs the URL for the real-time data API call and uses the makeApiCall helper method to send the request.
getHistoricalData(String symbol, String interval): This method constructs the URL for historical data API calls, where interval can be a value like TIME_SERIES_DAILY or TIME_SERIES_INTRADAY.
makeApiCall(String endpoint): This helper method sends an HTTP GET request to the provided endpoint and returns the response body.
Notes:
Make sure to handle the returned data (which will be in JSON format) appropriately. You might want to parse this data and use it within your Salesforce application.
The example assumes you are familiar with Salesforce's HttpRequest, Http, and HttpResponse classes.
Feel free to modify the code to better fit your needs or handle specific API endpoints and parameters.
