<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Bộ đếm ngược</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 50px;
    }
    #countdown {
      font-size: 48px;
      color: #333;
    }
  </style>
</head>
<body>
  <h1>Bộ đếm ngược đến sự kiện "Hồn Tày sắc"</h1>
  <div id="countdown"></div>
  
  <script>
    // Set the date we're counting down to
    var countDownDate = new Date("May 20, 2024 00:00:00").getTime();

    // Update the countdown every 1 second
    var x = setInterval(function() {

      // Get the current date and time
      var now = new Date().getTime();

      // Calculate the remaining time
      var distance = countDownDate - now;

      // Calculate days, hours, minutes, and seconds
      var days = Math.floor(distance / (1000 * 60 * 60 * 24));
      var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      var seconds = Math.floor((distance % (1000 * 60)) / 1000);

      // Display the result
      document.getElementById("countdown").innerHTML = days + "d " + hours + "h "
      + minutes + "m " + seconds + "s ";

      // If the countdown is over, display a message
      if (distance < 0) {
        clearInterval(x);
        document.getElementById("countdown").innerHTML = "Sự kiện đã diễn ra!";
      }
    }, 1000);
  </script>
</body>
</html>
