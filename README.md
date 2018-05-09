<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>World Cup Counter</title>
<span>World Cup will start in:</span>
<p id="counterTimer"></p>
<script>
  var countDownDate = new Date("Jun 14, 2018 10:00:00").getTime();
  var toRefresh = setInterval(
  function() {  
  var currentTime = new Date().getTime(); 
  var refresh = countDownDate - currentTime; 
  var d = Math.floor(refresh / (1000 * 60 * 60 * 24));
  var h = Math.floor((refresh % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var m = Math.floor((refresh % (1000 * 60 * 60)) / (1000 * 60));
  var s = Math.floor((refresh % (1000 * 60)) / 1000);
  document.getElementById("counterTimer").innerHTML = d + "d " + h + "h " + m + "m " + s + "s ";
	  if (refresh < 0) {
	    clearInterval(toRefresh);
	    document.getElementById("counterTimer").innerHTML = "World Cup began!!";
	  }
}, 1000);
</script>
</head>
<body>

</body>
</html>
