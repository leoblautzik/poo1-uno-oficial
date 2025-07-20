# Polimorfismo

## Ejercicios

1. En el método main de la clase TestInterface declarar un arreglo de N figuras (Interface). Las figuras pueden ser cuadrados, círculos y rectángulos. Todos responden al mensaje area. Mostrar en consola el siguiente mensaje: "De un total de N figuras, el área total es de ..."

    ![Interface Figura](img/interface1.png)

1. Dada la siguiente jerarquia de clases:
    * Sociedad Anónima es una Sociedad
    * SRL es una Sociedad
    * SH es una Sociedad
    * Datos comunes: denominación social, domicilio legal, capital social, CUIT
    * Datos adicionales según el tipo de sociedad:
        * Sociedad Anónima: cantidad de acciones, precio de cada acción, cotiza en bolsa (s/n), cantidad de directores
        * SRL: nombre de socios gerentes (máximo 3), patrimonio personal de cada socio gerente, cantidad de socios no gerentes
        * SH: lista de los nombres de los socios, porcentaje de participación de cada socio
    * Considerar que siempre una sociedad debe corresponder a algún tipo específico. Escribir los constructores y los métodos necesarios y adecuados. Escribir un programa usando el concepto de polimorfismo que muestre en pantalla toda la información disponible de una sociedad. Escribir un método (y usarlo en el programa) que permita comparar el capital de dos sociedades

1. Un Video Club pone a disposición de sus socios series, películas y videojuegos
    1. Crear una clase llamada Película con las siguientes características:
        * Sus atributos son título, año, entregado, género y director
        * Por defecto, el género es "no definido" y entregado false. El resto de atributos serán valores por defecto según el tipo del atributo
        * Los constructores que se implementarán serán:
            * Un constructor por defecto
            * Un constructor con el título y director. El resto por defecto
            * Un constructor con todos los atributos, excepto de entregado
        * Los métodos que se implementara serán:
            * Métodos get de todos los atributos, excepto de entregado
            * Métodos set de todos los atributos, excepto de entregado
            * Sobrescribe los métodos toString
    1. Crear una clase llamada Serie con las siguientes características:
        * Sus atributos son título, número de temporadas, entregado, género y creador
        * Por defecto, el número de temporadas es de 3 temporadas y entregado false. El resto de atributos serán valores por defecto según el tipo del atributo
        * Los constructores que se implementarán serán:
            * Un constructor por defecto
            * Un constructor con el título y creador. El resto por defecto
            * Un constructor con todos los atributos, excepto de entregado
        * Los métodos que se implementara serán:
            * Métodos get de todos los atributos, excepto de entregado
            * Métodos set de todos los atributos, excepto de entregado
            * Sobrescribe los métodos toString
    1. Crear una clase Videojuego con las siguientes características:
        * Sus atributos son título, horas estimadas, entregado, género y compañía
        * Por defecto, las horas estimadas serán de 10 horas y entregado false. El resto de atributos serán valores por defecto según el tipo del atributo
        * Los constructores que se implementarán serán:
            * Un constructor por defecto
            * Un constructor con el título y horas estimadas. El resto por defecto
            * Un constructor con todos los atributos, excepto de entregado
        * Los métodos que se implementara serán:
            * Métodos get de todos los atributos, excepto de entregado
            * Métodos set de todos los atributos, excepto de entregado
            * Sobrescribe los métodos toString
    1. Hacer una interface llamada Entregable con los siguientes métodos:
        * entregar(): cambia el atributo prestado a true
        * devolver(): cambia el atributo prestado a false
        * isEntregado(): devuelve el estado del atributo prestado
        * compareTo (Object a), compara las horas estimadas en los videojuegos y en las series el número de temporadas. y en las películas el año
    1. Crear una aplicación ejecutable que haga lo siguiente:
        * Crea tres arrays, uno de Películas, otro de Series y otro de Videojuegos
        * Crea un objeto en cada posición del array, con los valores que desees, puedes usar distintos constructores
        * Entrega algunos Videojuegos y Películas y Series con el método entregar()
        * Cuenta cuantas Películas Series y Videojuegos hay entregados. Al contarlos, devuelvelos
        * Por último, indica que Videojuego tiene más horas estimadas, la serie con más temporadas y la Película más antigua. Muéstralos en pantalla con toda su información (usa el método toString())

