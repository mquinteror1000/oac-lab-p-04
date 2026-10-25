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
     
     ![](images/2026-10-24-23-02-41-image.png)![](images/2026-10-24-23-04-43-image.png)![](images/2026-10-24-23-04-54-image.png)


