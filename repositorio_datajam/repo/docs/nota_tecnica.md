# Nota técnica sobre integración de datos públicos (máx. 1 página)
**Equipo:** DATAPRIME · **Proyecto:** DATA WOLRD

## 1. Dificultades de acceso, calidad, actualización y documentación
- El archivo de siniestros trae BOM en UTF-8, lo que altera el nombre de la primera columna si no se lee con `utf-8-sig`.
- Cobertura hasta el 10/09/2021: no permite analizar el periodo posterior.
- ~19 % de nulos en `PK_CALZADA`, ~1 % en `CIV` y 46 registros sin `LOCALIDAD`.
- `CIV = 0` aparece 883 veces y parece un valor de relleno, no un tramo real.
- Las fechas llevan el sufijo `+00` aunque parecen horas locales; falta documentación que lo aclare. [VERIFICAR contra el diccionario de datos]
- [COMPLETAR: metadatos, diccionario de datos, fecha de actualización]

## 2. Retos en la integración de fuentes
- [COMPLETAR: llave de cruce (localidad, CIV, UPZ, fecha)]
- [COMPLETAR: diferencias de nombres, tildes, escalas temporales o espaciales]

## 3. Limitaciones encontradas
- No hay número de víctimas por evento, tipo de vehículo ni condiciones de la vía.
- [COMPLETAR]

## 4. Recomendaciones para mejorar el uso de datos públicos
- Publicar diccionario de datos y fecha de última actualización.
- Documentar valores especiales (`CIV = 0`).
- Publicar en UTF-8 sin BOM y con zona horaria explícita.
- Incluir víctimas, tipo de vehículo y actores viales por evento.
- [COMPLETAR]

## 5. Utilidad de los datos para comprender el problema
[COMPLETAR: 3 a 4 líneas sobre qué permitieron entender los datos y qué no.]
