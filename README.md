# tesisivanco
usamos thingspeak


<html>
<head>

  <!-- 
  
  NOTE: This plugin will not be visible on public views of a channel. 
        If you intend to make your channel public, consider using the
        MATLAB Visualization App to create your visualizations.
  
  -->  

  %%PLUGIN_CSS%%
%%PLUGIN_JAVASCRIPT%%
  
</head>
<body>  
  Datos  Posicionamiento , fecha , caudal volumen.
 Inicio evento
     
  
  
  <div id="json" ></div>
  
 fin evento 
     <div id="str"></div>
</body>
</html>





<style type="text/css">
  body { background-color: #ddd; }
</style>







<script type='text/javascript' src='https://ajax.googleapis.com/ajax/libs/jquery/1.4.4/jquery.min.js'></script> 
<script type='text/javascript' src='https://www.google.com/jsapi'></script>

<script type="text/javascript">
  var data;
  
  
  $.getJSON('https://api.thingspeak.com/channels/660168/feed/last.json?result=4', function(data) {
	
     
    console.log(data);
		// get the data point
    //document.write(data.field1);
	document.getElementById('json').innerHTML = data.field1;
	document.getElementById('str').innerHTML = data.field2;	
	
  });
  
</script>
