Diagrama UML

El sistema está dividido en cinco partes principales:

Product es una clase abstracta que tiene los datos básicos del producto (nombre, precio base y categoría).

De ella heredan Electronics, Clothing y Food, cada una con su propia forma de calcular envío y descripción.

ProductFactory se encarga de crear los productos según el tipo.

PricingStrategy es una interfaz para calcular precios finales.

De ella salen RegularPricing, MemberPricing y BlackFridayPricing, que aplican distintos descuentos.

OrderObserver es una interfaz para notificaciones.

EmailNotifier, SMSNotifier y LogNotifier implementan esa interfaz.

ustificación de los Patrones

Observer:
Lo usé para que cuando el pedido cambie de estado, todos los sistemas de notificación reciban el aviso automáticamente. Así no tengo que programar cada notificación manualmente.

Factory Method:
Lo usé para crear productos sin usar directamente new en el Main. Esto hace que el código esté más organizado y sea más fácil agregar nuevos tipos de producto.

Strategy:
Lo usé para aplicar distintos descuentos sin modificar la clase del producto. Así puedo cambiar la forma de calcular el precio fácilmente.

Instrucciones de Ejecución

Clonar el repositorio.

Abrir el proyecto en NetBeans.

Ejecutar Main.java.

Ver en consola:

Creación de productos

Aplicación de descuentos

Notificaciones cuando cambia el estado del pedid
