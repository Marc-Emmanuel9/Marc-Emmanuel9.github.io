# Write Up At0M - Root Me

## Description du challenge - Javascript - Authentication 2

Aucune information 

## Solution

Le challenge root-me commence sur le site : <b><u>http://challenge01.root-me.org/web-client/ch11/</u></b>.

On arrive alors sur le site suivant :

![Image](https://marc-emmanuel9.github.io/Root%20Me/WEB%20-%20Client/Javascript%20-%20Authentication%202/Ressources/Photo_site.jpg)

J'ai decidé d'aller jetter un coup d'oeil dans l'inspecteur d'élément (Sources).

On a les code suivant :

```html
<html>
    <head>
	    <title>JS Authentication</title>
	    <script language="JavaScript" src="login.js"></script>
    </head>
    <body><link rel='stylesheet' property='stylesheet' id='s' type='text/css' href='/template/s.css' media='all' /><iframe id='iframe' src='https://www.root-me.org/?page=externe_header'></iframe>
	    <div id=EchoTopic>
	        <p>Authentication</p>
	        <p><input type="button" value="login" onclick="connexion();"></p>
	        <br/><br/>
	        <a href="javascript:window.close();">Close Window</a>
	    </div>
    </body>
</html>
```

```javascript
function connexion(){
    var username = prompt("Username :", "");
    var password = prompt("Password :", "");
    var TheLists = ["GOD:HIDDEN"];
    for (i = 0; i < TheLists.length; i++)
    {
        if (TheLists[i].indexOf(username) == 0)
        {
            var TheSplit = TheLists[i].split(":");
            var TheUsername = TheSplit[0];
            var ThePassword = TheSplit[1];
            if (username == TheUsername && password == ThePassword)
            {
                alert("Vous pouvez utiliser ce mot de passe pour valider ce challenge (en majuscules) / You can use this password to validate this challenge (uppercase)");
            }
        }
        else
        {
            alert("Nope, you're a naughty hacker.")
        }
    }
}

```

En analysant bien le code on remarque que ...


`Le flag est : HIDDEN`

-------------
[Page précedente](https://marc-emmanuel9.github.io/Root%20Me/)