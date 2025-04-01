# HuskyLens y Raspberry Pi Pico

Vamos a controlar las [HuskyLens](https://www.dfrobot.com/product-1922.html) desde un [Raspberry Pi Pico](https://www.raspberrypi.com/products/raspberry-pi-pico/) usando [MicroPython](https://micropython.org/).

Suponemos que...
1. Tenemos actualizada el firmware de la HuskyLens 
2. La Pico tiene instalado su firmware de MicroPython .
3. Tenemos instalado en el PC el entorno de programación de python [Thonny](https://thonny.org)

Ahora vamos con la conexión del montaje

1. Conectamos la Raspberry Pi Pico con las HuskyLens, ambas apagadas, siguiendo el esquema y utilizando los cables que incluyen las HuskyLens (hemos utilizado los colores de los cables de nuestras HuskyLens). Las HuskyLens no estarán conectadas al USB, se alimentan desde la Pico

![Pico-Husky](./images/Pico-Husky.png)

| HuskyLens | Raspberry Pi Pico |
| --------- | ----------------- |
| Vcc       | 3.3V              |
| GND       | GND               |
| SDA       | GPIO6 (SDA)       |
| SCL       | GPIO7 (SCL)       |

![](images/Esquema_montaje_huskyLens_Pico.png)

2. Conectamos el cable USB de la Pico a tu PC.

Si todo ha ido bien las HuskyLens se encenderán. Ahora vamos a memorizar la cara que queremos reconocer. 
1. Enfocamos la cámara a la cara que queremos memorizar y pulsamos el botón 
2. Aparecerá identificada como ID:1
3. Si queremos memorizar más caras sólo tenemos que seguir el proceso que ya vimos

Ahora vamos con la programación:
1. Descarga la [librería y el código](https://github.com/javacasm/Pico-HaskyLens/archive/refs/heads/main.zip) (es algo largo para copiarlo a mano)
2. Descomprime el fichero zipPasted%20image%2020250401185147
3. Abre la ventana Archivos de Thonny, con la opción "Visualizar -> Archivos"
![](./images/thony_ver_archivos.png)
4. Apunto la ventana al directorio donde has descomprimido el archivo Zip
![](./images/selecciona_directorio_codigo.png)
5. Marca los ficheros ".py" y seleccionamos la opción "Subir a /" con lo que se enviarán a la Pico
![](./images/enviar_codigo_pico.png)

6. Si todo ha ido bien tendremos los fichero en la Pico
![](images/ficheros_codigo_pico.png)

7. Abrimos el código fichero test_1_pyhuskyLens.py en Thonny
8. Pulsamos "Ejecutar"
![](images/run_tests.png)
9. En la HuskyLens aparecerá el mensaje "Hola, soy la Pico"
![](images/Hola_soy_Pico.png)
10. Cuando reconozca una cara se encenderá el LED de la placa

## Reconocimiento


Módulo y ejemplos basados en [este repositorio](https://github.com/antonvh/PyHuskyLens/)