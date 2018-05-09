# world-cup-counter
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>World Cup Counter</title>
<p id="exercise"></p>

<script>
var WCDate = new Date("Jun 14, 2018 10:00:00").getTime();
var x = setInterval(function() {

var today= new Date().getTime();

var lapse = WCDate - today;

  var days = Math.floor(distance / (1000 * 60 * 60 * 24));
  var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
  var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
  var seconds = Math.floor((distance % (1000 * 60)) / 1000);

  document.getElementById("exercise").innerHTML = days + "d " + hours + "h "
  + minutes + "m " + seconds + "s ";

  if (lapse < 0) {
    clearInterval(x);
    document.getElementById("exercise").innerHTML = "World Cup Began!!";
  }
}, 1000);
</script>
</head>
<body>

</body>
</html>
