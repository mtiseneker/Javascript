# Javascript
let Button = document.getElementById('mySubmit');
Button.addEventListener('click', function(e){
    e.preventDefault();
    game();}, false);
	var i=0;
	var j=0;
	
//game function
//random numbers and submit buttons
//tracks number of wins 
function game(x, y){
	
	var x;
	var y;
	
	x= Math.floor(Math.random() * 10) +1;
	y= Math.floor(Math.random() * 10) +1;
	
	document.getElementById("hum").value = x;
	document.getElementById("comp").value = y;
 
	
	
	if(x>y)
		{
			
			i ++;
			document.getElementById("Whum").innerHTML = i;
		}
	else{
		
		j ++;
		document.getElementById("Wcomp").innerHTML = j;
	}
	
}


//code for digital clock
//based on current  military time 
function Clock() {
  
	var date = new Date();
  
	var h = date.getHours();
  	var m = date.getMinutes();
  	var s = date.getSeconds();
  
	m = checkTime(m);
 	s = checkTime(s);
  
	var time = h + ":" + m + ":" + s;
	document.getElementById("clock").innerHTML = time;
	
	setTimeout(Clock, 1000);
	
}

function checkTime(num) {
  if (num < 10) 
  {
	  num = "0" + num;
  } 
  return num;
}

Clock();
