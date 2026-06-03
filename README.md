# Inteligencia Artificial: Análisis Comparativo de Random Forest vs. Árboles de Decisión

Este repositorio documenta el progreso académico y técnico en la asignatura de Inteligencia Artificial. El núcleo del trabajo se centra en el desarrollo del **Capítulo 6** para el libro *Fundamentos de Inteligencia Artificial Clásica (Edición 2026)*, coordinado por el editor Luis Chamba-Eras.

---

## 👤 Información del Autor
* **Estudiante:** Juan Alberto Calopino Martinez
* **Institución:** Universidad Nacional de Loja (UNL)
* **Correo Electrónico:** [juan.calopino@unl.edu.ec](mailto:juan.calopino@unl.edu.ec)
* **Técnica Asignada:** Random Forest (RF)

---

## 🎯 Objetivo del Proyecto
El objetivo principal es realizar un **Análisis Comparativo y Ventajas de Random Forest (RF) Frente a Árboles de Decisión (DT) en Problemas de Clasificación**. La investigación busca demostrar matemáticamente cómo la arquitectura de ensamble de RF supera las limitaciones críticas de los modelos base mediante la descorrelación de estimadores.

### ❓ La Pregunta Clave
> **¿Por qué la aleatorización doble de Random Forest soluciona la inestabilidad estructural y la alta varianza del Árbol de Decisión tradicional?**

* **Fundamentación Técnica:** Los árboles de decisión individuales son estimadores de alta capacidad pero sufren de una alta varianza geométrica; pequeñas perturbaciones en el dataset derivan en topologías radicalmente distintas (*overfitting*). Random Forest mitiga esto mediante:
  1. **Bagging (Bootstrap Aggregating):** Muestreo aleatorio con reemplazo para entrenar cada árbol en una realización distinta del proceso de generación de datos.
  2. **Subespacios Aleatorios:** Selección de un subconjunto de características ($m=\sqrt{p}$) en cada split para romper la correlación entre árboles.

$$\hat{y} = \frac{1}{B} \sum_{b=1}^{B} h_b(x)$$

---

## 🗂️ Organización del Repositorio (Componentes Académicos)
El código, las tareas y la documentación se estructuran rigurosamente de acuerdo con los componentes curriculares de la asignatura:

### 🏛️ 1. ACD: Aprendizaje en Contacto con el Docente (Clases y Laboratorios)
Desarrollo de las sesiones presenciales y guías asistidas orientadas a la fundamentación de algoritmos supervisados.
* `📁 labs/`: Implementaciones guiadas en el aula de modelos base (Naïve Bayes, KNN, SVM, árboles CART).
* `📁 notebooks/`: Cuadernos interactivos con visualización de fronteras de decisión ortogonales compartidos durante la clase.

### 🔬 2. APE: Aprendizaje Práctico-Experimental (Deberes y Optimización)
Componente de experimentación autónoma y resolución de problemas técnicos donde se evalúan métricas y optimización de modelos.
* `📁 evaluation/OOB_Error/`: Scripts en Python para el cálculo de la estimación *Out-Of-Bag*, demostrando la autovalidación interna de Random Forest sin requerir validación cruzada externa.
* `📁 evaluation/Feature_Importance/`: Implementación práctica de métricas MDI (*Mean Decrease Impurity*) y *Permutation Importance* para mitigar la opacidad del modelo de "caja negra" mediante SHAP y ELI5.

### 🏠 3. AA: Aprendizaje Autónomo (Investigación Avanzada y Redacción)
Trabajo de investigación independiente dedicado al análisis literario y construcción del manuscrito para el libro editorial.
* `📁 research/articles/`: Repositorio que almacena y organiza los 30 artículos científicos indexados analizados para el estado del arte.
* `📁 latex/`: Archivos fuente (`.tex`, `.bib`) y figuras de la Sección 6.1 a la 6.4 del Capítulo 6 compilados en Overleaf.

---

## 🛠️ Tecnologías Utilizadas
* **Lenguaje base:** Python 3.13.0
* **Librerías de ML:** Scikit-Learn, Pandas, NumPy, XGBoost, LightGBM.
* **Explicabilidad (XAI):** SHAP (*Shapley Additive Explanations*) y LIME.
* **Documentación Científica:** LaTeX (Overleaf) para tipografía matemática y BibTeX para la gestión bibliográfica automatizada.

---
*Este proyecto forma parte del currículo avanzado de Inteligencia Artificial Clásica 2026.*
