# Tarea03-Proyecto-Funcional
Patrones Empleados en el Sistema Actual

--------- Strategy Pattern ------------
Qué hace: Permite definir múltiples algoritmos (en este caso, métodos de pago) y seleccionarlos en tiempo de ejecución de forma intercambiable.
//Clases involucradas:
MetodoPago (clase abstracta que define la operación procesarPago)
PagoTarjeta (implementación concreta de un método de pago)
PagoEfectivo (otra implementación concreta de un método de pago)
ProcesoPago (utiliza un objeto de tipo MetodoPago para delegar el procesamiento del pago)

--------- Repository Pattern ---------
Qué hace: Abstrae el acceso a la fuente de datos (en este caso, archivos de texto) y encapsula la lógica para cargar, guardar, agregar, eliminar y buscar información.
//Clases involucradas:
RepositorioUsuariosArchivo (para cargar y guardar la información de los usuarios)
RepositorioFuncionesArchivo (para cargar y guardar la información de las funciones)
RepositorioSalasArchivo (para cargar, agregar, eliminar y buscar salas en un repositorio central)

----------- Facade Pattern --------
Qué hace: Ofrece una interfaz de alto nivel que oculta la complejidad de subsistemas más detallados.
//Clases involucradas:
Cine
La clase principal actúa como fachada del sistema, coordinando el acceso a la persistencia, la gestión de funciones, salas, procesos de pago y notificaciones.

-------- Singleton-like Behavior (Mediante uso de métodos y variables estáticas) -------
Qué hace: Garantiza que haya una única instancia o punto de acceso a ciertas funcionalidades en todo el sistema, sin necesidad de crear múltiples instancias.
//Clases involucradas:
RepositorioSalasArchivo
Al manejar internamente una lista estática y métodos estáticos para cargar, guardar y buscar salas, se simula un repositorio único y centralizado de salas.

--------- Adapter/Wrapper (Simplificado) --------
Qué hace: Encapsula el uso de una librería o API (en este caso, Swing para la interfaz gráfica) para ofrecer una interfaz más sencilla al resto del sistema.
//Clases involucradas:
CuentaRegresivaGUI
Aunque no se ha implementado un Adapter completo, la clase encapsula la lógica de la cuenta regresiva con Swing, lo que permite que el proceso de pago simplemente 
actualice el tiempo sin preocuparse por la implementación interna de Swing.


Strategy, Repository, Facade, Singleton (a través de métodos estáticos) y un Adapter/Wrapper para la interfaz gráfica.