# Write Up At0M - Root Me

## Description du challenge - HTML - Source code

Aucune information 

## Solution

Le challenge root-me commence sur le site : <b><u>http://challenge01.root-me.org/web-serveur/ch1/</u></b>.

On arrive alors sur le site suivant :

![Image](https://marc-emmanuel9.github.io/Root%20Me/WEB%20-%20Serveur/HTML%20-%20Source%20code/Ressources/Photo_site.jpg)

J'ai decidé d'aller jetter un coup d'oeil dans l'inspecteur d'élément (Sources).

On a le code suivant :

```html
<html>
    <head>
        <link rel='stylesheet' property='stylesheet' id='s' type='text/css' href='/template/s.css' media='all' />
        <iframe id='iframe' src='https://www.root-me.org/?page=externe_header'></iframe>
    </head>

    <body>
        <!--

        Bienvenue sur ce portail,
        Welcome on this portal,

        J'espère que vous passerez un agréable moment parmi nous, mais surtout que vous repartirez plein de choses dans la tête...
        I hope that you will enjoy your time among us, and above that all you will leave with lots of things in the head ...

        @ très bientôt
        See ya

        -->
        <h1>Login v0.00001</h1>

        <form>
            Password&nbsp;<input type="password" value="" name="password"/><br/>
            <input type="submit" value="login" />
        </form>
        <h4>Mot de passe incorrect / Incorrect password</h4>

        <!--
        Je crois que c'est vraiment trop simple là !
        It's really too easy !
        password : nZ^&@q5&sjJHev0
        -->
    </body>
</html>
```

`Le flag de ce challenge est : nZ^&@q5&sjJHev0`

-------------
[Page précedente](https://marc-emmanuel9.github.io/Root%20Me/)