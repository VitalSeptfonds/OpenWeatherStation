# OpenWheatherStation

## The Project
The main goal is to create an Open Wheather Station based on STM32.
This weather station will give access to real time data through an Web API.

### Main Functionality 
- POE : Power Over Ethernet
- 3D printable 
- Ingress Protection : IP33
  - Protected from tools and wires greater than 2.5 millimeters
  - Protected from water spray less than 60 degrees from vertical
- Real time data
- Sensors :
  - Temperature
  - Humidity
  - Pressure
  - Light


## API
### Request
`GET /get_data/`

Return Real Time Data

### Response


    {
      "time" : "01/01/01 00:00:00",
      "data" :
        {
          "temperature" : 20.00,
          "humidity" : 50,
          "pressure" : 1013,
          "light" : 3000
        }

    }



## Error handling

Error responses should include a common HTTP status code, message for the developer, message for the end-user (when appropriate), internal error code

    {
      "error" :
        {
          "status" : 400,
          "errorCode" : "444444",
          "errorMessage" : "Verbose, plain language description of the problem. Provide developers
           suggestions about how to solve their problems here",
          "userMessage" : "This is a message that can be passed along to end-users, if needed."
         }
    }

Use three simple, common response codes :

* 400 - Bad Request
* 404 - Not Found
* 500 - Internal Server Error

## Docs

### Hardware

### Software
