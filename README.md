
# **Parcial domiciliario:** Sistemas de procesamiento de datos

![Tinkercad](./Img/ArduinoTinkercad.jpg)
## *Division E*

## **Integrantes:**
- Nicolás Gastón Larrochi
- Franco Martin Mancilla
- Valeria Barrera

## **Parte 1: Contador de 0 a 99 con Display 7 Segmentos y Multiplexación**

![Tinkercad](./Img/Parcial%201.%201-E.%20Larrochi%20Nicol%C3%A1s%20Gast%C3%B3n.png)

## Descripción

Este contador de 0 a 99 creado con dos displays de 7 segmentos, contiene 3 pulsadores y está inicializado en 0.

El primer pulsador se encarga de resetea el contador en 0.
El segundo pulsador se encarga de sumar 1 el contador.
El tercer pulsador se encarga de restar 1 el contador.

## Función principal

Esta función se encarga de hacer funcionar los displays con el método de la multiplexación, prendiendo/mostrando y apagando entre cada display, logrando que muestre a la vez la unidad y decena.

```c+
 void printCount(int count) // Imprime el num obtenido del contador
                           // Utilización de multiplexación para que muestre ambos displays
{
  prendeDigito(APAGADOS);  // Apaga todos
  printDigit(count/10);  // Toma el valor de la decena 
  prendeDigito(DECENA);  // Prende display decena
  prendeDigito(APAGADOS); // Apaga todos
  printDigit(count - 10 * ((int)count/10)); // Toma el valor de la unidad
  prendeDigito(UNIDAD); // Prende display unidad          
}  
``` 

## Link al proyecto

- [Tinkercad - Parte 1](https://www.tinkercad.com/things/fetWNTi0TVU?sharecode=T-MGLzgRG0ofzq09FHtvedgoTW_YTNKws7TqGVk4iJY)
