This repo contains a list of countries containing center, south west and north east latitude and longitude.
The list can be used for centering on a country in google maps.

Here is a code example:
```js
    fetch('./countries.json')
        .then(response => response.json())
        .then(countries => {
            const INDIA = countries.find(country => country.long_name === 'India')
            console.log(INDIA)
            const FRANCE = countries.find(country => country.short_name === 'FR')
            console.log(FRANCE)
            /* // for google maps
            var myOptions = {center: new google.maps.LatLng(FRANCE.center_lat, FRANCE.center_lng)}
            var map = new google.maps.Map(document.getElementById("myMap"), myOptions);
            var bounds = new google.maps.LatLngBounds(
                        new google.maps.LatLng(FRANCE.sw_lat, FRANCE.sw_lng),
                        new google.maps.LatLng(FRANCE.ne_lat, FRANCE.ne_lng) );
            map.fitBounds(bounds); 
            */
        });
 ```
