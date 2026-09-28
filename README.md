# Taller1Andes

**MINE-4101: Ciencia de Datos Aplicada**  
*Maestría en Ingeniería de Información / Escuela de Posgrado*  
*Universidad de los Andes*  

---

##  Integrantes del Equipo
* **Joubert Daniel Alvarez Ramirez**

---

##  Objetivo y Alcance
### Objetivo
Diseñar una estrategia analítica y un conjunto de criterios de focalización temprana (desde el momento de la firma) para la oficina de control interno de una entidad pública, con el fin de optimizar los recursos de supervisión e identificar qué contratos de compra de bienes presentan mayor propensión a sufrir adiciones de plazo o cierres irregulares sin liquidación bilateral.

### Alcance
* **Fuente de datos:** Contratos de bienes (compraventa y suministros) suscritos por entidades públicas colombianas extraídos de SECOP II entre 2019 y 2025 (196.391 registros y 36 columnas).
* **Enfoque analítico:** Exploración y depuración de calidad de datos (inconsistencias sintácticas y de dominio), contraste formal de hipótesis estadísticas no paramétricas y de independencia categórica, análisis bivariado/multivariado, y formulación de una matriz de riesgo preventiva e informe ejecutivo para la toma de decisiones.

---

##  Organización del Repositorio

```text
├── data/
│   └── secop_bienes.parquet     # Dataset base (no se versiona en Git por tamaño; ver instrucciones.txt)
│   └── instrucciones.txt        # txt de las instrucciones para descargar el dataset
├── taller_1.ipynb 
├── InformeEjecutivo_Taller1.pdf     # Informe ejecutivo con hallazgos, conclusiones y graficas
├── analisis_estadistico_relaciones.png # Gráficas generadas para el informe
├── .gitignore                   # Exclusión de archivos binarios y temporales
├── requirements.txt             # Dependencias exactas de Python
└── README.md                    # Documentación general del proyecto
```
##  Conclusiones
- Para prevenir casos graves de adiciones de plazo se debe tener bajo vigilancia los contratos de licitación pública de larga duración y alto valor presupuestado inicial, teniendo en cuenta especialmente los de suministros que se tienden a demorar mucho más en sus incidencias.
- Para evitar incidentes de cierres sin liquidar, se deben vigilar los procesos de régimen especial y contratación directa, vigilando especialmente el sector de ciencia y tecnología (aunque la mayoría de sectores igual tiene altos índices de cierres sin liquidar)
- El hecho de que más de la mitad (55.31%) de los contratos finalizados carezca de acta de liquidación representa una vulnerabilidad administrativa y jurídica crítica para el Estado. Control Interno debe transitar de una supervisión pasiva a la implementación de alertas tempranas automáticas previas al vencimiento de los términos de liquidación bilateral. 

##  Instrucciones de Ejecucion
1. Una vez descargado el repositorio se debe descargar el archivo secop_bienes.parquet siguiendo las instrucciones que estan en data/instrucciones y ubicar los datos descargados en la carpeta data/
2. Cuando ya se tengan descargados deben tener en cuenta que se usaron las librerias:
pandas
numpy
scipy
matplotlib
seaborn
pyarrow
statsmodels
jupyterlab
