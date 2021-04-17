# Mapit 🌎

A simple Angular framework based Google Maps with place search feature. 🗺️🧭

# Description 🎀

A google map based on angular with draggable marker and place search bar to get address and laitude, longitude coordinates.

You've to use your own google API key and enable restrictions. In order to do, kindly, follow up [this link](https://developers.google.com/maps/documentation/javascript/get-api-key). 🛎️

Make sure to enable the <code>Maps Javascript API</code> (Show Map), <code>Places API</code> (Places search results) & <code>Geocoding API</code> (Convert Lat, Long to address). ⏰

# Tools used 🧰

* [Angular framework, CLI ver 11.0.4](https://angular.io/)
* [Bootstrap cdn](https://cdnjs.cloudflare.com/ajax/libs/twitter-bootstrap/4.5.3/css/bootstrap.min.css)
* [Angular Google Maps (AGM)](https://angular-maps.com/)
* [@types/googlemaps](https://www.npmjs.com/package/@types/googlemaps)

# To run 🏃
1. <code>git clone</code> using https://github.com/Kshatriyaprithviraj/Angular-Mapit.git
2. navigate to folder after <code>git clone</code> and run <code>npm install</code>
3. open http://localhost:4200

# Disclaimer ⚡

Depending upon the AGM version, you may get an error for Mouseevent on map when in use of <code>markerDragEnd()</code> method.
For @agm/core version < 3.0, MouseEvent doesn't come anymore from <code>@agm/core</code>
 i.e., Usage will depend on the version of AGM. 😀
 
 For the version that I've implemented i.e., @agm/core@3.0.0.beta, you've to use MouseEvent as follow :

```typescript
mapClicked($event: google.maps.MouseEvent): void {
    this.markers.push({
      lat: $event.latLng.lat(),
      lng: $event.latLng.lng(),
      draggable: true
    });
  }
 ```
 
Cheers!!  🥂
