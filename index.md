```html
<html>
<head>
<style></style>
</head>
<body>

<script>
function rnd(min, max){
	return Math.floor(Math.random() * (max - min) ) + min;	
}

var firstNameArr = ["James","John","Robert","Mary","Patricia","Jennifer","Michael","William","David","Linda","Elizabeth","Barbara","Richard","Joseph","Thomas","Susan","Jessica","Sarah","Charles","Karen","Christopher","Nancy","Daniel","Lisa","Matthew","Margaret","Anthony","Betty","Donald","Sandra","Mark","Ashley","Paul","Dorothy","Steven","Kimberly","Andrew","Emily","Kenneth","Donna","Joshua","Michelle","Kevin","Carol","Brian","Amanda","George","Melissa","Edward","Deborah","Cum","Obama","Flynn","Walter","Jonathan","Nathan","Tyler","Justin","Travis","Abel","Tom"];
var lastNameArr  = ["Smith","Johnson","Anderson","Miller","Garcia","Hernandez","Lopez","Anderson","Martinez","Chavez","Olson","Williams","Nelson","Jones","Black","White","Barrett","Sullivan","Brown","Obama","Jefferson","Adams","Lee","Wong","Kim","Lincoln","Cum","Shitass","McCarthy","Kelly","Murphy","Ryan","O'Sullivan","Flynn","Scott","Scallion","Bruh"];

function lineNum(n){
	var numArr = new Array(n);
	numArr[0] = rnd(0,10);
	
	for (var i = 1; i<=n; i++) {
		numArr[i] = numArr[i-1] + rnd(0,15);
	}
	globalNumArr = numArr;
	document.getElementById("bruh").innerHTML = writeBullshit();
}


function writeBullshit(){
	var string = "";
	for (var i = 0; i<globalNumArr.length; i++){
		string = string + "Line " + globalNumArr[i] + ":found dead voter:firstname:" + firstNameArr[rnd(0,firstNameArr.length)].toUpperCase() + " lastname: " + lastNameArr[rnd(0,lastNameArr.length)].toUpperCase() + " year:19" + rnd(10,50) + " zipcode:8" + (rnd(8,10)*1000+rnd(0,199)) + " month " + rnd(1,12) + "<br/>"
	}
	return string;
}

</script>

<input type="number" id="num" value="50">
<button onclick="lineNum(document.getElementById('num').value)">FIND DEAD VOTERS ! ! !</button>
</input>

<p id="bruh"></p>

</body>
</html>
```
