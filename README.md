<!DOCTYPE html>
<html>
<head>

	<title>Mini Planet System</title>
	<link rel="stylesheet" type="text/css" href="bootstrap.css" />
     <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.2.1/jquery.min.js"></script>
     <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"></script>

<style type="text/css">
	
        body{
        	background-image: url("bg2.jpeg");
        }

        #system{
            width:1000px;
            margin:auto;
            height:600px;
        }

        #sun{
          width:100px;
          height:100px;
            margin-top:250px;
            margin-left:450px;
            position:absolute;
          border-radius:100%;
        }

        #merc{
            position:absolute;
            margin-left:150px;
            height:50px;
            width:50px;
          border-radius:100%;
        }

        #venus{
        	display: block;
            position:absolute;
            margin-left:250px;
            height:50px;
            width:50px;
          border-radius:100%;
        }

        #earth{
            position:absolute;
            margin-left:300px;
            height:50px;
            width:50px;
          border-radius:100%;
        }

        #merc-orbit{
            position:absolute;
            margin-top:200px;
            margin-left:400px;
            width:200px;
            height:200px;
            border:1px dotted black;
            border-radius:100%;
            -webkit-animation:spin 10s linear infinite;
            animation:spin 10s linear infinite;
        }

        #venus-orbit{
            position:absolute;
            margin-top:150px;
            margin-left:350px;
            width:300px;
            height:300px;
            border:1px dotted black;
            border-radius:100%;
            -webkit-animation:spin 10s linear infinite;
            animation:spin 10s linear infinite;
        }

        #earth-orbit{
            position:absolute;
            margin-top:50px;
            margin-left:250px;
            width:500px;
            height:500px;
            border:1px dotted black;
            border-radius:100%;
            -webkit-animation:spin 10s linear infinite;
            animation:spin 10s linear infinite;
        }

        @-webkit-keyframes spin{
        100%{
                -webkit-transform:rotate(360deg);
                transform:rotate(360deg);
        }
        }
        @keyframes spin{
        100%{
                -webkit-transform:rotate(360deg);
                transform:rotate(360deg);
        }

</style>
</head>


<body >

            <div class="btn-group">
                  <button type="button" class="btn btn-danger dropdown-toggle" data-toggle="dropdown" >
                  <i>Mercury <span class="caret"></span> </i> </button>
                  <ul class="dropdown-menu" role="menu" >
                        <li onclick="restart_merc()" >Start</li>
                        <li onclick="pause_merc()" > Stop</li>
                  </ul>
            </div>

            <div class="btn-group">
                  <button type="button" class="btn btn-danger dropdown-toggle" data-toggle="dropdown" >
                  <i>Venus <span class="caret"></span> </i> </button>
                  <ul class="dropdown-menu" role="menu" >
                        <li onclick="restart_venus()" >Start</li>
                        <li onclick="pause_venus()" > Stop</li>
                  </ul>
            </div>

            <div class="btn-group">
                  <button type="button" class="btn btn-danger dropdown-toggle" data-toggle="dropdown" >
                  <i>Earth <span class="caret"></span> </i> </button>
                  <ul class="dropdown-menu" role="menu" >
                        <li onclick="restart_earth()" >Start</li>
                        <li onclick="pause_earth()" > Stop</li>
                  </ul>
            </div>

            <button type="button" class="btn btn-info" id="br" onclick="reset()">Reset</button>


<div id="system">
	<img src="sun1.jpeg" id="sun" style="background: center; background-repeat: no-repeat;" />

        	<div id="earth-orbit" >
        		<img src="pl11.jpeg" id="earth" />
        	</div>

        	<div id="venus-orbit">
        		<img src="pl13.jpeg" id="venus" />
        	</div>

        	<div id="merc-orbit">
        		<img src="pl2.jpeg"  id="merc" />
        	</div>

</div>

<script>
        function pause_merc() {
            document.getElementById("merc-orbit").style.webkitAnimationPlayState="paused";
        }
        function restart_merc() {
            document.getElementById("merc-orbit").style.webkitAnimationPlayState="running";
        }
        function pause_venus() {
            document.getElementById("venus-orbit").style.webkitAnimationPlayState="paused";
        }
        function restart_venus() {
            document.getElementById("venus-orbit").style.webkitAnimationPlayState="running";
        }
        function pause_earth() {
            document.getElementById("earth-orbit").style.webkitAnimationPlayState="paused";
        }
        function restart_earth() {
            document.getElementById("earth-orbit").style.webkitAnimationPlayState="running";
        }
        function reset(){
            location.reload() ;
        }
</script>

</body>
</html>
