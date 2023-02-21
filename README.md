<html>
<head>
	<title>Ciudad Mitad del Mundo</title>
	<style>
	      h1 {
		color: red;
	      }
	      p {
		color: blue;
	      }
	      body {
		background-color: #FFF5DA;
	      }
    </style>
</head>
<body>
	
	<h1>Ciudad Mitad del Mundo</h1>
	
		<section>
			<h2>Atracción turística</h2>
			<p>La Ciudad Mitad del Mundo es un monumento que marca la línea ecuatorial, donde se puede pararse con un pie en cada hemisferio. Es una de las atracciones turísticas más populares de Ecuador.</p>
			<img src="img/mitad-del-mundo-quito.jpg"/>
		</section>
		
    <h1>Calculadora de Distancia a la Mitad del Mundo</h1>
    <p>Su ubicación actual: <span id="location"></span></p>
    <p>Distancia a la mitad del mundo: <span id="distance"></span></p>

    <script>
      // Obtener la ubicación actual
      navigator.geolocation.getCurrentPosition(function (position) {
        var lat1 = position.coords.latitude;
        var lon1 = position.coords.longitude;

        // La ubicación de Quito es  ??
        var lat2 = -0.0102496 ;
        var lon2 = -78.4464668;

        // Función para calcular la distancia en kilómetros
        var R = 6371; // Radio de la Tierra (km)
        var dLat = (lat2 - lat1) * (Math.PI / 180);
        var dLon = (lon2 - lon1) * (Math.PI / 180);
        var a = Math.sin(dLat / 2) * Math.sin(dLat / 2) +
                Math.cos(lat1 * (Math.PI / 180)) * Math.cos(lat2 * (Math.PI / 180)) *
                Math.sin(dLon / 2) * Math.sin(dLon / 2);
        var c = 2 * Math.atan2(Math.sqrt(a), Math.sqrt(1 - a));
        var d = R * c;
	    
        // Mostrar la distancia en la página
        document.getElementById("location").innerHTML = lat1 + ", " + lon1;
        document.getElementById("distance").innerHTML = d + " km";
      });
    </script>
</body>
</html>
