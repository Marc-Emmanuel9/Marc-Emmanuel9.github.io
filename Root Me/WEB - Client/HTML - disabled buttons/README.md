# Write Up At0M - Root Me

## Description du projet - HTML - disabled buttons

This form is disabled and can not be used. It’s up to you to find a way to use it.

## Solution

Le challenge root-me commence sur le site : <b><u>http://challenge01.root-me.org/web-client/ch25/</u></b>.

On arrive alors sur le site suivant :

![Image](https://marc-emmanuel9.github.io/Root%20Me/WEB%20-%20Client/HTML%20-%20disabled%20buttons/Ressources/Photo_site.jpg)

On a le code suivant :

```html
<html>
    <head>
        <title>Under construction</title>
        <link rel='stylesheet' property='stylesheet' type='text/css' href='style.css' media='all' />
    </head>
   <body><link rel='stylesheet' property='stylesheet' id='s' type='text/css' href='/template/s.css' media='all' /><iframe id='iframe' src='https://www.root-me.org/?page=externe_header'></iframe>
        <h1>Website temporarily closed.</h1>
        <hr>

        <form action="" method="post" name="authform">
            <div>
                <input disabled type="text" name="auth-login" value="" />
                <input disabled type="submit" value="Member access" name="authbutton" />
            </div>
        </form>
    </body>
</html>
```

On remarque assez vite que le formulaire présent sur le site est désactivé avec l'attribut <b>disabled</b>.

>L'attribut booléen disabled, lorsqu'il est présent, rend l'élément non mutable, non focusable, ou même non soumis avec le formulaire. L'utilisateur ne peut ni modifier ni cibler le contrôle, ni les descendants du contrôle de formulaire. Si l'attribut disabled est spécifié sur un contrôle de formulaire, l'élément et ses descendants de contrôle de formulaire ne participent pas à la validation des contraintes. Souvent, les navigateurs grisent ces contrôles et ils ne reçoivent aucun événement de navigation, comme les clics de souris ou les événements liés au focus.

J'ai alors décider de supprimer cette attribut comme ci-dessous :  

```html
<html>
    <head>
        <title>Under construction</title>
        <link rel='stylesheet' property='stylesheet' type='text/css' href='style.css' media='all' />
    </head>
   <body><link rel='stylesheet' property='stylesheet' id='s' type='text/css' href='/template/s.css' media='all' /><iframe id='iframe' src='https://www.root-me.org/?page=externe_header'></iframe>
        <h1>Website temporarily closed.</h1>
        <hr>
        <form action="" method="post" name="authform">
            <div>
                <input type="text" name="auth-login" value="" />
                <input type="submit" value="Member access" name="authbutton" />
            </div>
        </form>
    </body>
</html>
```

On obtient alors un formulaire utilisable :

![Image](https://marc-emmanuel9.github.io/Root%20Me/WEB%20-%20Client/HTML%20-%20disabled%20buttons/Ressources/Photo_champ_actived.jpg)

Après avoir soumis le formulaire (pas besoin de le remplir) on obtient enfin le flag et on peut le valider !

![Image](https://marc-emmanuel9.github.io/Root%20Me/WEB%20-%20Client/HTML%20-%20disabled%20buttons/Ressources/Photo_flag.jpg)

`Le flag pour valider le challenge est : HTMLCantStopYou`

-------------
[Page précedente](https://marc-emmanuel9.github.io/Root%20Me/)