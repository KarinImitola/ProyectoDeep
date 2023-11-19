# Detección de Botellas de Plástico con YOLOv3

## Video del Desarrollo del Proyecto
[![Video del Desarrollo](https://img.youtube.com/vi/ojxQuIABw4I/0.jpg)](https://www.youtube.com/watch?v=ojxQuIABw4I)

## Descripción del Proyecto
Este proyecto utiliza YOLOv3 para la detección de botellas de plástico en centros de acopio, cumpliendo con la resolución 1407 de 2018 sobre la responsabilidad extendida del productor en envases y empaques. El informe abarca desde la obtención de datos hasta la validación del modelo.

## Obtención de Datos
- **Dataset:** Imágenes anotadas de botellas de plástico de Kaggle.
- **Enlace al Dataset:** [Plastic Bottles Image Dataset](https://www.kaggle.com/datasets/siddharthkumarsah/plastic-bottles-image-dataset).

## Estructura del Modelo YOLOv3
- **Algoritmo:** YOLOv3.
- **Características Destacadas:** Rápida detección de objetos, capacidad para identificar múltiples clases, utiliza Darknet-53 como base.

## Implementación en Colab
- Habilitación de GPU.
- Montaje de Google Drive para almacenamiento y acceso a archivos.
- Archivos Custom_data: [Modelo inicial](https://drive.google.com/drive/u/2/folders/1B2CaKL25vJv6RKt6KSMK0jgbG3bAYrLl),                           [Modelo modificado](https://drive.google.com/drive/folders/1phvuS45YYsYIx9PNWd6_HDa43mwUn-Pb)

## Proceso de Entrenamiento
1. Creación de directorio de imágenes.
2. Creación de archivos de entrenamiento y prueba.
3. Creación de directorio de backup para pesos del modelo.
4. Creación del archivo de datos YOLO.
5. Clonación y ajuste de Darknet.
6. Descarga de pesos pre-entrenados.
7. Entrenamiento del modelo por 2000 épocas.
8. Cálculo de la precisión media (mAP).

## Ajuste a la Estructura del Modelo
- **Modelo Inicial:**
  - Resolución: 416x416
  - Batch: 64
  - Max Batches: 2000
  - Steps (80%, 90%): 1600, 1800

- **Modelo Modificado:**
  - Canal único (escala de grises).
  - Cambio en el tamaño de las cajas delimitadoras.
  - 
## Detección en Tiempo Real
Se implementó la detección en tiempo real con OpenCV y YOLOv3.

## Conclusiones y Sugerencias
El modelo inicial muestra potencial de mejora, mientras que el modificado ofrece perspectivas con escala de grises. Se sugiere ajustes adicionales en hiperparámetros y arquitectura para mejorar la detección de objetos.
