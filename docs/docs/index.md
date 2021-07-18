<!DOCTYPE html>
<html> 
<head>
    <title>Greeting Message</title> 
    <style>
#lbl {
    font-family: monospace;
    font-size: xx-large;
    color: #FDD5AF;
    padding: 5px;
    border: 1px solid #FDD5AF;
    text-align: center;
    line-height: 1.5;
    height:85%


}
#date{
    font-size:x-large;
}
body{
    background-color: #860909;
}
    </style>
</head>
<body>
    <div id="lbl"></div>
</body>

<script>
    var weekday = new Array(7);
    weekday[0] = "Sunday";
    weekday[1] = "Monday";
    weekday[2] = "Tuesday";
    weekday[3] = "Wednesday";
    weekday[4] = "Thursday";
    weekday[5] = "Friday";
    weekday[6] = "Saturday";

    
    var today = new Date();
    var hrs = today.getHours();
    var dayOfWeek = weekday[today.getDay()];
    var date = dayOfWeek+" " +(today.getMonth()+1) + "/" + today.getDate() +'/'+today.getFullYear()  ;

    var greet;

    if (hrs < 12)
        greet = 'Good Morning,  ';
    else if (hrs >= 12 && hrs <= 17)
        greet = 'Good Afternoon, ';
    else if (hrs >= 17 && hrs <= 24)
        greet = 'Good Evening,  ';

    document.getElementById('lbl').innerHTML =
          greet+= "Srinithi! " +`<div id="date"> It's ${date}</div>`;
</script> 
</html>
