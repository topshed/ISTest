## Using live data

- For testing and development, you used some fictitious data values, stored as variables in your code. Once you've tested your upload, you should delete these and use the code to process real data from your weather station.

- As we're going to be building some dashboards, it will be easier to see a text-based representation of the wind direction. At the moment we send a numerical value for the angle detected by our wind vane. Let's convert that into cardinal  (N, S, E or W) or intercardinal  directions (ESE, NW etc).

- There are 16 possible values First of all, divide the angle by 22.5 (because 360 degrees / 16 directions = 22.5deg/direction change.
Add .5 so that when you truncate the value you can break the 'tie' between the change threshold.
Truncate the value using integer division (so there is no rounding).
Directly index into the array and print the value (mod 16).
```python
def degrees_to_cardinal(d):

    dirs = ["N", "NNE", "NE", "ENE", "E", "ESE", "SE", "SSE",
            "S", "SSW", "SW", "WSW", "W", "WNW", "NW", "NNW"]
    #ix = int((d + 11.25)/22.5)
    ix = int((d + 11.25)/22.5 - 0.02)
    return dirs[ix % 16]
```


```python
streamer.log(":cloud_tornado: " + SENSOR_LOCATION_NAME + " Wind Direction Text", wind_direction_text)
```

The Oracle Weather Station software uses the Crontab method to run a Python script called [log_all_sensors.py](https://github.com/raspberrypi/weather-station/blob/master/log_all_sensors.py) every 5 minutes. A simple way to modify your Weather Station so that it regularly uploads data to Weather Underground is to add the upload code you have written to this file.

If you've followed the [standard installation instructions](https://www.raspberrypi.org/learning/weather-station-guide/), this script should be run every five minutes via Cron, which is a sensible frequency for uploading to a site like Weather Underground.

If you get stuck, here is a basic example of a [modified log_all_sensors.py](resources/log_all_sensorsWU.py) script.


Once you have data uploading regularly, you can use your Initial State dashboard to analyse how your local climate is changing over time.

![](images/image5.png)
