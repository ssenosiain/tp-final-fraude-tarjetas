Versión en Colab: https://colab.research.google.com/drive/1m9KKbu5SnBcNiqg4syJ2vFOClZHONm0u

# Detección de fraude en transacciones con tarjeta de crédito

Trabajo final integrador de la Diplomatura en Ciencia de Datos y Análisis Avanzado.
Autora: Sol Senosiain

## Contenido
- `codigo_fraude.ipynb`: análisis completo (carga, calidad de datos, EDA, modelos, evaluación).
- `credit_card_fraud_10k.csv`: dataset sintético de 10.000 transacciones (Arif Miah, Kaggle).

## Cómo ejecutarlo

### Opción 1: en Google Colab
1. Abrí el link de arriba.
2. Subí `credit_card_fraud_10k.csv` al panel de archivos (ícono de carpeta).
3. Apretá **Runtime → Run all**.

### Opción 2: en tu computadora
1. Instalá las librerías:
pip install pandas scikit-learn numpy
2. Poné el CSV en la misma carpeta que el notebook.
3. Abrí `codigo_fraude.ipynb` en Jupyter o VS Code y corrélo de arriba hacia abajo.

## Qué hace el análisis
- Revisa calidad de datos (nulos, duplicados, outliers).
- Compara Regresión Logística, Random Forest y SVM (RBF), con validación cruzada estratificada de 5 folds.
- Evalúa en un conjunto de prueba del 20%, con PR-AUC, recall y precisión como métricas principales.
- Compara contra una regla simple (compra en el extranjero o ubicación sospechosa).
- Calcula la lectura de negocio del modelo elegido: de cada 100 alertas, cuántas son fraude y qué porcentaje de fraudes se detecta.

## Resultados principales
El modelo elegido es **SVM (RBF)**. En el conjunto de prueba, de 48 alertas, 25 son fraude (52,1 de cada 100). Se detectan 25 de los 30 fraudes (83,3%).
