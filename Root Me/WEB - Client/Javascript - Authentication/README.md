# Write Up At0M - Root Me

## Description du challenge - Javascript - Authentication

Aucune information 

## Solution

Le challenge root-me commence sur le site : <b><u>http://challenge01.root-me.org/web-client/ch9/</u></b>.

On arrive alors sur le site suivant :

![Image](https://marc-emmanuel9.github.io/Root%20Me/WEB%20-%20Client/Javascript%20-%20Authentication/Ressources/Photo_site.jpg)

J'ai decidé d'aller jetter un coup d'oeil dans l'inspecteur d'élément (Sources).

On a les code suivant :

```html
<html>
    <head>
        <script type="text/javascript" src="login.js"></script>
    </head>
    <body><link rel='stylesheet' property='stylesheet' id='s' type='text/css' href='/template/s.css' media='all' /><iframe id='iframe' src='https://www.root-me.org/?page=externe_header'></iframe>
        <fieldset style="margin-top: 10px; padding: 10px;" width="60%">
	    <legend><b>Login</b></legend><br/>
	    <form name="login" method="POST" action="">
	        Username : <input name="pseudo" /><br/>
	        Password : <input type="password" name="password" /></br></br>
	        <input onclick="Login()" type="button" value="login" name="button" />
	    </form>
        </fieldset>
    </body>
</html>
```

```javascript
/* <![CDATA[ */

function Login(){
	var pseudo=document.login.pseudo.value;
	var username=pseudo.toLowerCase();
	var password=document.login.password.value;
	password=password.toLowerCase();
	if (pseudo=="4dm1n" && password=="sh.org") {
	    alert("Password accepté, vous pouvez valider le challenge avec ce mot de passe.\nYou an validate the challenge using this password.");
	} else { 
	    alert("Mauvais mot de passe / wrong password"); 
	}
}
/* ]]> */ 
```

On remarque que dans le code js les credentials sont directement affiché en clair.

`Le flag sera : sh.org`

-------------
[Page précedente](https://marc-emmanuel9.github.io/Root%20Me/)