# Google Maps Profile Integration #

The user can specify his exact location with the Google Maps window embedded in the profile. This works in a two-way mode:

  * If we select a country from the HTML SELECT LIST, the country will be positioned on the embedded Google Maps. And if we write a location (the country must be selected first), the location will be located on the map too.

  * If we click on the map, the country and the location will be deduced and inserted on the HTML SELECT LIST. That's the reverse geopositioning, and is accomplished making a call to a webservice of the great DB of http://www.geonames.org. All of this using Jquery for the AJAX thing.



## Screenshot ##

![http://django-profile.googlecode.com/files/maps2.png](http://django-profile.googlecode.com/files/maps2.png)