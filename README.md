## Practica 04

### Objetivos

Conocer y usar las librerías de módulos **LPM** (  Lybrary of Parametrized Modules)

#### Creación de un nuevo proyecto

![](images/2026-10-24-20-42-40-image.png)

Elegimos el modelo de dispositivo FPGA **ep4ce22f17c6** que corresponde a la Cyclone IV

![](images/2026-10-24-20-44-21-image.png)

Como herramienta de simulación se eligió Questa en lugar de ModelSim

![](images/2026-10-24-20-52-35-image.png)

#### Agregar Librería LPM_ADD_SUB

del **IP Catalog** Seleccionamos la librería LPM_ADD_SUB

![](images/2026-10-24-22-18-03-image.png)

Del tipo VHDL en el directorio de la práctica actual, con el nombre **add_sub_lib**

![](images/2026-10-24-22-20-33-image.png)  

De 8 bits

![](images/2026-10-24-22-21-48-image.png) 

Opcioines de entrada/ salida

![](images/2026-10-24-22-22-39-image.png)

sin pipeline

![](images/2026-10-24-22-23-25-image.png)

Elegimos incluir solamente el archivo de definición

![](images/2026-10-24-22-24-08-image.png)

Confirmamos el archivo a generar

![](images/2026-10-24-22-24-40-image.png)

#### Compilar el proyecto

#### 

Y luego  se compila

![](images/2026-10-24-22-34-36-image.png)

Resultado del RTL Viewer


