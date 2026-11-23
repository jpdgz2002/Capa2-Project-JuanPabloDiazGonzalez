# Model Card · Fashion-MNIST · EstudIA C2

## Propósito
Ejercicio educativo de clasificación de 10 categorías de prendas de Fashion-MNIST.

## Dataset
Zalando Research Fashion-MNIST vía Keras. Entrenamiento: 54000;
validación: 6000; test: 10000 ejemplos.

## Modelo y selección
Modelo elegido: CNN. Criterio: menor pérdida de validación.

## Resultado final (test)
Accuracy: 0.8779. F1 macro: 0.8772.

## Entrada/salida
Entrada: arreglo float32 (28,28,1) normalizado entre 0 y 1.
Salida: 10 valores softmax. No interpretar como probabilidades calibradas.

## Limitaciones
No entrenado para fotografías reales, fondos complejos ni imágenes de mayor resolución.
No aplicar directamente a decisiones comerciales automatizadas sin validación externa.

## Reproducibilidad
Semilla: 42. Versiones registradas en versiones.json.
