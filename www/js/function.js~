/**
 *
 * trigger on success geolocation event
 */
function onSuccess(position) {
    var element = document.getElementById('geolocation');                
    var myLat = position.coords.latitude;
    var myLong = position.coords.longitude;
    //harcodig de coordenadas del santiago bernabeu
    var lat = 40.453017;
    var long = -3.688335;
    var latLng = new google.maps.LatLng(lat,long);
    var myLatLng = new google.maps.LatLng(myLat,myLong);
    var mapOptions = {                    
        zoom: 18,
        center: latLng,
        scrollwheel: false,
        disableDefaultUI: true,
        draggable: false
    }
    var map = new google.maps.Map(document.getElementById('map-canvas'), mapOptions);
    google.maps.event.addListener(map, 'click', function(event) {
        window.location = 'geo:40.453017,-3.688335';
    });
    google.maps.event.addListener(map, 'rightclick', function(event) {
        window.location = 'geo:40.453017,-3.688335';
    });
    var marker = new MarkerWithLabel({
        position: latLng,
        map: map,
        draggable: false,
        labelContent: 'Usted se encuentra a: <br />' + calcDistance(latLng, myLatLng) + ' Km <br /> del estadio Santiago Bernabeu',
        labelAnchor: new google.maps.Point(100, 0),
        labelClass: "labels", // the CSS class for the label
        labelStyle: {opacity: 0.50, border: '1px solid #000', 'border-radius': '3px', padding: '1px'}
    });
    element.innerHTML = 'Usted se encuentra a: <br />' + calcDistance(latLng, myLatLng) + ' Km <br /> del estadio Santiago Bernabeu <br /> <hr />';
}

/**
 *
 * trigger on error geolocation event 
 * @param object error
 */            
function onError(error) {
    alert('code: ' + error.code + '\n' +
        'message: ' + error.message + '\n');
}
            
/**
 *
 * @param google.maps.LatLng p1
 * @param google.maps.LatLng p2
 * @return float con la distancia entre los puntos
 */
function calculateDistance(p1, p2){                
    return (google.maps.geometry.spherical.computeDistanceBetween(p1, p2)).toFixed(2);
}

function onSuccessMyGps(position) {
    alert('Latitud: '          + position.coords.latitude          + '\n' +
          'Longitud: '         + position.coords.longitude         + '\n');
}
