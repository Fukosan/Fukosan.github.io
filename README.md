<!DOCTYPE html> <!--Los documentos HTML5 comienzan con esta declaración-->

<!-- 
Existen varias instrucciones nuevas en HTML5, tales como:
<article>: Define un artículo.
<aside>: Define contenido aparte (A un lado?) del contenido normal de la página. 
<audio>: Define contenido de audio.
<canvas>: Usado para dibujar gráficos vía scripts.
<datalist>: Especifica una lista de opciones predefinidas o de input.
<details>: Define detalles de un elemento.
<embed>: Define contenedores para una aplicación externa no-HTML.
<footer>: Define un pie de página. 
<header>: Define un encabezado.
<nav>: Define una sección de navegación.
<output>: Representa el resultado de una operación realizada por un script.
<progress>: Representa el progreso de una tarea.
<section>: Define una sección de un documento.
<video>: Define contenido video.
Cabe destacar que el sistema de codificación de carácteres estándar es UTF-8.
Entre las cosas nuevas que encontramos en HTML5 están:
Nuevos tipos de campos "input" (search, email, url, tel, number, range, date, month, week, time, datetime, datetime-local, color)
Métodos PUT and DELETE.
Drag and Drop.
Audio y video.
Aplicaciones web offline.
Historial.
Almacenamiento local.
Geolocalización.
Mensajería web.
Entre otros.	
-->

<!--
HTML5 introduce siete nuevos tipos de contenedores:
	Metadata: Prepara la presentación o el comportamiento del documento y su contenido. Se encuentra en el HEAD del documento. Entre los elementos ocupados por este contenedor están:
					
		Base: Establece un URL objetivo para todos los links relativos del documento.
		Link: Define una relación entre un documento y un recurso externo.
					
		Meta: Define metadatos usados por un documento HTML. Usualmente se ocupa para describir la página (Autor, palabras claves que ayuden a buscar la página, entre otros).
		Noscript: Define contenido alternativo para navegadores que no tienen soporte de scripts.
		Script: Define contenidos script. Puede usarse también en body.
					
		Style: Define información de estilo del documento. 
					
		Title: Define un titulo para la página.
				
	Embedded: Contenido que importa recursos al documento.
		Audio: Define contenido de sonido. Sopota tres formatos: MP3, WAV Y OGG.
		Video: Define contenido de video. Soporta mp4, webm y ogg.
		Canvas: Usado para dibujar gráficos vía scripts.
		iFrame: Define un "Inline Frame", es decir, un documento HTML dentro de otro. Sirve con documentos, páginas y videos de youtube.
		Img: Define una imagen.
		Math: Usado para expresar y visualizar expresiones matemáticas. Tristemente, no funciona en chrome.
		Object: Define un elemento multimedia tal como audio, video, flash, pdf, entre otros.
		Svg: Define gráficos svg, es decir, gráficos 2D.
				
	Interactive: Contenido creado para la interacción con el usuario.
		
		A: Define un hipertexto.
		Button: Define un botón.
		Details: Crea una ventana con detalles.
		Embed: Define un contenedor de una animación flash.
		Label: Es usado en conjunto con los elementos "form". Es texto que va específicamente con la form.
		Select: Usado para crear listas desplegables.
		Textarea: Usado para crear contenedores que admiten infinitas lineas de texto. Se pueden limitar con el atributo "maxlenght".
		También se incluyen audio, video, iframe, img, object, input.
		
	Heading:
				
	Phrasing:
				
	Flow:
				
	Sectioning:
El objetivo de estos es hacer la página más entendible y ordenada tanto para quien la usa como para el que la diseña.
-->

