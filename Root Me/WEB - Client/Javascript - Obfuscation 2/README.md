# Write Up At0M - Root Me

## Description du challenge - Javascript - Obfuscation 2

Aucune information 

## Solution

Le challenge root-me commence sur le site : <b><u>http://challenge01.root-me.org/web-client/ch12/ch12.html</u></b>.

On arrive alors sur une page blanche.

J'ai decidé d'aller jetter un coup d'oeil dans l'inspecteur d'élément (Sources).

On a le code suivant :

```html
<html>
    <head>
	    <title>Obfuscation JS</title>
        <!-- 
        Obfuscation 
        .Niveau : Facile 
        .By Hel0ck
        .The mission : 
	    Retrouver le password contenu dans la var pass.
	    You need my help ? IRC : irc.root-me.org #root-me
        -->
        <script type="text/javascript">
	        var pass =  unescape("unescape%28%22String.fromCharCode%2528104%252C68%252C117%252C102%252C106%252C100%252C107%252C105%252C49%252C53%252C54%2529%22%29");
        </script>
    </head>
</html>
```

Pour comprendre le contenue de la variable `pass` decortiquons le :
* unescape : La fonction dépréciée unescape() calcule une nouvelle chaîne de caractères et remplace les séquences d'échappement hexadécimales par les caractères qu'elles représentent.
* %28%22 : en décodage d'URL représente -> `("`
* String.fromCharCode : La méthode statique String.fromCharCode() renvoie une chaîne de caractères créée à partir de points de code UTF-16. EX : `String.fromCharCode(189, 43, 190, 61) = ½+¾=`
* %2528 : en décodage d'URL représente -> `(`
* %252C : en décodage d'URL représente -> `,`
* %22%29 : en décodage d'URL représente -> `")`
* %25%29 : en décodage d'URL représente -> `)`

Si on remplace tout cela par la bonne valeur on obtiendra :

```javascript
pass = unescape("unescape("String.fromCharCode(104,68,117,102,106,100,107,105,49,53,54)")")
```

En exuctant :

```javascript 
String.fromCharCode(104,68,117,102,106,100,107,105,49,53,54)
```

`On obtient le flag qui est : hDufjdki156`

-------------
[Page précedente](https://marc-emmanuel9.github.io/Root%20Me/)