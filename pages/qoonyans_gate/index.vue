<template>
<el-container>
    <el-main>
        <h1>Qoonyan's Gate</h1> 
        <p id="demo"></p>

    </el-main>
    
</el-container>
</template>

<script>
    // Set the date we're counting down to
    var countDownDate = new Date("2019/3/21 9:35:00").getTime();

    // Update the count down every 1 second
    var x = setInterval(function() {

    // Get todays date and time
    var now = new Date().getTime();

    // Find the distance between now and the count down date
    var distance = countDownDate - now;

    // Time calculations for days, hours, minutes and seconds
    var days = Math.floor(distance / (1000 * 60 * 60 * 24));
    var hours = ('00' + Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60))).slice(-2);
    var minutes = ('00' + Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60))).slice(-2);
    var seconds = ('00' + Math.floor((distance % (1000 * 60)) / 1000)).slice(-2);

    // Display the result in the element with id="demo"
    document.getElementById("demo").innerHTML = days + "DAYS " + hours + ":"
    + minutes + ":" + seconds;

    // If the count down is finished, write some text 
    if (distance < 0) {
        clearInterval(x);
        document.getElementById("demo").innerHTML = "EXPIRED";
    }
    }, 1000);
</script>

<style>
  #demo {
      font-size: 30px;
      font-weight: 300;
  }
  .el-main {
    color: #ffffff;
    text-align: center;
    line-height: 120px;
  }
  .el-container {
    font-family: 'Courier New', Courier, monospace;
    
    height:100%;
  }
  h1 {
    font-size:25px
  }
  html {
    height: 100%;
  }

  body {
      height: 100%;
      margin: 0;
      background-color: #303133;
  }

</style>