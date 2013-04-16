# geopy

© GeoPy Project and individual contributors,
[MIT License](https://github.com/geopy/geopy/blob/master/LICENSE)

geopy is a Python client for several popular geocoding web services.

This is a fork of geopy for updating geopy and adding some capabilities for
display of data on google maps.

Current geocoder classes for the [Google Geocoding API (V3)][google_v3],
[geocoder.us][geocoderus], [Bing Maps API][bing], [Nokia Here][nokia],
and several more Geocoder API services. The various geocoder classes are located in
[geopy.geocoders][geocoders_src]. Note that Yahoo has shut its geocoding
service.

[google_v3]: https://developers.google.com/maps/documentation/geocoding/
[bing]: http://www.microsoft.com/maps/developers/web.aspx
[geocoderus]: http://geocoder.us/
[geocoders_src]: https://github.com/geopy/geopy/tree/master/geopy/geocoders


## Basic Geocoding

**Examples**

from geopy import geocoders

b = geocoders.Bing(api_key)

n = geocoders.Nokia(api_id, app_code)

g = geocoders.GoogleV3()

b.geocode("Doak nagar, madurai, india")
>> (u'Doak Nagar, Tamil Nadu, India', (9.935750007629395, 78.08531951904297))

n.geocode("Doak nagar madurai india", (9.9, 78))
>> (u'Doak Nagar Madurai TN', (9.93575, 78.08532))

g.geocode("Doak nagar madurai india")
>> (u'Doak Nagar, Madurai, Tamil Nadu 625016, India',
>>             (9.935720600000002, 78.0844477))

