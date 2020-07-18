### gpauto Examples

## How to use gpauto

1) Copy gpauto in SD card root
2) Replace `Password` to your password
3) Remove battery
4) Insert SD card
5) Insert battery
6) Wait at least 10 seconds
7) Remove battery
8) Wait at least 2 seconds
9) Insert battery

# Enable WiFi
This file will enable your WiFi and BT
If [Enable WiFi](EnableWiFi/gpauto) doesn't work, use [EnableWiFiAdv](EnableWiFiAdv/gpauto)

# Change SSID/password
- Change `SSID`
- Change `NewPassword` 
[File](ChangeWiFiSettings/gpauto)

# gpauto default example
source: /usr/local/gopro/scripts/gpauto

```
goprohero
#The line above must contain the AP password for this camera.
#Copy this "/gpauto" file into the root directory of the SD card.
# then power cycle Camera twice. Once to load, once to use.
#
#One button Off Mode  (requires v03.00)
#1.Use the power button to turn off the Camera: The Wifi also powers off.
#2.Use the RC to turn off the Camera: Wifi remains on in low power RC mode.
#3.Use the Phone APP to turn off the Camera: Wifi remains on in high power mode.
EVoff_button_on,1
# The following line will set a 30 second camera off timeout for Rockypoint
EVtraffic_timeouts,wake=310:rc[scan=60:loss=30:warn=5:ok=1]app[scan=300:loss=30:warn=5:ok=1]
EVled_style,1
```


### Know commands:

- EVoff_button_on,1

The following line will set a 30 second camera off timeout for Rockypoint
- EVtraffic_timeouts,wake=310:rc[scan=60:loss=30:warn=5:ok=1]app[scan=300:loss=30:warn=5:ok=1]
- EVled_style,1

- EVssidprimary,newGoproName
- EVpassphrase,newGoProPassword

- EVwifienable