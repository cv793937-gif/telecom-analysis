# 📊 Análisis de Usuarios y Segmentación para ConnectaTel

Este proyecto realiza un análisis integral del comportamiento de los usuarios de ConnectaTel utilizando datos de perfil, uso del servicio y planes contratados. El objetivo es identificar segmentos de clientes, patrones de uso y oportunidades de negocio basadas en datos.

---

## 🚀 Objetivos del Proyecto

- Limpiar y validar la calidad de los datos.
- Analizar la distribución de edad y su relación con los planes.
- Crear segmentos de uso (bajo, medio, alto) basados en llamadas y mensajes.
- Detectar outliers y patrones de uso extremo.
- Generar insights accionables para mejorar la oferta de planes.
- Proponer recomendaciones estratégicas para ConnectaTel.

---

## 🧹 Limpieza de Datos

- Se detectaron valores **sentinel** como `-999` en la columna `age`.
- Se identificaron altos porcentajes de nulos en:
  - `duration` (55%)
  - `length` (44.7%)
- Se verificó que los nulos en `duration` y `length` son **MAR**, ya que dependen del tipo de evento (`call` vs `text`).
- Los nulos se conservaron para mantener la integridad analítica.

---

## 📈 Análisis Exploratorio

### Distribución de Edad
- La edad presenta una distribución **sesgada a la derecha**, concentrada entre 30 y 60 años.
- Se generaron histogramas y curvas KDE para comparar entre planes.

### Segmentación por Nivel de Uso
Se creó la columna `grupo_uso`:

- **Bajo uso**: llamadas < 5 y mensajes < 5  
- **Uso medio**: llamadas < 10 y mensajes < 10  
- **Alto uso**: resto de casos  

### Outliers
- Se detectaron valores extremos en `length` y `duration`.
- Representan heavy users o posibles líneas corporativas.

---

## 🔍 Insights Clave

- El segmento **Alto uso** es el más valioso por su mayor consumo y menor sensibilidad al precio.
- El segmento **Uso medio** tiene alto potencial de migración a planes superiores.
- El segmento **Bajo uso** requiere estrategias de retención y planes económicos.
- Los outliers sugieren oportunidades para planes premium o corporativos.

---

## 💡 Recomendaciones

- Crear un **plan premium** para heavy users.
- Desarrollar un **plan intermedio** para usuarios de uso medio.
- Implementar un **plan económico** para usuarios de bajo uso.
- Ofrecer paquetes personalizados basados en patrones de uso extremo.
- Monitorear continuamente los patrones de uso para detectar oportunidades de upselling.

---

## 🛠️ Tecnologías Utilizadas

- Python  
- Pandas  
- NumPy  
- Seaborn  
- Matplotlib  
- Jupyter Notebook  

---

## 📁 Estructura del Proyecto


---

## 📬 Contacto

Proyecto desarrollado por **Christian** como parte de su formación en análisis de datos y optimización de procesos.

