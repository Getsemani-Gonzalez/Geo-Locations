<h1>Datos Personales</h1>

<p><img src="https://scontent.fpac1-1.fna.fbcdn.net/v/t1.0-9/p720x720/75317345_1013081332373661_3512196591337340928_o.jpg?_nc_cat=108&_nc_oc=AQmH5USIgts8bGxpcqYxP4iqOSKiseQYd46KdPJtx-dXEuvEVTOJ4i9xvdwxxP0GxlI&_nc_ht=scontent.fpac1-1.fna&oh=2079724765843dd7c26c4af6120d3ae6&oe=5E880DF2">
<h2><p><strong><a href="https://getsemani-gonzalez.github.io/Formulario-de-datos/">Formulario de datos</a></strong>
<p><strong>Nombre Completo:</strong> Getsemani Gonzalez Castro 
<p><strong>Fecha Nacimiento:</strong> 24 de Enero de 2001
<p><strong>Edad:</strong> 18 años
<p><strong>Nacionalidad:</strong> Panameña 

<h1>Datos Educativos</h1>
<p><strong>Escuelas:</strong><p>
<p><em>- Primaria: Centro Educativo Burunga </em>
<p><em>- Premedia y media: Centro Educativo Cristobal Adan de Urriola. </em>
<p><strong>Universidad:</strong>
  <P><em>- Universidad de Panamà</em>
  <h1>Redes Sociales</h1>
  <p><strong>Instagram:</strong> <a href="https://www.instagram.com/vicctoriagg?igshid=1m9ijfj6qj28o">vicctoriagg</a>
  <p><strong>Facebook:</strong> <a href="https://www.facebook.com/profile.php?id=100010154114100">Gethsemane G. Castro</a> 
	  
<!DOCTYPE html>
<html>
  <head>
    <title>Geolocation</title>
    <meta name="viewport" content="initial-scale=1.0, user-scalable=no">
    <meta charset="utf-8">
    <style>
      html, body, #map-canvas {
        height: 100%;
        margin: 0px;
        padding: 0px
      }
    </style>
    <!--
    Include the maps javascript with sensor=true because this code is using a
    sensor (a GPS locator) to determine the user's location.
    See: https://developers.google.com/maps/documentation/javascript/tutorial#Loading_the_Maps_API
    -->
    <script src="https://maps.googleapis.com/maps/api/js?v=3.exp&sensor=true"></script>

    <script>
// Note: This example requires that you consent to location sharing when
// prompted by your browser. If you see a blank space instead of the map, this
// is probably because you have denied permission for location sharing.

var map;

function initialize() {
  var mapOptions = {
    zoom: 6
  };
  map = new google.maps.Map(document.getElementById('map-canvas'),
      mapOptions);

  // Try HTML5 geolocation
  if(navigator.geolocation) {
    navigator.geolocation.getCurrentPosition(function(position) {
      var pos = new google.maps.LatLng(position.coords.latitude,
                                       position.coords.longitude);

      var infowindow = new google.maps.InfoWindow({
        map: map,
        position: pos,
        content: 'Location found using HTML5.'
      });

      map.setCenter(pos);
    }, function() {
      handleNoGeolocation(true);
    });
  } else {
    // Browser doesn't support Geolocation
    handleNoGeolocation(false);
  }
}

function handleNoGeolocation(errorFlag) {
  if (errorFlag) {
    var content = 'Error: The Geolocation service failed.';
  } else {
    var content = 'Error: Your browser doesn\'t support geolocation.';
  }

  var options = {
    map: map,
    position: new google.maps.LatLng(60, 105),
    content: content
  };

  var infowindow = new google.maps.InfoWindow(options);
  map.setCenter(options.position);
}

google.maps.event.addDomListener(window, 'load', initialize);

    </script>
  </head>
  <body>
    <div id="map-canvas"></div>
  </body>
</html>
<!DOCTYPE HTML>

<html lang = "en">

<head>

  <title>location.html</title>

  <meta charset = "UTF-8" />

  <script type = "text/javascript">

  //<![CDATA[



  function getLoc(){

    navigator.geolocation.getCurrentPosition(showMap);

  } // end getLoc



  function showMap(position){

    var lat = position.coords.latitude;

    var long = position.coords.longitude;

    var linkUrl = "http://maps.google.com?q=" + lat + "," + long;

    var mapLink = document.getElementById("mapLink");

    mapLink.href = linkUrl;

    var embedMap = document.getElementById("embedMap");

    embedMap.src = linkUrl + "&z=16&amp;output=embed";

  } // end showMap



  //]]>

  </script>

</head>



<body onload = "getLoc()">

  <h1>Geolocation Demo</h1>



  <p>

    <a id = "mapLink"

       href = "http://maps.google.com">click for a map</a>

  </p>



<iframe id = "embedMap"

        width="800" 

        height="500" 

        frameborder="0" 

        scrolling="no" 

        marginheight="0" 

        marginwidth="0" 

        src= "">

</iframe><br />



</body>

</html>
p {
  animation-duration: 3s;
  animation-name: slidein;
}

@keyframes slidein {
  from {
    margin-left: 100%;
    width: 300%
  }

  to {
    margin-left: 0%;
    width: 100%;
  }
}
