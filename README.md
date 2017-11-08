# Temperature-Converter-
Converter for fahrenheit to celsius, and celsius to fahrenheit.
<!DOCTYPE html>
<html>
<head>
   <!--
      JavaScript 6th Edition
      Chapter 2
      Hands-on Project 2-1

      Author: Russ f to c project 
      Date:   

      Filename: index.htm
   -->
   <meta charset="utf-8" />
   <meta name="viewport" content="width=device-width,initial-scale=1.0">
   <title>Hands-on Project 2-1</title>
   <link rel="stylesheet" href="styles.css" />
   <link href="https://fonts.googleapis.com/css?family=Cinzel|Days+One|Signika+Negative" rel="stylesheet">
   <script src="modernizr.custom.05819.js"></script>
</head>

<body>
   <header>
      <h1>
         Temperature Converter
      </h1>
   </header>

   <article>
      <h2>Fahrenheit (&#176; F) to Celsius (&#176; C) converter</h2>
      <form>
          <fieldset>
            <label for="fValue">
              Enter temp in &#176; F
            </label>
            <input type="number" id="fValue" />
          </fieldset>
          <fieldset>
            <button type="button" id="button">Convert to &#176; C</button>
          </fieldset>
          <fieldset>
             <p>Enter Temp in &#176; C</p>
            <p id="cValue">&nbsp;</p>
          </fieldset>
	  </form>
	</article>
	
	<article>
	  <h2>Celsius (&#176; C) to Fahrenheit (&#176; F) converter</h2>
	  <form>
		  <fieldset>
            <label for="ccValue">
              Enter temp in &#176; C
            </label>
            <input type="number" id="ccValue" />
          </fieldset>
		  
          <fieldset>
            <button type="button" id="buttons">Convert to &#176; F</button>
          </fieldset>
          <fieldset>
             <p>Enter Temp in &#176; F</p>
            <p id="ffValue">&nbsp;</p>
          </fieldset>
     </form>
   </article>
   <script>
		function convert() {
			var degF = document.getElementById("fValue").value;
			var degC = (degF - 32) * (5 / 9);
			document.getElementById("cValue").innerHTML = degC;
		}
		
		document.getElementById("button").addEventListener("click", convert, false);
	</script>
	
	<script>
		function convert() {
			var degC = document.getElementById("ccValue").value;
			var degF = degC * 1.8 + 32;
			document.getElementById("ffValue").innerHTML = degF;
		}
		
		document.getElementById("buttons").addEventListener("click", convert, false);
   </script>
</body>
</html>
