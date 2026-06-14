# Práctica de Laboratorio N° 3: Transformada de Fourier y sus Aplicaciones en el Análisis de Señales

Este repositorio contiene el desarrollo completo, tanto analítico como computacional, de la **Práctica N° 3** para la asignatura de **Matemática Avanzada**. El objetivo principal es aplicar la Transformada de Fourier continua y sus propiedades fundamentales para analizar, filtrar y modular señales en el dominio de la frecuencia utilizando Python.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1Gn9pm6FAJ2RcyxniAwA4uVoYAnipAbIE?usp=sharing)

---

## 🏛️ Información Institucional
* **Institución:** Escuela Superior Politécnica de Chimborazo (ESPOCH)
* **Facultad:** Facultad de Informática y Electrónica (FIE)
* **Carrera:** Tecnologías de la Información
* **Curso:** Cuarto Semestre (PAO 4)
* **Asignatura:** Matemática Avanzada
* **Docente:** Lcda. Miriam Ávila P., Mg.

---

## 👥 Integrantes del Grupo
* **Jonathan Steven Acosta Aldaz** 
* **Kevin Andres Morales Abril**
* **Kevin Gabriel Chinlle Yunga**

---

## 📝 Descripción de la Práctica

La práctica aborda el estudio de la **Transformada de Fourier (TF)** como una herramienta matemática binaria capaz de trasladar representaciones del dominio del tiempo al dominio de la frecuencia. Se divide en cuatro actividades macro estructuradas bajo los lineamientos de la guía de laboratorio:

### 1. Transformada de Fourier de Funciones Canónicas
* **Impulso Unitario:** Aproximación de la Delta de Dirac $\delta(t)$ mediante una función gaussiana de área unitaria ($\epsilon = 0.001$) demostrando un espectro completamente plano.
* **Función Constante ($f(t) = 1$):** Demostración numérica del truncamiento temporal de la ventana, donde la delta ideal teórica $2\pi\delta(\omega)$ se manifiesta como un pico finito escalado por la duración de la ventana $T$.
* **Escalón Unitario ($u(t)$):** Análisis espectral y visualización en frecuencia del **Fenómeno de Gibbs** originado por la discontinuidad abrupta en el origen.

### 2. Teorema de Convolución y Filtrado Paso-Bajo
* **Verificación del Teorema:** Comparación matemática y computacional entre la integración directa por tramos de un pulso rectangular con una exponencial causal $(f * g)(t)$, frente al producto espectral inmediato mediante la FFT e IFFT. El error relativo obtenido es menor al $0.102\%$.
* **Filtro Paso-Bajo Ideal:** Diseño y aplicación de una ventana rectangular de filtrado frecuencial con frecuencia de corte $f_c = 15 \text{ Hz}$ sobre una señal compuesta por múltiples tonos contaminada con ruido blanco gaussiano.

### 3. Transformadas Seno y Coseno de Fourier
* Deducción analítica completa y verificación mediante simulación de las transformadas para la función exponencial decreciente causal $f(t) = e^{-at}u(t)$.
* Comprobación de las relaciones directas con las extensiones de paridad:
  * $\text{Re}\{\mathcal{F}\{f_e(t)\}\} = \mathcal{F}_c\{f(t)\}$
  * $\text{Im}\{\mathcal{F}\{f_o(t)\}\} = -\mathcal{F}_s\{f(t)\}$

### 4. Teoremas Fundamentales y Modulación AM
* **Desplazamiento Temporal:** Validación gráfica del factor de fase compleja $e^{-j\omega t_0}$ inducido por un retardo en el tiempo.
* **Teorema de Parseval:** Demostración cuantitativa de la conservación de la energía espectral vs. temporal empleando la función gaussiana $f(t) = e^{-t^2}$, obteniendo un error numérico absoluto de orden $10^{-16}$.
* **Modulación AM:** Análisis espectral de una portadora linealizada mediante identidades trigonométricas, identificando los 6 deltas de Dirac bilaterales correspondientes a la portadora ($\omega = \pm 100 \text{ rad/s}$) y sus bandas laterales ($\omega = \pm 90 \text{ rad/s}$ y $\omega = \pm 110 \text{ rad/s}$).

---

## 📁 Estructura del Proyecto

```bash
├── README.md              # Descripción del repositorio y de la práctica
├── Lab III.ipynb                # Script unificado en Python con todas las actividades
├── Grupo_1_práctica_3.pdf # Informe formal de laboratorio en formato PDF
└── .gitignore             # Exclusión de archivos temporales de Python
