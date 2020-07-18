# gpauto documentation

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

## Examples
##### Enable WiFi [File](Examples/EnableWiFi/gpauto)
This file will enable your WiFi and BT

If [EnableWiFi](Examples/EnableWiFi/gpauto) doesn't work, use [EnableWiFiAdv](Examples/EnableWiFiAdv/gpauto)

##### Change SSID/password [File](Examples/ChangeWiFiSettings/gpauto)
- Change `SSID`
- Change `NewPassword` 


##### gpauto default [File](Examples/default/gpauto)
source: /usr/local/gopro/scripts/gpauto


## Know commands:
```
- EVoff_button_on,1

# The following line will set a 30 second camera off timeout for Rockypoint
- EVtraffic_timeouts,wake=310:rc[scan=60:loss=30:warn=5:ok=1]app[scan=300:loss=30:warn=5:ok=1]
- EVled_style,1

- EVssidprimary,newGoproName
- EVpassphrase,newGoProPassword

- EVwifienable,1
```