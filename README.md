# sunrise 🌄

**sunrise** is a super simple website that uses open data APIs to display the sunrise time in your local timezone. 
I built it to demo an introductory lesson on practical API use cases. 
This is a personal project and not intended for commercial use. [View it here](https://doerrfeldbill.github.io/sunrise/).

![](https://github.com/doerrfeldbill/sunrise/blob/master/sunrise-preview.png)

## About

**sunrise** demonstrates how to use simple HTTP GET calls to open data APIs. 
First, the code calls the [GeoIPLookup.io](GeoIPLookup.io) API to return lattitude and longitude coordinates based on the caller's IP address.
Next, it uses passess these coordinates as parameters in a call to the [Sunrise-Sunset API](https://sunrise-sunset.org/api).
The Sunrise-Sunset API returns the UTC timestamp for the sunrise time.
Lastly, **sunrise** converts UTC into local time. It uses some JS functions to do that, and some janky slice methods to output what we want to see.

## Disclaimer

Since **sunrise** depends on the caller's IP address, mobile use may return an incorrect time.
Code is not elegant, it's just for sample purposes.
