# 📊 Análisis de Datos de la Ciudad de México (CDMX) con Pandas

Este proyecto presenta un flujo de trabajo completo de Ciencia de Datos utilizando bases de datos abiertas de la **CDMX**. El objetivo principal fue transformar datos brutos en información útil mediante técnicas avanzadas de manipulación de datos y visualización.

## 🛠️ Tecnologías y Librerías
* **Python**
* **Pandas:** Procesamiento y limpieza.
* **Matplotlib / Seaborn:** Visualización de datos.
* **Google Colab / Drive:** Entorno de desarrollo e integración en la nube.

## 📈 Tareas de Ingeniería de Datos Realizadas

### 1. Manipulación y Limpieza de Estructuras
* **Selección Selectiva:** Filtrado de filas y columnas específicas para optimizar el análisis.
* **Transformación de Valores:** Implementación de diccionarios (`{}`) para intercambiar valores y corregir inconsistencias (Ej. mapeo de strings a booleanos).
* **Gestión de Columnas:** * **Adición:** Creación de columnas calculadas (puntos extra, porcentajes y estados lógicos).
  * **Eliminación:** Limpieza de datos irrelevantes o redundantes para simplificar el DataFrame.
* **Manejo de Valores Nulos:** Identificación y tratamiento de datos faltantes (`NaN`).

### 2. Análisis y Lógica de Negocio
Se aplicaron filtros booleanos complejos para identificar cambios de estado en los datos, como detectar estudiantes o registros que cambiaron su estatus de "Reprobado" a "Aprobado" tras aplicar bonificaciones.

### 3. Visualización Exploratoria
Se desarrollaron diversos tipos de gráficos para entender el comportamiento de los datos:
* **Gráficos de Barras:** Comparación de categorías.
* **Gráficos de Líneas:** Evolución de tendencias.
* **Histogramas:** Distribución y frecuencia de las variables.

## 💻 Ejemplo de Implementación Técnica

```python
# Intercambio de valores y conversión de tipos
mapeo = {'Verdadero': True, 'Falso': False}
df['Aprobado'] = df['Aprobado'].replace(mapeo).astype(bool)

# Creación de nuevas métricas
df['Puntos_extra'] = df['Nota'] * 0.40
df['Nota_final'] = df['Nota'] + df['Puntos_extra']

# Filtrado avanzado
seleccionados = df[(df
