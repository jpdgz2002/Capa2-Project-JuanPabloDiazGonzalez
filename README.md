# EstudIA · Capa 2 — Fashion-MNIST y fundamentos de MLOps

Laboratorio práctico de visión artificial y fundamentos de MLOps usando **TensorFlow / Keras** sobre el dataset **Fashion-MNIST**, comparando un modelo base (MLP) frente a una red neuronal convolucional (CNN) y dejando evidencia reproducible del experimento.

## 1. Problema
Clasificar imágenes de prendas en **10 categorías** como apoyo para sugerir etiquetas en la organización de un catálogo de productos, dejando la revisión final a una persona cuando existan casos ambiguos o dudosos.

- **Modelo base (baseline):** red neuronal densa sencilla (`MLP`).
- **Modelo alternativo:** red neuronal convolucional (`CNN`).
- **Criterio de selección:** menor pérdida de validación (`val_loss`).

## 2. Dataset
Se utiliza **Fashion-MNIST** (Zalando Research) cargado directamente vía `tf.keras.datasets.fashion_mnist.load_data()`:
- **Entrenamiento original:** 60.000 imágenes (separadas en 54.000 de entrenamiento y 6.000 de validación con `train_test_split` estratificado y semilla `42`).
- **Prueba (`test`):** 10.000 imágenes reservadas exclusivamente para la evaluación final del modelo seleccionado.
- **Clases (10):** `Camiseta/top`, `Pantalón`, `Suéter`, `Vestido`, `Abrigo`, `Sandalia`, `Camisa`, `Zapatilla`, `Bolso`, `Botín`.

## 3. Entrada y salida
- **Entrada:** imagen en escala de grises de `28 × 28` píxeles, normalizada en `float32` en el rango `[0.0, 1.0]` con forma `(28, 28, 1)`.
- **Salida:** vector de 10 probabilidades/puntuaciones `softmax` (una por categoría)[cite: 3].

## 4. Estructura del repositorio
- `EstudIA_C2_FashionMNIST_MLOps.ipynb`: notebook principal con exploración, preparación de datos, baseline, CNN, evaluación, guardado de artefactos y registro opcional en MLflow[cite: 3].
- `requirements.txt`: dependencias del entorno de Python[cite: 3].
- `artifacts/`: modelo guardado (`.keras`), métricas (`metricas.json`), configuración, versiones, `model_card.md` y gráficas generadas[cite: 3].
- `samples/`: imágenes PNG de ejemplo exportadas para pruebas de inferencia[cite: 3].

## 5. Cómo ejecutar
1. Clona o descarga el repositorio y entra a la carpeta del proyecto:
   ```bash
   git clone [https://github.com/jpdgz2002/Capa2-Project-JuanPabloDiazGonzalez.git](https://github.com/jpdgz2002/Capa2-Project-JuanPabloDiazGonzalez.git)
   cd Capa2-Project-JuanPabloDiazGonzalez
