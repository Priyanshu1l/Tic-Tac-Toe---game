# Tic-Tac-Toe---game
this is just a beginner level javascript project and also my first one <br>

<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title> TIC TAC TOE GAME </title>

	<style>

		*{
			margin: 0px;
			padding: 0px;
		}

		.container{

			display: grid;
			grid-template-columns: 10vw 10vw 10vw;
			justify-content: center;
			align-items: center;
		}
		
		.box{
			
			height: 20vh;
			background-color: whitesmoke;
			border: 2px solid black;
			border-radius: 10px;
			display: flex;
			justify-content: center;
			align-items: center;
         font-size: 50px;
		}

      .write{
         text-align: center;
         font-size: 20px;
         margin-top: 10px;
      }


	</style>
</head>
<body>


<div class="container">
   <div id="1" class="box" onclick="start(this.id)"></div>
   <div id="2" class="box" onclick="start(this.id)"></div>
   <div id="3" class="box" onclick="start(this.id)"></div>
   <div id="4" class="box" onclick="start(this.id)"></div>
   <div id="5" class="box" onclick="start(this.id)"></div>
   <div id="6" class="box" onclick="start(this.id)"></div>
   <div id="7" class="box" onclick="start(this.id)"></div>
   <div id="8" class="box" onclick="start(this.id)"></div>
   <div id="9" class="box" onclick="start(this.id)"></div>
</div>  

  <button class="button" style="margin-left: 47vw; margin-top: 10px; width: 100px; height: 35px;">Reset</button>
  <div class = "write" style="margin-left: 10"></div>

</body>

  <script>

  	let a = true,i=1;
	
	  function start(i){
  
             if(a){

             	document.getElementById(`${i}`).innerHTML = "X";
             	a = false;
             }
             else{
             	document.getElementById(`${i}`).innerHTML = "O";
             	 a = true;
             }

             check();
	  }

for(i=1;i<10;i++){
	 start(i);
}	 	

	 function check(){

	 	let a1,a2,a3,a4,a5,a6,a7,a8,a9;

         a1 = document.getElementById("1").innerHTML;
         a2 = document.getElementById("2").innerHTML;
         a3 = document.getElementById("3").innerHTML;
         a4 = document.getElementById("4").innerHTML;
         a5 = document.getElementById("5").innerHTML;
         a6 = document.getElementById("6").innerHTML;
         a7 = document.getElementById("7").innerHTML;
         a8 = document.getElementById("8").innerHTML;
         a9 = document.getElementById("9").innerHTML;

         if(a1 == "X" && a2 == "X" && a3 == "X"){
         	  document.querySelector(".write").innerHTML = "X win";
              document.querySelector(".write").style.color = "blue";

         }else if(a1 == "X" && a4 == "X" && a7 == "X"){
         	  document.querySelector(".write").innerHTML = "X win";
              document.querySelector(".write").style.color = "blue";

         }else if(a1 == "X" && a5 == "X" && a9 == "X"){
            document.querySelector(".write").innerHTML = "X win";
            document.querySelector(".write").style.color = "blue";

         }else if(a3 == "X" && a5 == "X" && a7 == "X"){
            document.querySelector(".write").innerHTML = "X win";
            document.querySelector(".write").style.color = "blue";

         }else if(a4 == "X" && a5 == "X" && a6 == "X"){
         	document.querySelector(".write").innerHTML = "X win";
            document.querySelector(".write").style.color = "blue";

         }else if(a7 == "X" && a8 == "X" && a9 == "X"){
            document.querySelector(".write").innerHTML = "X win";
            document.querySelector(".write").style.color = "blue";

         }else if(a2 == "X" && a5 == "X" && a8 == "X"){
            document.querySelector(".write").innerHTML = "X win";
            document.querySelector(".write").style.color = "blue";

         }else if(a3 == "X" && a6 == "X" && a9 == "X"){
            document.querySelector(".write").innerHTML = "X win";
            document.querySelector(".write").style.color = "blue";

	 }

     if(a1 == "O" && a2 == "O" && a3 == "O"){
              document.querySelector(".write").innerHTML = "O win";
              document.querySelector(".write").style.color = "blue";

         }else if(a1 == "O" && a4 == "O" && a7 == "O"){
              document.querySelector(".write").innerHTML = "O win";
              document.querySelector(".write").style.color = "blue";

         }else if(a1 == "O" && a5 == "O" && a9 == "O"){
            document.querySelector(".write").innerHTML = "O win";
            document.querySelector(".write").style.color = "blue";

         }else if(a3 == "O" && a5 == "O" && a7 == "O"){
            document.querySelector(".write").innerHTML = "O win";
            document.querySelector(".write").style.color = "blue";

         }else if(a4 == "O" && a5 == "O" && a6 == "O"){
            document.querySelector(".write").innerHTML = "O win";
            document.querySelector(".write").style.color = "blue";

         }else if(a7 == "O" && a8 == "O" && a9 == "O"){
            document.querySelector(".write").innerHTML = "O win";
            document.querySelector(".write").style.color = "blue";

         }else if(a2 == "O" && a5 == "O" && a8 == "O"){
            document.querySelector(".write").innerHTML = "O win";
            document.querySelector(".write").style.color = "blue";

         }else if(a3 == "O" && a6 == "O" && a9 == "O"){
            document.querySelector(".write").innerHTML = "O win";
            document.querySelector(".write").style.color = "blue";

    }
    else if(
   a1 != "" && a2 != "" && a3 != "" &&
   a4 != "" && a5 != "" && a6 != "" &&
   a7 != "" && a8 != "" && a9 != ""
){
   document.querySelector(".write").innerHTML = "Match Draw";
   document.querySelector(".write").style.color = "red";
}
    

    
}


	 function restart(){

    let a1,a2,a3,a4,a5,a6,a7,a8,a9;

document.querySelector("button").addEventListener("click",()=>{
    a1 = document.getElementById("1").innerHTML = "";
    a2 = document.getElementById("2").innerHTML = "";
    a3 = document.getElementById("3").innerHTML = "";
    a4 = document.getElementById("4").innerHTML = "";
    a5 = document.getElementById("5").innerHTML = "";
    a6 = document.getElementById("6").innerHTML = "";
    a7 = document.getElementById("7").innerHTML = "";
    a8 = document.getElementById("8").innerHTML = "";
    a9 = document.getElementById("9").innerHTML = "";
    document.querySelector(".write").innerHTML = "";
  });

	 }

	 restart();



  </script>

</html>

Author - Priyanshu
