# Weather Data Generator

## Synosis
####  we are going to generate fake weather data for a game!!!.
<p>
We need you to provide a prototype of a program which articially simulates the weather and outputs weather
data in a standard format for our game to read.</p>

The Game under development needs test data to do the testing of different use cases. One use case for testing 
is to simulate a scenario using weather data which the game uses for smooth operation.

This tool will generate the weather data for definite set of locations. The weather data generator tool will 
utilise an algorithmic approach to generate the data. The approach will assume various factors like location
coordinates, elevation, pressure, humidity, temperature to generate the weather data for a location for a specific date and time.

The `Hypsometric algorithm` will be utilised to generate pressure, humidity variable based on the elevation
of the location from sea level.

Algorithm Reference **[here](https://keisan.casio.com/exec/system/1224579725)**

### Output data format expected 
```
Sydney|-33.86,151.21,39|2015-12-23T05:02:12Z|Rain|+12.5|1004.3|97
Melbourne|-37.83,144.98,7|2015-12-24T15:30:55Z|Snow|-5.3|998.4|55
```
## Technologies used
- Python 3.7.4
## Development Platform
- Mac OS Mojave
###  Python packages used
* datetime
* random
* time
* json
* os
* sys
* faker
* geopy

## User manual

### Installation
- Checkout the code to a directory of your choice\
`git clone https://github.com/avp1984/weatherdata.git`
- change to the directory `weatherdata` 
- The necessary python packages required are installed by running the command,\
`pip install -r  requirements.txt`


### Execution
The weather data can be generated by running the command
> `python src/WeatherDataGen <config_file> <output_file.psv>`
> - `Eg: python src/WeatherDataGen.py src/config.json weather_data.psv`