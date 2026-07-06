# Detección de ocupación en una pista de atletismo con OpenCV 🏃‍♀️

Este proyecto consiste en un sistema de procesamiento digital de imágenes para detectar corredores dentro de una pista de atletismo y estimar qué tan ocupada se encuentra.

La idea principal es utilizar una imagen de la pista vacía como referencia y compararla con otra imagen donde aparecen corredores. A partir de las diferencias encontradas se realiza un proceso de limpieza, filtrado y análisis para obtener el número aproximado de personas presentes.


## ¿Cómo funciona?

El proceso general del programa es:

1. Se cargan dos imágenes:
   - una pista sin corredores
   - una pista con corredores

2. Las imágenes pasan por una etapa de preprocesamiento:
   - conversión a escala de grises
   - reducción de ruido mediante filtro Gaussiano

3. Se calcula la diferencia entre ambas imágenes para localizar los cambios producidos por los corredores.

4. Se aplica una segmentación para separar los posibles corredores del fondo.

5. Se delimita una región de interés (ROI) para analizar únicamente la zona de la pista y evitar detecciones innecesarias.

6. Mediante operaciones morfológicas se eliminan pequeños errores y se unen partes separadas de un mismo corredor.

7. Finalmente se detectan los contornos, se aplican filtros para reducir falsos positivos y se calcula la ocupación de la pista.


## Herramientas utilizadas

- Python
- OpenCV
- NumPy
- Matplotlib
- Google Colab
- 


## Resultado

El programa genera una imagen final donde se muestra:

- corredores detectados
- conteo total de personas
- porcentaje de ocupación
- clasificación de ocupación (baja, media o alta)


## Notas

Este proyecto fue desarrollado como una práctica de visión por computadora aplicando técnicas clásicas de procesamiento de imágenes. La imagen de referencia es real por completo, sin embargo la imagen de prueba fue dada por una ia para que fuera la misma pero con personas.

Requiere mejoras futuras
