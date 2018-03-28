# Data Format

```
Airline:                  Airline name	
Airline ID:               3-letter (ICAO) code of the airline
Source Airport:           Source airport name
Source Airport ID:        3-letter (ICAO) code of the airline
Destination Airport:      Destination airport name
Destination Airport ID:   3-letter (ICAO) code of the airline
```

# Sample Data
```
[
   {
       "airline": "American Airlines",
       "airlineId": "AAL",
       "sourceAirport": "LaGuardia",
       "sourceAirportId": "LGA",
       "destinationAirport": "San Francisco International Airport",
       "destinationAirportId": "SFO"
   },
   {
       "airline": "JetBlue Airlines",
       "airlineId": "JBU",
       "sourceAirport": "LaGuardia",
       "sourceAirportId": "LGA",
       "destinationAirport": "San Francisco International Airport",
       "destinationAirportId": "SFO"
   },
   {
       "airline": "American Airlines",
       "airlineId": "AAL",
       "sourceAirport": "LaGuardia",
       "sourceAirportId": "LGA",
       "destinationAirport": "Philadelphia International Airport",
       "destinationAirportId": "PHL"
   },
   {
       "airline": "JetBlue Airlines",
       "airlineId": "JBU",
       "sourceAirport": "Philadelphia",
       "sourceAirportId": "PHL",
       "destinationAirport": "Sky Harbor International Airport",
       "destinationAirportId": "PHX"
   },
   {
       "airline": "American Airlines",
       "airlineId": "AAL",
       "sourceAirport": "Sky Harbor International Airport",
       "sourceAirportId": "PHX",
       "destinationAirport": "San Francisco International Airport",
       "destinationAirportId": "SFO"
   }
]

```

# Sample Query

## Input
```
{
  "source": "LGA",
  "destination": "SFO"
}
```

## Output
```
[
    [
        {
            "airline": "AAL",
            "sourceAirportId": "LGA",
            "destinationAirportId": "SFO"
        }
    ],
    [
        {
            "airline": "JBU",
            "sourceAirportId": "LGA",
            "destinationAirportId": "SFO"
        }
    ],
    [
        {
            "airline": "AAL",
            "sourceAirportId": "LGA",
            "destinationAirportId": "PHL"
        },
        {
            "airline": "JBU",
            "sourceAirportId": "PHL",
            "destinationAirportId": "PHX"
        },
        {
            "airline": "AAL",
            "sourceAirportId": "PHX",
            "destinationAirportId": "SFO"
        }
    ]
]```
