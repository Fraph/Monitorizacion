# Procesos
#### En este documento hablaremos sobre los diversos comandos que podemos usar frente a la monitorizacion de tareas y usuarios
---
# PS
Comandos de ps y sus opciones


![ps](https://img.shields.io/badge/ps-au-blue)


```
ps au
```
Presenta una lista de los procesos que se estan ejecutando en el momento en el que se escribe el comando. Incluyendo el usuario y el PID.

![psau](img/psau.png)

---

![ps](https://img.shields.io/badge/ps-aux-blue)




```
ps aux
```
Como el anterior pero incluyendo todos los procesos ejecutandose en el sistema.
![psaux](img/psaux.png)

---

![ps](https://img.shields.io/badge/ps---u-blue)


```
ps -u 'usuario'
```
Muestra todos los procesos ejecutados por un usuario concreto.

![ps-u](img/ps-u.png)


# TOP
Comandos de top y sus opciones


![top](https://img.shields.io/badge/top-blue)

```
top
```
Muestra los procesos ejecutandose a tiempo real


![top](img/top.png)


```
top -b -n 3 > top.info
```

Este comando hace una captura de lo que se mostraria en el comando top (procesos en tiempo real) y los introduce en un archivo, en el caso del ejemplo, en top.info



# HTOP
Comandos de htop y sus opciones

![htop](https://img.shields.io/badge/htop-blue)

```
htop
```
Es parecido al comando top, vendria a ser equivalente al administrador de tareas en windows, permitiendo interactuar y realizar acciones con los procesos, por ejemplo, cerrarlas sin necesidad de usar un comando aparte.


![top](img/htop.png)


# ATOP
Comandos de atop y sus opciones

![atop](https://img.shields.io/badge/atop-blue)

```
atop
```
Este servicio toma instantaneas de los procesos en ejecucion cada cierto tiempo. Por defecto las hace cada 10 minutos.

![atop](img/atop.png)

Para acceder al comando "raw" de un dia en concreto debes acceder a /var/log/atop/ y ejecutar el comando 
```
cd /var/log/atop
atop -r atop_XXXXX
```

Podemos "estresar" la cpu con atop forzandola a crear instantaneas:

```
for i in {1..2}; do yes >/dev/null & done
atop
```

![atop](img/atopestresado.png)






