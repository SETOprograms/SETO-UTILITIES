![SETO Logo](http://s32.postimg.org/5jkdakmbp/festisite_google.png "SETO Utilities V1.0.0")
# SETO Utilities V1.0.0
To begin using SETO Utilities, make sure you import it using the statement:
```vb
Imports SETO
```
### SETO.Speech
##### SETO.Speech.Speak()
Usage:
```vb
Speech.Speak(text) As Boolean
```
Definition: The text will be spoken by the computer. A boolean output is also given, to indicate whether the task was successful

Example:
```vb
Speech.Speak("Hello World")
' The computer will now say "Hello World", and True is returned
```
### SETO.API
##### SETO.API.Tools.GetTextFromUrl()
Usage:
```vb
API.Tools.GetTextFromUrl(url) As String
API.Tools.GetTextFromUrl(url,readline) As String
```
Definition: Text will be returned from a given URL. If the ```readline``` property is True then only the first line will be read, otherwise the whole document will be read.
##### SETO.API.Google.Maps.FindCoordinates()
Usage:
```vb
API.Google.Maps.FindCoordinates(address) As String
API.Google.Maps.FindCoordinates(address,showlatitude,showlongitude) As String
```
Definition: The latitude and longitude of a given address will be returned, using Google maps. If either of the ```showlatitude``` or ```showlongitude``` are false, that corresponding value will not be returned. By default, data is returned in the format "latitude,longitude". Address can be given in any format.

Example:
```vb
API.Google.Maps.FindCoordinates("12 Downing Street, London")
' Returns "51.5033767,-0.1280607"
API.Google.Maps.FindCoordinates("12 Downing Street, London", False, True)
' Returns "-0.1280607"
API.Google.Maps.FindCoordinates("12 Downing Street, London", False, False)
'Returns "0,0"
```
##### SETO.API.Google.Maps.GetFullAddress()
Usage:
```vb
API.Google.Maps.GetFullAddress(address) As String
```
Definition: The full, formatted address will be returned when a partial address is entered

Example:
```vb
API.Google.Maps.GetFullAddress("12 Downing Street, London")
' Returns "12 Downing St, Westminster, London SW1A, UK"
```
##### SETO.API.Bitly.Shorten()
Usage:
```vb
API.Bitly.Shorten(url) As String
```
Before using this function, please set the ```SETO.API.Keys.Bitly``` property to your own Bitly API key

Definition: A long url will be shortened and the short url will be returned

Example:
```vb
API.Keys.Bitly = "YOUR-KEY-HERE"
API.Bitly.Shorten("http://seto.pcriot.com")
' Returns "http://bit.ly/2hTCraC"
```

