## Practica 04

### Objetivos

Conocer y usar las librerías de módulos **LPM** (  Lybrary of Parametrized Modules)

### Creación de un nuevo proyecto

![](images/2026-10-24-20-42-40-image.png)

Elegimos el modelo de dispositivo FPGA **ep4ce22f17c6** que corresponde a la Cyclone IV

![](images/2026-10-24-20-44-21-image.png)

Como herramienta de simulación se eligió Questa en lugar de ModelSim

![](images/2026-10-24-20-52-35-image.png)

### Agregar Librería LPM_ADD_SUB

del **IP Catalog** Seleccionamos la librería LPM_ADD_SUB

![](images/2026-10-24-22-18-03-image.png)

Del tipo VHDL en el directorio de la práctica actual, con el nombre **add_sub_lib**

![](images/2026-10-24-22-20-33-image.png)  

De 8 bits

![](images/2026-10-24-22-21-48-image.png) 

Opciones de entrada/ salida

![](images/2026-10-24-22-22-39-image.png)

sin pipeline

![](images/2026-10-24-22-23-25-image.png)

Elegimos incluir solamente el archivo de definición

![](images/2026-10-24-22-24-08-image.png)

Confirmamos el archivo a generar

![](images/2026-10-24-22-24-40-image.png)

### Compilar el proyecto

Se selecciona la libraría como top level entity

Y luego se compila

![](images/2026-10-24-22-32-22-image.png)

Resultado del RTL Viewer

![](images/2026-10-24-22-34-36-image.png)

### Simulación

Como al inicio se eligió Questa como herramienta de simulación, es la herramienta que se lanza al hacer clic en **Gate Level Simulation**

![](images/2026-10-24-22-52-34-image.png)

Interfáz de Questa

![](images/2026-10-24-22-55-06-image.png)



#### Preparar la simulación

1. En library se selecciona **add_sub_lib**
   
   ![](images/2026-10-24-22-56-29-image.png)

2. En la sección **Objects** se seleccionan las señales de interés
   
   1. ![](images/2026-10-24-22-58-07-image.png)
      
      Y se hace clic en **add to -> wave -> selected Signals**

3. En la sección **Wave Default**
   
   ![](images/2026-10-24-23-00-50-image.png)
   
   Se fuerzan lo valores de prueba
   
   Por ejemplo : 
   
   - 5 para dataa
   
   - 8 para datab
   
   - 0 para cin
     
     ![](images/2026-10-24-23-02-41-image.png)![](images/2026-10-24-23-04-43-image.png)![](images/2026-10-24-23-04-54-image.png)![](images/2026-10-24-23-07-09-image.png)

Questa acepta comandos, asi que ejecutamos

```bash
run 30 ns
```

![](images/2026-10-24-23-11-07-image.png)

Obtenemos el siguiente resultado

![](images/2026-10-24-23-11-40-image.png)

Que corresponde con lo esperado 5 + 8  = 0D en exadecimal

#### Probar con otros datos

Ahora cambiamos el radix de los puertos a decimal

![](images/2026-10-24-23-14-28-image.png)

Y agregamos otros valores, mal altos, ya que al ser de 8 bits alcanza valores de hasta 255

para dataa 50

![](images/2026-10-24-23-23-11-image.png)

para datab 50 también

![](images/2026-10-24-23-23-42-image.png)

cin en cero

Lo corremos 10 ns

![](images/2026-10-24-23-24-43-image.png)

y observamos como resultado 50 + 50 = 100

Con lo que la librería suma de manera correcta

![](images/2026-10-24-23-25-15-image.png)

## Conclusiones

Conocer la existencia de estas librerías nos ayuda a no tener que generar todos los componentes VHDL desde cero, por ejemplo, hay una librería para implementar Ethernet. y muchas librerías aritméticas, además de que al contar con un configurador, es sencillo personalizar la librería de acuerdo con nuestras necesidades. Por lo que en adelante, cuando requiera una funcionalidad avanzada y general, en lugar de pensar en crearla por mi mismo, primero haría una búsqueda en esta biblioteca.