1. Definir las clases VehiculoCliente, VehiculoAbonado y VehiculoHotel. Estas clases deben implementar la interfaz Vehículo cuyos datos son una cadena de texto id y un valor entero tiempo
    * La cadena de texto funciona como identificador del vehículo y es inmutable. El valor entero almacena el número de horas, días o meses dependiendo del tipo de vehículo. La clase VehiculoCliente deberá tener constructores y métodos set y get. El valor inicial para tiempo es 0
    * Deberá realizar el método factura() que determina lo que tiene que abonar un objeto del tipo VehiculoCliente por su estancia en el garaje. El costo de la permanencia es de $12 el día completo y $0.6 la hora o fracción. El método hayPlaza() que determina si hay lugar en el garaje para estacionar un objeto del tipo VehiculoCliente
    * La clase VehiculoAbonado tiene los datos id y tiempo que en este caso representa un numero de meses, debe contener constructores y los métodos factura() que determina lo que debe abonar un objeto del tipo VehiculoAbonado, el costo de la estancia es de $200 por mes y hayPlaza() igual que en el caso anterior
    * En la clase VehiculoHotel el tiempo se mide en días. El costo es de $10 por día

1. Definir la clase Vehículo como clase base de las clases derivadas VehiculoTerrestre, VehiculoAereo, VehiculoAcuatico. A la clase VehiculoYerrestre adicionarle dos clases hijas: VehiculoCarretera y VehiculoVias. Detallar las variables miembros de cada una y los métodos que correspondan

1. Se debe crear una pequeña orquesta de cámara que pueda ofrecer información de si misma. Se deberán definir las siguientes clases:
    * Clase abstracta Instrumento. Atributos: nombre, precio. Método: abstract void afinar(). Variable estática: numeroInstrumentos
    * Clase Viento. Variables miembro estáticas: numInstrVientoMetal y numInstrVientoMadera. Método: boolean esDeMetal()
    * Clase Percusion. Variable miembro estática: numInstrPercusion
    * Clase Cuerda. Variable miembro estática: numInstrCuerda
    * Además, se debe crear la interface Identificable con el método String queInstrumentoEres(). Esta interface deberá ser implementada por todas las clases descendientes de Instrumento. El método afinar() deberá emitir “de alguna manera” el sonido propio del instrumento

1. Se pide escribir un programa de gestión bancaria. Para ello se crearán dos clases, las que se detallan a continuación:
    * Una clase Cuenta con 4 atributos: Número de cuenta (long), el cual debe ser único. Nombre del propietario de la cuenta (String). Saldo actual (double). Interés que se aplica a esa cuenta (double). Esta clase debe implementar la interface Salida que tiene un único método imprimirCuenta(), que debe mostrar en pantalla el saldo actual de la cuenta y sus datos. La clase Cuenta deberá tener el método actualizarSaldo() que actualizará el saldo de la cuenta aplicándole el interés. Además, deberá tener los métodos constructores
    * La clase Banco que contendrá una lista de cuentas, con 4 métodos: crearCuenta() para agregar una nueva cuenta a la lista. Se deberá verificar que no exista otra cuenta con ese número. ActualizarCuentas() que aplicará el interés apropiado a cada una de las cuentas existentes usando el método actualizarSaldo() de la clase Cuenta. MostrarCuentas(), mostrará los extractos de cada cuenta. BorrarCuenta(), que permitirá borrar una cuenta dado el número de cuenta
    * El programa principal deberá mostrar un menú de opciones: crear, borrar, actualizar, mostrar y salir, y deberá permitir el ingreso de la opción

1. Modelar, desarrollar y probar las distintas unidades de un juego de estrategia. Del juego participan las siguientes Unidades: Soldados, Arqueros, Lanceros y Caballeros. Reglas del juego:
    * Los soldados pueden atacar cuerpo a cuerpo a otras unidades si tienen suficiente energía. Cada ataque les consume 10 puntos de energía, y comienzan con 100. Restauran energía si reciben la ración de agua. Infringen un daño de 10 puntos y comienzan con 200 de salud
    * Los Arqueros pueden atacar a una distancia de entre 2 y 5 respecto de su enemigo, y si tienen suficientes flechas. Comienzan con 20 flechas en su carcaj, y pueden recargar si reciben un paquete de seis flechas. Infringen un daño de 5 puntos, y comienzan con 50 de salud
    * Los lanceros pueden atacar a una distancia de 1 a 3, sin condición. Infringen un daño de 25 puntos, y comienzan con 150 de salud
    * Los caballeros pueden atacar a una distancia de 1 a 2, siempre que su caballo no se haya puesto rebelde. Infringe un daño de 50 puntos y comienza con 200 de salud. Un caballo se pone rebelde luego de 3 ataques, y puede calmarse si recibe una ración de agua
    * Ninguna unidad muerta puede atacar, por supuesto
