## What you will need

You need to have built and installed your Oracle Weather Station kits.  If you have not done that yet, follow [these instructions](https://www.raspberrypi.org/learning/weather-station-guide/), and then come back here when you've finished!

The steps in this guide assume that you will be continuously uploading data to Weather Underground. You can do this *and* continue to upload data to the Oracle database. If you have limited bandwidth or poor connectivity between your station and the internet, then you might want to consider a configuration that sends data every 15 minutes. The Weather Underground website will not display any data older than 20 minutes, so batch uploads of data are only really useful for historical storage. If you have one of out school Weather Station kits and frequent uploads cause problems, then you should probably stick to only using the Oracle database as described in the standard software build guide.

### Hardware

- A Raspberry Pi Oracle Weather Station kit.

### software

- The [Oracle Weather Station software](https://www.raspberrypi.org/learning/weather-station-guide/software.md){:target="_blank"}.


 - The Python `ISStreamer` library. It can be installed by logging on to the Pi at the heart of your Weather Statio,  opening a terminal window and typing:

     ```bash
     sudo pip3 install ISStreamer

     ```
