## Uploading data to Initial State

You are going to use the `ISStreamer` Python library to stream data to your Initial State bucket.

- Open a new Python file with Idle (or your favourite Python IDE) and save it into /home/pi as IS-upload.py

-  First of all, import the parts of the ISStreamer library that you need. Add this line at the top.

    ```python
    from ISStreamer.Streamer import Streamer
    ```

- Now you need to develop the code to process each one of your weather readings. Rather than use actual measurements from your sensors during this development stage, create some test data as Python variables. Add these lines underneath your library imports. If you have a Sense Hat, you should have:

   ```python
   humidity = 55.998
   ambient_temp = 23.456
   pressure = 1067.890
   ```

   --- collapse ---
   ---
   title: Notes for Raspberry Pi Oracle Weather Station schools
   ---

   You should add the additional test data variables:
    ```python
    ground_temp = 16.345
    wind_speed = 5.6129
    wind_gust = 12.9030
    wind_average = 180
    rainfall = 1.270
    ```
--- /collapse ---

- Then add some more variables to store the Initial State streaming configuration information.

    ```python

    CITY = "Pi Town"
    BUCKET_NAME = ":partly_sunny:  Weather Station"
    BUCKET_KEY = credentials['XXXX']
    ACCESS_KEY = credentials['YYYY']
    SENSOR_LOCATION_NAME = "My School"
    ```
