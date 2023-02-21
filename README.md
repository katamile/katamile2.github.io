<html>
<head>
	<title>Ciudad Mitad del Mundo</title>
	<style>
	      h1 {
		color: #900C3F;
      	font-family: Candara;
      	font-size: 30pt;
	      }
      
      		h2 {
		color: #FF5733;
      	font-family: Brush Script MT;
      	font-size: 25pt;
	      }
      
	      p {
		color: #C70039;
      	font-family: Cambria;
     	font-size: 15pt;
	      }
      
	      body {
		background-color: #F9EBEA;
	      }
      
     	.calculo{
		font-weight: bolder;
	      }
    </style>
</head>
<body>
	
	<h1>Ciudad Mitad del Mundo</h1>
	
		<section>
			<h2>Atracción turística</h2>
			<p>La Ciudad Mitad del Mundo es un monumento que marca la línea ecuatorial, donde se puede pararse con un pie en cada hemisferio. Es una de las atracciones turísticas más populares de Ecuador.</p>
			<img src="img/mitad-del-mundo-quito.jpg"/>
          
          <p>La principal atracción del lugar es el monumento a la Mitad del Mundo, el cual tiene como finalidad el resaltar la ubicación exacta de la línea ecuatorial, del cual el país toma su nombre, y destacar también la misión geodésica franco-española del siglo XVIII que ubicó el sitio aproximado por el cual pasa la línea equinoccial.
            
También se encuentra el Museo Etnográfico Mitad del Mundo, un museo sobre la etnografía indígena de Ecuador. Una pequeña ciudad que rodea el monumento actúa como centro turístico, ofreciendo una réplica de una ciudad colonial española llamada "Ciudad Mitad del Mundo".</p>
			<img src="img/612664395a40232133447d33247d383533303033313133.jfif"/>
		</section>
		
    <h1>Calculadora de Distancia a la Mitad del Mundo</h1>
    <p class="calculo">Su ubicación actual:</p>
  	<p><span id="location"></span></p>
  
    <p class="calculo">Distancia a la mitad del mundo:</p>
  	<p><span id="distance"></span></p>

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
