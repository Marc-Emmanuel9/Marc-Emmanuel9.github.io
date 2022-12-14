# Write Up At0M - Root Me

## Description du challenge - Encoding - ASCII

Decode the string.

## Solution

### Introduction 

### Première solution - [CyberChef](https://gchq.github.io/CyberChef/)

Il nous suffit de copier-coller la chaine dans CyberChef : <b>4C6520666C6167206465206365206368616C6C656E6765206573743A203261633337363438316165353436636436383964356239313237356433323465</b>

![Image](https://marc-emmanuel9.github.io/Root%20Me/Cryptanalysis/Encoding%20-%20ASCII/Ressources/PhotoChef.jpg)

On obtient alors : <b>Le flag de ce challenge est: 2ac376481ae546cd689d5b91275d324e</b>

Le flag pour valider le challenge est : <b>2ac376481ae546cd689d5b91275d324e</b>

### Deuxième solution - Faire un script

Voici un script python simple permettant d'arriver à la même solution :

```python
chain = "4C6520666C6167206465206365206368616C6C656E6765206573743A203261633337363438316165353436636436383964356239313237356433323465"
flag = bytes.fromhex(chain).decode("ASCII")
print(flag)
```

On obtient alors en sortie du code : <b>Le flag de ce challenge est: 2ac376481ae546cd689d5b91275d324e</b>

Le flag pour valider le challenge est : <b>2ac376481ae546cd689d5b91275d324e</b>

-------------
[Page précedente](https://marc-emmanuel9.github.io/Root%20Me/)