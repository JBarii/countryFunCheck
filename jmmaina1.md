# countryFunCheck
About:
A location application to search a country,get interesting areas in the country,distance from where you are and the current weather in those areas.The application uses voice commands to 
interrogate the data once the user has given the country.

The application has utilized the following public APIs:
1.CountryAPI to search for countries data
2.Google Maps to display the searched country on a map
3.API AI to enable voice based enquiry about weather and other interesting things about the searched country.

The application uses asynch calls in android to handle UI latency.
It also employs background threads when making calls to the various APIs.

To ensure the application can handle high IO,the application uses retrofit library to manage the network connectivity.
The local cache is maintained as a form of SQLlite to ensure queried data is stored locally for further query by user and for natural language processing.

Natural language processing is used in the app to ensure the user can use voice to ask for details about the country on the map.Details like weather,currency and many more.
