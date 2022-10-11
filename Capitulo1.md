
> Un analizador de red se obtenienen archivos `.pcap`, otro herramienta analizadora de red es `tcpdump`. Y ambos estan desarrollados encima de una librería en C `libcap`.

A travez de `tcpdump` se logra obtener datos en bruto del tráfico de red.

## TCP stat
Cuando se captura paquetes se logra encontrar estadisticos a travez de `TCP stat`.

> Ejemplo: Para 100 paquetes, y 100 bytes cada paquete que se envia en 10 segundos.

$$
(100*100*8)/10 = 8kbps
$$

Para instalar la utilidad:

```
sudo apt-get install tcpstat
```

En la clase se debe utilizar `tcpdump`.

```
tcpstat -r file.pcap interval
```

- `r`: Read
- `interval`: Intervalo de tiempo

## Practica 1:

### Analisis del Perfil del Trafico Multimedia mediante Tcpstat

1. Instalar tcpstat y tcpdump.
2. Realizar una captura de trafico durante una videoconferencia (con audio y video).
3. Direccionamos el resultado de la captura con `tcpdump` a un fichero `.pcap`.
4. Emplee `tcpstat` para procesar el fichero `.pcap` con diferentes intervalos de analisis 1 segundo y 0.1 segundos y 0.01 segundos.


```
tcpstat -i wlan 0
```

Que filtro utilizar para saber cual es el ideal para enviar y recibir.
