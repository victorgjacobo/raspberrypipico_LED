# Raspberry pi pico y LED

## Materiales
- Raspberry pi pico
- Protoboard
- Diodo LED
- Resistencias de 330 Ohms
- Jumpers 

## Descripción
En la figura observamos la conexión de la raspberry pi pico con el LED.  El diodo LED está conectado al `GPIO 0` el cual está configurado como salida `Pin.Out` y al mismo tiempo tomamos el led que incorpora la raspberry pi pico habilitando el `GPIO 25`.  Es importante aclarar que la resistencia de 330 Ohms que va conectada al LED sirve de protección.

![primera_practica](https://github.com/victorgjacobo/raspberrypipico_LED/assets/141197135/10f76230-405d-470a-87af-f9cf7885c46c)

## Código
```python
"""
  Nombre de la práctica: Prender y apagar un led con un retardo
  Microcontrolador Raspberry Pi Pico 
  Autor: Ing. Víctor González Jacobo
  Módulo: GPIO
"""
from machine import Pin
import utime

### Declaración de los pines físicos
LED = Pin(0, Pin.OUT)

estado = 0

def main():
    print("Inicio del programa")
    while True:
        LED.toggle()
        estado = LED.value()
        if estado == 1:
            print("Encendido")
        else:
            print("apagado")
        utime.sleep(1)

if __name__ == '__main__':
    main()
```

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Raspberry Pi](https://img.shields.io/badge/-RaspberryPi-C51A4A?style=for-the-badge&logo=Raspberry-Pi)
![]( https://img.shields.io/github/followers/victorgjacobo)
![](https://img.shields.io/github/stars/victorgjacobo/raspberrypipico_LED)
![](https://img.shields.io/github/watchers/victorgjacobo/raspberrypipico_LED)