<html>
	<head>
		<base href="www.google.cl"> 

		<link rel="icon" href="https://cdn0.iconfinder.com/data/icons/HTML5/128/HTML_Logo.png">

		<meta charset="UTF-8"> 
		<meta name="author" content="Benjamin Islas"> 
		<meta name="keywords" content="DUCKS, DUCKS, DUCKS, DUCKS"> 
		<meta name="description=" content="Página creada para testear y aprender acerca de contenedores"> 
		<meta name="viewport" content="width=device-width, initial-scale=1.0"> <!--Establece intrucciones para que la página se arregle según el aparato en el que se visualiza la página-->

		<noscript>¡Lamentablemente tu navegador no tiene soporte para Scripts!</noscript>

		<script>
			function myFunction(id) {
				if (document.getElementById(id).style.color == "white"){
				    document.getElementById(id).style.color = "black";
				    document.body.style.background ="#FFFFFF";
				}
				else{
				    document.getElementById(id).style.color = "white";
				    document.body.style.background = "#000000";					
				}
			}
		</script>	

		<script>
			function dibujar(id) {
				var c = document.getElementById(id);
				var ctx = c.getContext("2d");
				ctx.font = "75px Arial";
				ctx.fillText("ZA WARUDO",25,150);
				var audio = new Audio("https://www.myinstants.com/media/sounds/za-warudo-toki-wo-tomare-1.mp3");
				audio.play();
				var audiodos = new Audio("https://www.myinstants.com/media/sounds/dio-wryyy.mp3");			
				setTimeout(function(){audiodos.play();}, 4300);
			}
		</script>		

		<style>
			h1 {color:white;font-family:georgia;font-size:300%;}
			p {color:white;font-family:georgia;font-size:150%;}
		</style>

		<title>CONTAINERS</title>
	</head>

	<body>
		<center>
			<body bgcolor="#000000" id="Fondo">			
			<h1><b><span id="Titulo" onclick="myFunction(this.id)">EMBEDDED</span></b></h1>
			<hr/>
			<p>AUDIO</p>


			<audio controls title="YUME 2KKI IS AMAZING">
				<source src="https://vignette.wikia.nocookie.net/yume2kki/images/0/06/Aquarium.ogg" type="audio/ogg">
				<source src="horse.mp3" type="audio/mpeg"> 
				<source src="horse.wav" type="audio/wav">
				Your browser does not support the audio element. <!-- Este texto solo se mostrará en navegadores que no soporten el formato audio-->
			</audio>

			<p>VIDEO</p>

			<video width="800" height="400" loop autoplay title="I DIDN'T KNOW DIIVES WAS CHILEAN <3"> 
				<source src="https://cs.sankakucomplex.com/data/4a/a8/4aa86f8b196386f855af81aaa05b9da2.webm" type="video/webm">
				<source src="movie.mp4" type="video/mp4">
				<source src="movie.ogg" type="video/ogg">
		    	Your browser does not support the video tag.
			</video>

			<p>CANVAS (Click it)</p>

			<canvas id="myCanvas" width="500" height="250" style="border:1px solid #FFFFFF;background: #FFFFFF" onclick="dibujar(this.id)">
				Your browser does not support the HTML5 canvas tag.
			</canvas>

			<p>IFRAME</p>

			<iframe width="500" height="250" src="https://www.youtube.com/embed/3LwrzFBK2IQ?ecver=1" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen>
				Your browser does not support the HTML5 canvas tag.
			</iframe>

			<p>IMG</p>

			<img src="https://media1.giphy.com/media/100QWMdxQJzQC4/giphy.gif" alt="A cute dog" height="450" width="450">

		    <p>OBJECT</p>

		    <object width="700" height="500" name="PDF" data="https://www.rscautomobile.com/data/documents/cars/1511270057-naamloosdocument.pdf"></object> 

		    <p>SVG</p>

			<svg width="250" height="250">
				<circle cx="125" cy="125" r="175" stroke="white" stroke-width="20" fill="black" onclick="circulo()"/>
				<circle cx="125" cy="125" r="150" stroke="white" stroke-width="20" fill="black" onclick="circulo()"/>
				<circle cx="125" cy="125" r="125" stroke="white" stroke-width="20" fill="black" onclick="circulo()"/>
				<circle cx="125" cy="125" r="100" stroke="white" stroke-width="20" fill="black" onclick="circulo()"/>
	     		<circle cx="125" cy="125" r="75" stroke="white" stroke-width="20" fill="black" onclick="circulo()"/>
	     		<circle cx="125" cy="125" r="50" stroke="white" stroke-width="20" fill="black" onclick="circulo()"/>
	     		<circle cx="125" cy="125" r="25" stroke="white" stroke-width="20" fill="black" onclick="circulo()"/>
	     		<circle cx="125" cy="125" r="1" stroke="white" stroke-width="20" fill="black" onclick="circulo()"/>
	     		<circle cx="125" cy="125" r="1" stroke="black" stroke-width="1" fill="black" onclick="circulo()"/>
			</svg>

			<p>A AND BUTTON</p>

			<a href="http://www.google.cl"><button type="button">Click me!</button></a>

			<p>DETAILS</p>

				<div style="background-color:white; color:black; padding:1px 1px 10px 1px;">
					<details>
						Inserte detalles aquí
					</details>			
				</div>				

			<p>EMBED (Blank swf file)</p>

			<embed src="test.swf" width="100" height="100">

			<p>LABEL</p>

				<input type="checkbox" id="agree" /> 
				<label style="color:white;font-size:80%" for="agree">I agree with the Terms and Conditions</label>

			<p>SELECT</p>

			<select>
			  <option value="1">1</option>
			  <option value="2">2</option>
			  <option value="3">3</option>
			  <option value="4">4</option>
			</select>

			<p>TEXTAREA</p>

			<textarea autofocus wrap="soft" placeholder="J̴̢̡͎͕͕̪̯͇̓̇͆̒̂͆̍͐́͝U̧͇̞̙ͩ̆̋̂͑͊̄͋̑̐̄S̨̢̧̪̘̤̺͓͎͚̜̝͓̮̳̐̿̊̇̍̓͛̋̑̔͞T̵̛̪͙̣̼̺͓̠͈̥̤̪̯̯͓̞͔͔͊ͬ̆͢͠ ̴̺͇̮̻͔ͣ̄͌ͣ̀́͢͜M̸̆̎ͥ͒̔̇̈ͩ̄͒ͧ̚̚҉̛̞̯̬̲͓̺̼̼͇̝̞̦̟̖͙̭̺͜͞ͅͅO̶̧̧̙͓̱̪̪̘̫͕̣̟̙̩͂̈̽̀͆̊ͮͪͩ̓ͨ̑̍̽͗̄̒̂ͫ͘Ṇ̨̛̼̣͓̗͔̣̳̮̥͍̘̠ͧ̄̿ͧͨͭ̀I̞̯̣̺̱̪̱̪̙͑̉ͦ̔ͧͭͨͩ̐̂̽̓̃̅͆͗ͣ̈͟͢͝͡K̸̰̫̻̗͎̟̘̠̱͉̠̮̥̑ͫͫ̽̉͛͗̿͌͒̄͗͗̓̀̆͢A̸ͭ̍͗̉̄͑̒̍̆͊́̚҉̝͈͖̗̳͔̮͍̙̱̳̗͔̥̙̥̮͚̠" rows="4" cols="50">J̴̢̡͎͕͕̪̯͇̓̇͆̒̂͆̍͐́͝U̧͇̞̙ͩ̆̋̂͑͊̄͋̑̐̄S̨̢̧̪̘̤̺͓͎͚̜̝͓̮̳̐̿̊̇̍̓͛̋̑̔͞T̵̛̪͙̣̼̺͓̠͈̥̤̪̯̯͓̞͔͔͊ͬ̆͢͠ ̴̺͇̮̻͔ͣ̄͌ͣ̀́͢͜M̸̆̎ͥ͒̔̇̈ͩ̄͒ͧ̚̚҉̛̞̯̬̲͓̺̼̼͇̝̞̦̟̖͙̭̺͜͞ͅͅO̶̧̧̙͓̱̪̪̘̫͕̣̟̙̩͂̈̽̀͆̊ͮͪͩ̓ͨ̑̍̽͗̄̒̂ͫ͘Ṇ̨̛̼̣͓̗͔̣̳̮̥͍̘̠ͧ̄̿ͧͨͭ̀I̞̯̣̺̱̪̱̪̙͑̉ͦ̔ͧͭͨͩ̐̂̽̓̃̅͆͗ͣ̈͟͢͝͡K̸̰̫̻̗͎̟̘̠̱͉̠̮̥̑ͫͫ̽̉͛͗̿͌͒̄͗͗̓̀̆͢A̸ͭ̍͗̉̄͑̒̍̆͊́̚҉̝͈͖̗̳͔̮͍̙̱̳̗͔̥̙̥̮͚̠</textarea>













		</center>	
	</body>

</html>
