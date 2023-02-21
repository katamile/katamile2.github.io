<!DOCTYPE html>
<html>
<head>
	<title>Ciudad Mitad del Mundo</title>
	<link rel="stylesheet" href="style.css">
</head>
<body>
	<header>
		<h1>Ciudad Mitad del Mundo</h1>
	</header>
	
	<main>
		<section>
			<h2>Atracción turística</h2>
			<p>La Ciudad Mitad del Mundo es un monumento que marca la línea ecuatorial, donde se puede pararse con un pie en cada hemisferio. Es una de las atracciones turísticas más populares de Ecuador.</p>
			<img src="mitad-del-mundo.jpg" alt="Ciudad Mitad del Mundo">
		</section>
		
		<section>
			<h2>Calculadora de distancia</h2>
			<p>Ingresa tu ubicación para calcular la distancia a la Ciudad Mitad del Mundo:</p>
			<form>
				<label for="location">Ubicación:</label>
				<input type="text" id="location" placeholder="Ingresa tu ubicación">
				<button type="button" onclick="calcDistance()">Calcular distancia</button>
			</form>
			<p id="distance"></p>
		</section>
	</main>
	
	<script>
		function calcDistance() {
			// código para calcular la distancia a la Ciudad Mitad del Mundo
		}
	</script>
</body>
</html>
