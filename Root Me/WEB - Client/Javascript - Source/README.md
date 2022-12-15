# Write Up At0M - Root Me

## Description du challenge - Javascript - Source

Aucune information 

## Solution

Le challenge root-me commence sur le site : <b><u>http://challenge01.root-me.org/web-client/ch1/</u></b>.

On arrive alors sur le site suivant :

![Image](https://marc-emmanuel9.github.io/Root%20Me/WEB%20-%20Client/Javascript%20-%20Source/Ressources/Photo_site.jpg)

J'ai decidé d'aller jetter un coup d'oeil dans l'inspecteur d'élément (Sources).

On a le code suivant :
```html
<html>
    <head>
	<script type="text/javascript">
	/* <![CDATA[ */
	    function login(){
		    pass=prompt("Entrez le mot de passe / Enter password");
		    if ( pass == "123456azerty" ) {
		        alert("Mot de passe accepté, vous pouvez valider le challenge avec ce mot de passe.\nYou can validate the challenge using this password.");
            }
		    else {
		        alert("Mauvais mot de passe / wrong password !");
		    }
	    }
	/* ]]> */
	</script>
    </head>
    <body onload="login();"><link rel='stylesheet' property='stylesheet' id='s' type='text/css' href='/template/s.css' media='all' /><iframe id='iframe' src='https://www.root-me.org/?page=externe_header'></iframe>

    </body>
</html>
```

On remarque que dans le code js le mot de passe est directement affiché en clair.

`Le flag sera : <b>123456azerty</b>`

-------------
[Page précedente](https://marc-emmanuel9.github.io/Root%20Me/)