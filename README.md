# Login-animated-metamask-Moralis
Access animated metamask Moralis - html web design, part 1/10 build nft game.  Follow me on instagram @bigrapb

First part of this edition creating nft game.


We will start with access to metamask using Moralis


follow me https://www.instagram.com/bigrapb/





























INDEX:

<!--
Edit the keys
	Moralis.initialize("APPLICATION_ID"
  Moralis.serverURL = "SERVER_URL"


-->

<html>
  <head>
    <title>Metamask</title>
  <meta charset="UTF-8">
  <title>Login</title>
  <link rel="stylesheet" href="./style.css">
 <link rel="icon" href="https://www.returngis.net/wp-content/uploads/2019/05/logo-metamask-1.png">
</head>
<body>
<-- ------------------------------- -->
<div id="logo-container" style="text-align: center;">&nbsp;</div>
<!-- ------------------------------ -->
  <script  src="./script.js"></script>
	<script src="https://cdn.jsdelivr.net/npm/web3@latest/dist/web3.min.js"></script>
	<script src="https://unpkg.com/moralis/dist/moralis.js"></script>

<h1 class="unlock-page__title" style="text-align: center;"><span style="color: #333333;">HOLA DE NUEVO</span></h1>
<div style="text-align: center;"><span style="color: #999999;"><strong>Conecta con tu cuenta de Metamask</strong></span></div>


<span class="boton" onclick="login()">Login</button>

	<script>
		Moralis.initialize("APPLICATION_ID"); // Application id from moralis.io
		Moralis.serverURL = "SERVER_URL"; //Server url from moralis.io
	
		async function login(){
			console.log("login clicked");
			var user = await Moralis.Web3.authenticate();
			if(user){
				console.log(user);
				user.set("nickname","VITALIK");
				user.set("fav_color","blue");
				user.save();
			}
		}
	
	</script>
  </body>
</html>
