# [COMPLETAR: título del proyecto] · Bogotá DataJam 2026 (Datos y Usabilidad)

**Equipo:** [COMPLETAR]

## 1. Problema público abordado
[COMPLETAR: copiar el problema y la hipótesis/pregunta del formulario de caracterización, tal cual, para mantener la trazabilidad.]

- **Pregunta:** [COMPLETAR]
- **Hipótesis:** [COMPLETAR]

## 2. Fuentes de datos
| Fuente | Entidad | Registros | Uso en el análisis |
|---|---|---|---|
| Histórico de siniestros viales Bogotá D.C. | [COMPLETAR] | 199.146 (2015-01-01 a 2021-09-10) | Eventos, gravedad, clase, ubicación, fecha y hora |
| [COMPLETAR: fuente 2] | [COMPLETAR] | [COMPLETAR] | [COMPLETAR: cómo se integra, p. ej. cruce por localidad] |

Detalles de descarga en [`data/README.md`](data/README.md).

## 3. Metodología general
1. **Limpieza:** lectura con `utf-8-sig`, eliminación de columnas redundantes (`X`, `Y`), tratamiento de nulos (`LOCALIDAD`, `CIV`, `PK_CALZADA`), exclusión de `CIV = 0` (valor de relleno).
2. **Transformación:** variables de año, mes, hora, día de la semana, indicadores de gravedad.
3. **Integración de fuentes:** [COMPLETAR: llave de cruce y resultado, p. ej. tasas por 100.000 habitantes por localidad].
4. **Análisis:** evolución temporal, gravedad y tipo, localidades, franjas horarias, puntos críticos, mapas de calor.
5. **Visualización:** [COMPLETAR: dashboard o mapa].

## 4. Cómo ejecutar el código
```bash
git clone [COMPLETAR: URL del repo]
cd [COMPLETAR]
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements.txt
# Coloca los CSV en /data (ver data/README.md)
jupyter notebook notebooks/01_analisis_siniestros.ipynb
```
**En Google Colab:** subir `notebooks/01_analisis_siniestros.ipynb`, ejecutar las celdas en orden y cargar el CSV cuando lo pida. Colab ya incluye las dependencias.

## 5. Despliegue de la visualización
[COMPLETAR: enlace al dashboard o instrucciones para abrir el archivo de `/outputs`, p. ej. abrir `outputs/mapa_calor.html` en el navegador.]

## 6. Estructura del repositorio
```
/data        datasets o instrucciones de acceso
/notebooks   código del análisis (Python)
/outputs     visualizaciones y resultados exportados
/docs        nota técnica, formulario, checklist
README.md
requirements.txt
```

## 7. Resultados principales
[COMPLETAR: 3 a 5 hallazgos con cifras, cada uno enlazado a la figura de /outputs.]

## 8. Limitaciones
- 2021 incompleto (hasta el 10 de septiembre) y 2020 atípico por la pandemia.
- El registro no incluye número de víctimas por evento ni tipo de vehículo.
- `PK_CALZADA` tiene ~19 % de nulos.
