# Tesis

# Identificación de patrones en obras de Arte Marginal (Art Brut) mediante Deep Learning

## Descripción

Este proyecto analiza obras de arte del movimiento **Art Brut** (Arte Marginal) para identificar 
patrones visuales asociados a condiciones de salud mental en sus autores, utilizando técnicas 
de aprendizaje profundo.

El trabajo combina web scraping automatizado, aumento de datos y optimización de hiperparámetros 
para entrenar una red neuronal convolucional capaz de clasificar estilos artísticos.

## Tecnologías utilizadas

- **Python** — lenguaje principal
- **VGG16 / VGG19** — arquitecturas de red neuronal convolucional (transfer learning)
- **Selenium** — web scraping para recolección de imágenes Art Brut
- **Artemis** — descarga de estilos alternativos de referencia
- **Optuna** — optimización automática de hiperparámetros
- **Data Augmentation** — transformaciones para ampliar y balancear el dataset

## Metodología

### 1. Adquisición y procesamiento de datos
- Descarga de imágenes desde dos fuentes:
  - **Estilos alternativos** (Realism, Abstract Expressionism) mediante Artemis
  - **Art Brut** mediante web scraping con Selenium
- Análisis exploratorio del dataset obtenido

### 2. Transformación a base de datos
- Establecimiento de estructura jerárquica de carpetas por clase
- Conversión de imágenes a tensores y creación de DataLoaders

### 3. Modelo Deep Learning
- Selección de arquitectura (VGG16 / VGG19) con transfer learning
- Definición del número óptimo de capas del clasificador mediante Optuna
- Verificación y ajuste de hiperparámetros

### 4. Data Augmentation
- Aplicación de transformaciones sobre el dataset de entrenamiento
- Análisis de sensibilidad para evaluar el impacto del aumento de datos

### 5. Resultados
- Tests estadísticos para validar el modelo
- Evaluación final de resultados

## Estructura del proyecto

| Archivo | Descripción |
|---|---|
| `Prueba_1_webscrapping.ipynb` | Scraping de imágenes Art Brut con Selenium |
| `D_augmentation_realism.ipynb` | Data augmentation — estilo Realism |
| `Daugmentation_AbExpressionionism copy.ipynb` | Data augmentation — Abstract Expressionism |
| `optuna.ipynb` | Búsqueda de hiperparámetros óptimos |
| `prueba6_realism.ipynb` | Entrenamiento del modelo VGG16 |
| `prueba_0.ipynb` | Experimentos iniciales |

## Contexto académico

Proyecto de Tesis de Máster — análisis de la relación entre expresión artística y 
salud mental a través de técnicas de visión por computador.
