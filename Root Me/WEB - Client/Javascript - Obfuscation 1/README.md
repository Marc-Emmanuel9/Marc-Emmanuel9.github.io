# Write Up At0M - Root Me

## Description du challenge - Javascript - Obfuscation 1

Aucune information 

## Solution

Le challenge root-me commence sur le site : <b><u>http://challenge01.root-me.org/web-client/ch4/ch4.html</u></b>.

On arrive alors sur le site suivant :

![Image](https://marc-emmanuel9.github.io/Root%20Me/WEB%20-%20Client/Javascript%20-%20Authentication%202/Ressources/Photo_site.jpg)

J'ai decidé d'aller jetter un coup d'oeil dans l'inspecteur d'élément (Sources).

On a le code suivant :

 ```html
 <html>
    <head>
        <title>Obfuscation JS</title>

          <script type="text/javascript">
              /* <![CDATA[ */

              pass = '%63%70%61%73%62%69%65%6e%64%75%72%70%61%73%73%77%6f%72%64';
              h = window.prompt('Entrez le mot de passe / Enter password');
              if(h == unescape(pass)) {
                  alert('Password accepté, vous pouvez valider le challenge avec ce mot de passe.\nYou an validate the challenge using this pass.');
              } else {
                  alert('Mauvais mot de passe / wrong password');
              }

              /* ]]> */
          </script>
          <link rel='stylesheet' property='stylesheet' id='s' type='text/css' href='/template/s.css' media='all' />
    </head>
   <body>
        <iframe id='iframe' src='https://www.root-me.org/?page=externe_header'></iframe>
    </body>
</html>
 ```

Le flag de ce challenge sera la variable `pass` présent dans le code.

Le contenu de la variable `pass` est encodé en URL.

>Encodage-pourcent (Percent-encoding) est un mécanisme d'encodage des caractères de 8 bits qui ont une signification spécifique dans le contexte des URL. Il est parfois appelé encodage d'URL. Il consiste en une substitution de : un caractère '%' suivi d'un code hexadecimal correspondant à la valeur ASCII du caractère à remplacer.

Il nous suffit alors de passer la chaîne `%63%70%61%73%62%69%65%6e%64%75%72%70%61%73%73%77%6f%72%64` dans CyberChef pour obtenir `cpasbiendurpassword`.

`Le flag de ce challenge sera alors : cpasbiendurpassword`

-------------
[Page précedente](https://marc-emmanuel9.github.io/Root%20Me/)