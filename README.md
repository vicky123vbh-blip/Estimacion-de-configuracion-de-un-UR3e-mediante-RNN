# Implementación de RNN para la Cinemática del Robot UR3e
### Tesis de Ingeniería Mecatónica | Victoria Bello

Este repositorio contiene la implementación de una **Red Neuronal Recurrente (RNN/LSTM)** diseñada para resolver la cinemática directa e inversa del robot colaborativo **UR3e**, validada mediante simulación en **RoboDK** y ejecución física real.

---

## Demostración de Resultados
Esta implementación demuestra el uso de una Red Neuronal Recurrente (RNN) para el control de un robot UR3e. El video captura la persistencia del movimiento, validando que el modelo predice coordenadas precisas y fluidas, evitando las singularidades mecánicas del manipulador de 6 GDL.

[![Implementación UR3e mediante RNN](https://img.youtube.com/vi/k7_GCkqmnfQ/maxresdefault.jpg)](https://youtube.com/shorts/k7_GCkqmnfQ)

> **Video 1:** Validación de trayectoria del brazo colaborativo UR3e. Haga clic en la imagen superior para visualizar el video de la implementación real.

---

## Características del Proyecto
* **Modelo Neuronal:** Red Neuronal Recurrente con memoria de largo-corto plazo (LSTM) para garantizar la continuidad temporal de los movimientos.
* **Control de Hardware:** Conversión automática de unidades (grados a radianes) para integración con el lenguaje **URScript**.
* **Validación:** Comparativa en tiempo real entre el estado ideal (simulación) y el estado real (inferencia de la red).



---

## Estructura del Software
1. **`/Inferencia`**: Scripts de Python que realizan el cálculo de movimiento en tiempo real.
2. **`/Entrenamiento`**: Notebooks de Jupyter con el pre-procesamiento del dataset y el entrenamiento de la RNN.
3. **`/Simulacion`**: Archivos de estación de **RoboDK** para validación cinemática.

---

## Flujo de Control
El sistema sigue un flujo secuencial optimizado para compensar la inercia mecánica del robot:
1. **Inferencia:** Recepción de coordenadas objetivo.
2. **Conversión:** Transformación a radianes para el controlador.
3. **Sincronización:** Pausas estratégicas (`time.sleep`) para asegurar la estabilidad del gripper.

---
**Contacto:** Victoria Bello | Veracruz, México.
