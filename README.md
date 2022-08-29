# clase_15
Validación: RegExp


EXPRESIÓN REGULAR: Es una secuencia de caracteres que conforma un patrón de búsqueda.


-Hasta ahora se han estado haciendo validaciones con JS, usando condicionales tal que así:

Travelo Summer:

    /**** Validar nombres ****/
    if (fname.length > 3 && fname.length <= 30) {
        console.log("nombre OK: " + fname);
    }
    else {
        alert("Nombre tiene que que estar entre 3 y 30");
        formValidated = false;
        // Cambios en el DOM para que se vea el error
        //...
        //...
    }

    /**** Validar apellidos ****/
    if (lname.length > 3 && lname.length <= 30) {
        console.log("apellidos OK:" + lname);
    }
    else {
        alert("Apellidos tiene que que estar entre 3 y 30");
        formValidated = false;
        // Cambios en el DOM para que se vea el error
        //...
        //...
    }

    /**** Validar email ****/
    if (email.endsWith(".com")) {
        console.log("apellidos OK:" + lname);
    } else {
        alert("Sólo dominio .com en mi empresa");
        formValidated = false;
        // Cambios en el DOM para que se vea el error
        //...
        //...
    }




-Sin embargo, con RegExp:

    /**** Validar email ****/
        let mailformat = /^\w+([\.-]?\w+)*@\w+([\.-]?\w+)*(\.\w{2,3})+$/;
        if (email.match(mailformat))


-Para comprobar que funciona (testear):

-En la consola del navegador -> mailformat.test('hola@gmail.com') // Devuelve un true si va bien


-Mirar la herramientas en la teoría para crear las RegExp, traducirlas...

-Por ejemplo: En la consola del navegador -> /^hey/.test('hey') devolverá "true", porque significa que el mensaje tiene que empezar por "hey"

-Más ejemplos y teoría: https://flaviocopes.com/javascript-regular-expressions/

https://www.regular-expressions.info/email.html

Muy sencillo buscar en Google...



DÓNDE METER REGEXP:

Validaciones en nuestras apps:
    - Formularios HTML
    - Validación DOM JS --> VanillaJS
    - Back: Recibo petición y compruebo si los campos cumplen la regexp
    - BBDD y compruebo si los campos cumplen la regexp