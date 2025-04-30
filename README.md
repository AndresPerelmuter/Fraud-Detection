# Fraud-Detection'

# 🕵️‍♂️ Fraud Detection con Autoencoders

Este proyecto tiene como objetivo detectar transacciones fraudulentas utilizando técnicas de machine learning y deep learning. Se realizó un análisis completo del dataset, desde su exploración inicial hasta el entrenamiento de modelos avanzados.

## 🧰 Tecnologías utilizadas

- Python (pandas, NumPy, matplotlib, seaborn)
- Scikit-learn
- TensorFlow / Keras
- Machine Learning: Árboles de Decisión
- Deep Learning: Autoencoders
- Métricas: Accuracy, F1-Score, Recall, Precision, ROC AUC.

## 📊 Estructura del análisis

1. **Preparación de los Datos:** Carga de librerias y datos.
2. **Exploración de los Datos:** Análisis estadístico y visual para comprender mejor las variables. Ademas, se utilizó arboles de decisión para analizar mediante features importance, la importancia de las variables en el resultado del modelo.
3. **Autoencoder para detección de fraude:**
   - Se entrenó un autoencoder únicamente con las transacciones **no fraudulentas** (`Class = 0`) para aprender el comportamiento "normal" del sistema.
   - Luego, se evaluaron las transacciones reconstruyendo la entrada con el autoencoder y calculando el **error de reconstrucción**.
   - Si el error superaba cierto umbral, se consideraba una transacción anómala (posiblemente fraudulenta).
   - Este enfoque es especialmente útil cuando hay un fuerte desbalance de clases, como ocurre en fraudes reales.

## 🧠 Conclusiones

El modelo basado en redes neuronales obtuvo resultados competitivos frente a algoritmos tradicionales, destacándose en métricas de recall y AUC, esenciales en la detección de fraudes.

