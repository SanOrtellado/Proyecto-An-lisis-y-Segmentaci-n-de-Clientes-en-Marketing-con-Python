# 📊 Proyecto de Marketing con Python – Segmentación de Clientes  

Este proyecto demuestra cómo aplicar **análisis RFM (Recencia, Frecuencia, Monto)** y **Machine Learning (K-Means)** para segmentar clientes en un caso de marketing digital.  

## 📂 Archivos incluidos
- `clientes_ficticios.csv` → Dataset ficticio con 50 clientes y sus datos de compras.  
- `proyecto_marketing_python.ipynb` → Notebook en Python (ejecutar en Jupyter o Google Colab) con el análisis paso a paso.
import pandas as pd
import numpy as np
import seaborn as sns
import matplotlib.pyplot as plt
from sklearn.cluster import KMeans
from sklearn.preprocessing import StandardScaler
 

## 🧾 Descripción del dataset
np.random.seed(42)
n_clientes = 50

data = {
    'ID_CLIENTE': range(1, n_clientes+1),
    'FECHA_ULTIMA_COMPRA': pd.date_range('2025-01-01', periods=n_clientes, freq='7D'),
    'N_COMPRAS': np.random.randint(1, 20, n_clientes),
    'MONTO_TOTAL': np.random.randint(5000, 100000, n_clientes),
    'CANAL': np.random.choice(['Email', 'RRSS', 'Web'], n_clientes)
}
df = pd.DataFrame(data)
df['RECENCIA'] = (pd.to_datetime('2025-09-30') - df['FECHA_ULTIMA_COMPRA']).dt.days
df.head()
<img width="538" height="184" alt="image" src="https://github.com/user-attachments/assets/fe1ac721-b4a2-407c-ad41-5ffcb38ad036" />


El archivo `clientes_ficticios.csv` contiene:  
- **ID_CLIENTE** → Identificador único del cliente.  
- **FECHA_ULTIMA_COMPRA** → Última compra registrada.  
- **N_COMPRAS** → Número total de compras.  
- **MONTO_TOTAL** → Total gastado en ARS.  
- **CANAL** → Canal preferido (Email, RRSS, Web).  
- **RECENCIA** → Días desde la última compra.

## Preparación de la Tabla RFM
  rfm = df[['ID_CLIENTE','RECENCIA','N_COMPRAS','MONTO_TOTAL']].copy()
  rfm.columns = ['ID_CLIENTE','Recencia','Frecuencia','Monto']
  rfm.head()

<img width="392" height="196" alt="image" src="https://github.com/user-attachments/assets/ae645afa-a430-4dcb-a32b-9a46e74c526e" />


## Segmentacion con K-means
X = rfm[['Recencia','Frecuencia','Monto']]
scaler = StandardScaler()
X_scaled = scaler.fit_transform(X)

kmeans = KMeans(n_clusters=4, random_state=42, n_init=10)
rfm['Segmento'] = kmeans.fit_predict(X_scaled)
rfm.head()
<img width="313" height="176" alt="image" src="https://github.com/user-attachments/assets/96d53f2e-60d6-4405-977e-a989e8e1f8d2" />


## Visualización de los segmentos
plt.figure(figsize=(10,6))
sns.scatterplot(data=rfm, x='Recencia', y='Monto', hue='Segmento', palette='tab10', s=100)
plt.title('Segmentación de Clientes - RFM con KMeans', fontsize=14, fontweight='bold')
plt.xlabel('Recencia (días desde última compra)')
plt.ylabel('Monto total gastado (ARS)')
plt.legend(title='Segmento')
plt.show()
<img width="806" height="510" alt="image" src="https://github.com/user-attachments/assets/c887786e-6208-4368-90e1-c223fc462bf2" />


## 🚀 Objetivo del proyecto
- Analizar clientes usando **RFM**.  
- Agrupar clientes en segmentos (ej. **VIPs, Leales, Nuevos, En riesgo**) con **K-Means**.  
- Generar visualizaciones útiles para el área de Marketing.



## 🔧 Tecnologías utilizadas
- Python 3  
- Pandas  
- Scikit-learn  
- Matplotlib / Seaborn  

## 📌 Próximos pasos
- Integrar con datos reales de marketing.  
- Conectar el análisis a un dashboard (Power BI o Looker Studio).  
- Crear un recomendador de productos básico.  


✍️ Autor: **San Ortellado**  
📅 Año: 2025  
