# 📊 Proyecto de Marketing con Python – Segmentación de Clientes  

Este proyecto demuestra cómo aplicar **análisis RFM (Recencia, Frecuencia, Monto)** y **Machine Learning (K-Means)** para segmentar clientes en un caso de marketing digital.

## Mapa Conceptual: Usos de Python en Netflix

<img width="914" height="629" alt="image" src="https://github.com/user-attachments/assets/b0a37919-dfa9-455c-b679-60a5e37d9ec6" />

** Este mapa conceptual muestra cómo Netflix usa Python en sus distintos procesos.

*En el centro está "Netflix y Python".

*De ahí salen las ramas principales:

/ Gestión Operativa

/ Procesamiento de Datos

/ Visualización

/ Automatización

/ Machine Learning

// Cada una se conecta con las actividades específicas que mencionaba el texto (financiación, ETL, recomendaciones, portadas dinámicas, etc.)


## 📂 Archivos incluidos
- `clientes_ficticios.csv` → Dataset ficticio con 50 clientes y sus datos de compras.  
- `proyecto_marketing_python.ipynb` → Notebook en Python (ejecutar en Jupyter o Google Colab) con el análisis paso a paso.

<img width="426" height="158" alt="image" src="https://github.com/user-attachments/assets/f43be390-f8cf-4ef0-bd5c-c739ad349284" />

 

## 🧾 Descripción del dataset
<img width="758" height="258" alt="image" src="https://github.com/user-attachments/assets/f16bd4f7-261e-435f-895f-187573106ea7" />

<img width="538" height="184" alt="image" src="https://github.com/user-attachments/assets/fe1ac721-b4a2-407c-ad41-5ffcb38ad036" />


El archivo `clientes_ficticios.csv` contiene:  
- **ID_CLIENTE** → Identificador único del cliente.  
- **FECHA_ULTIMA_COMPRA** → Última compra registrada.  
- **N_COMPRAS** → Número total de compras.  
- **MONTO_TOTAL** → Total gastado en ARS.  
- **CANAL** → Canal preferido (Email, RRSS, Web).  
- **RECENCIA** → Días desde la última compra.

## Preparación de la Tabla RFM
  <img width="570" height="82" alt="image" src="https://github.com/user-attachments/assets/a163ade2-d331-4122-885e-5fb5f5bfd76a" />


<img width="392" height="196" alt="image" src="https://github.com/user-attachments/assets/ae645afa-a430-4dcb-a32b-9a46e74c526e" />


## Segmentacion con K-means
<img width="543" height="154" alt="image" src="https://github.com/user-attachments/assets/8e82291a-946e-484f-b06e-8a032b56df6c" />

<img width="313" height="176" alt="image" src="https://github.com/user-attachments/assets/96d53f2e-60d6-4405-977e-a989e8e1f8d2" />


## Visualización de los segmentos
<img width="740" height="144" alt="image" src="https://github.com/user-attachments/assets/a6a7431d-7d87-4071-8395-e72d159ada29" />


<img width="806" height="510" alt="image" src="https://github.com/user-attachments/assets/c887786e-6208-4368-90e1-c223fc462bf2" />

## 📈 Análisis descriptivo de los segmentos

* El gráfico muestra la segmentación de clientes utilizando el modelo RFM (Recencia, Frecuencia, Monto) con K-Means.

* Eje X (Recencia): número de días desde la última compra. Valores más bajos indican clientes recientes.

* Eje Y (Monto): total gastado por cliente en ARS.

## Cada color representa un segmento detectado por K-Means:

🟦 Segmento 0: clientes de bajo gasto y compras recientes → perfil de clientes nuevos o básicos.

🟧 Segmento 1: clientes con gasto medio/alto y frecuencia intermedia → clientes valiosos y consistentes, considerados “VIPs”.

🟩 Segmento 2: clientes con frecuencia y gasto moderados → clientes leales, con buen potencial de retención.

🟥 Segmento 3: clientes de alto gasto en el pasado, pero con alta recencia → clientes en riesgo de abandono, ideales para campañas de retención.

## 📌 Conclusiones

* El modelo permite diferenciar clientes activos, leales, VIPs y clientes en riesgo.

* Estos insights pueden usarse para estrategias de marketing personalizadas:

* Descuentos para clientes en riesgo.

* Programas de fidelización para leales.

* Promociones exclusivas para VIPs.

* Campañas de bienvenida para nuevos.


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
