# CopyCode
Repositorio del proyecto para detección de plagio en código Java

# Descripción del Proyecto
En este proyecto se creará un modelo de clasificación de código con la capacidad de identificar autoría.

# Contexto
En el módulo se revisan redes neurolanes de capas densas y convolutivas cuyas funciones y parámetros le permitirán al modelo aprender a partir de código fuente.

# Descripción del dataset
El dataset utilizado es [AI-SOCO](https://github.com/AliOsm/AI-SOCO) disponible públicamente *GitHub* bajo la licencia **MIT**.

Espacio en disco: 8.63 MB

El dataset está dividido en train, development y testing con 50000, 25000 y 25000 ejemplos, respectivamente. Cada uno consiste de dos partes:
* Archivos CSV: Contiene pares de ids de usuarios (uids) y ids de problemas (pids). 
    * dev.csv: Cada uid aparece 25 veces en el archivo con 25 pids diferentes para entrenamiento.
    * test.csv: Cada uid aparece 25 veces en el archivo con 25 pids diferentes para entrenamiento.
    * train.csv: Cada uid aparece 50 veces en el archivo con 50 pids diferentes para entrenamiento.
* Directorios: Contienen los códigos fuentes. Cada pid en el archivo CSV está conectado al archivo de código fuente de su respectivo directorio directorio.
    * dev: Contiene 25000 ejemplos
    * test: Contiene 25000 ejemplos
    * train: Contiene 50000 ejemplos

Dada la estructura y contenido y el problema que ataca, el dataset está enfocado en la identificación de autoría de un código fuente, principalmente Java. Sin embargo, puede usarse con fines de identificar plagio o trampa.

# Metodología

## Separación
El dataset ya se encuentra separado, por lo que este paso no es necesario.

## Tokenización
