# countryFunCheck
About:
A location application to search a country,get interesting areas in the country,distance from where you are and the current weather in those areas.The application uses voice commands to 
interrogate the data once the user has given the country.

The application has utilized the following public APIs:
1.CountryAPI to search for countries data
2.Google Maps to display the searched country on a map
3.API AI and Wit API to enable voice based enquiry about weather and other interesting things about the searched country.

The application uses asynch calls in android to handle UI latency.
It also employs background threads when making calls to the various APIs.

To ensure the application can handle high IO,the application uses retrofit library to manage the network connectivity.
The local cache is maintained as a form of SQLlite to ensure queried data is stored locally for further query by user and for natural language processing.

Natural language processing is used in the app to ensure the user can use voice to ask for details about the country on the map.Details like weather,currency and many more.


Sample APIs usage:
1.Query Country info:
http://countryapi.gear.host/v1/Country/getCountries?pName=kenya

Reponse:
{"IsSuccess":true,"UserMessage":null,"TechnicalMessage":null,"TotalCount":1,"Response":[{"Name":"Kenya","Alpha2Code":"KE","Alpha3Code":"KEN","NativeName":"Kenya","Region":"Africa","SubRegion":"Eastern Africa","Latitude":"1","Longitude":"38","Area":580367,"NumericCode":404,"NativeLanguage":"swa","CurrencyCode":"KES","CurrencyName":"Kenyan shilling","CurrencySymbol":"Sh","Flag":"https://api.backendless.com/2F26DFBF-433C-51CC-FF56-830CEA93BF00/473FB5A9-D20E-8D3E-FF01-E93D9D780A00/files/CountryFlags/ken.svg","FlagPng":"https://api.backendless.com/2F26DFBF-433C-51CC-FF56-830CEA93BF00/473FB5A9-D20E-8D3E-FF01-E93D9D780A00/files/CountryFlagsPng/ken.png"}]}


The above data is the primary source of data that is used to display the map.
When a user uses voice to ask for more details about the country,we use the API AI to process the voice then return the data asked whether it is weather,flag,currency etc.