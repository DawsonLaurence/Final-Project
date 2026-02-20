<!DOCTYPE html>
<html>
<head>
<title>BotW Guide Login</title>
<style>
  body {
    padding-left: 700px;
	padding-top: 300px;
	padding-bottom 2px;
    height: 100vh;
    font-family: sans-serif;
    background-color: #ffffff;
    align-items: center;
    justify-content: center;
    color: #d7fff4;
	text: align-center;
  }
  #register-form {
	background-color: #464646;
	align-items: center;
    padding: 2rem;
    border-radius: 12px;
    width: 280px;
    text-align: center;
	display: inline-block;
  }
  #login-form {
    background-color: #464646;
    padding: 2rem;
    border-radius: 12px;
    width: 280px;
    text-align: center;
	display: none;
	align-items: center;
  }
  h1 {
    margin-bottom: 1rem;
    letter-spacing: 2px;
  }
  input {
    width: 100%;
    padding: 10px;
    margin: 0.5rem 0;
	border: none;
    border-radius: 6px;
    background: #0e4b47;
    color: #d7fff4;
  }
  button {
    width: 100%;
    padding: 10px;
    margin-top: 1rem;
    background: #2fffd5;
    color: #003330;
    font: bold;
  }
  button:hover {
    background: #8ffff0;
  }
  .msg {
    font-size: 0.85rem;
    color: #ffbdbd;
  }
  #menu {
	display: none;
	color: black;
  }
</style>
</head>
<body>
<form id="register-form">
  <h1>BotW Guide Register</h1>
  <input id="user-register" placeholder="Traveler Name">
  <input id="pass-register" type="password" placeholder="Sheikah Slate Key">
  <button type="submit" >Enter Hyrule</button>
  <div class="msg-register" id="msg-register"></div>
  <button onclick="ermLogin()"> Login Here </button>
</form>
<form id="login-form">
  <h1>BotW Guide Login</h1>
  <input id="user-login" placeholder="Traveler Name" required>
  <input id="pass-login" placeholder="Sheikah Slate Key" required>
  <button type="submit" >Enter Hyrule</button>
  <div class="msg-login" id="msg-login"></div>
</form>
<div id="menu" class="menu"> 
	<h1> Welcome to Hyrule! </h1>
	<h4> Please pick which topic you wish to learn about! </h4>
	<ul> 
		<li> <button type="submit"> Thing1 </button> </li>
		<li> <button type="submit"> Thing2 </button> </li>
		<li> <button type="submit"> Thing3 </button> </li>
		<li> <button type="submit"> Thing4 </button> </li>
		<li> <button type="submit"> Thing5 </button> </li>
	</ul>
<script>
	function ermLogin() {
		document.querySelector("#register-form").style.display = "none";
		document.querySelector("#login-form").style.display = "inline-block";
	}
	function checkPassword(ul,pl) {
	  return localStorage.getItem("username") == ul && localStorage.getItem("password") == pl;
	}
	function showMsgRegister(m) {
		const msg = document.getElementById("msg-register");
		msg.textContent = m;
	}
	function showMsgLogin(m) {
		const msg = document.getElementById("msg-login");
		msg.textContent = m;
	}
	function login(){
		const ul = document.querySelector("#user-login").value;
		const pl = document.querySelector("#pass-login").value;
		if (checkPassword(ul,pl)) {
		document.querySelector("#login-form").style.display = "none";
		document.querySelector("#menu").style.display = "inline-block";
		} else {
		showMsgLogin("Sheikah Slate denied. Please enter the correct password.");
		}
	}
	function register() {
		localStorage.setItem("username", document.querySelector("#user-register").value);
		localStorage.setItem("password", document.querySelector("#pass-register").value);
		showMsgRegister("Sheikah Slate added. Please login with your new password.");
	}	
	const form1 = document.getElementById("login-form");
	const form2 = document.getElementById("register-form");
	form1.addEventListener("submit", function(event) {
		const form1 = document.getElementById("login-form");
		event.preventDefault(); // Prevents the page from reloading
		login();
	});
	form2.addEventListener("submit", function(event) {
		const form2 = document.getElementById("register-form");
		event.preventDefault(); // Prevents the page from reloading
		register();
	});
</script>
</body>
</html>
