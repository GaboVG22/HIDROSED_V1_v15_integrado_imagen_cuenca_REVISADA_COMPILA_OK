# HIDROSED_V1 · Base modular integrada

Esta versión fusiona:

1. **Cuenca y propiedades morfométricas**: módulo especializado para área, perímetro, cotas, pendiente media, curva hipsométrica y base técnica para hidrología/hidráulica.
2. **HidroSed · Eje Cauce y Secciones v15 · geometría ajustada a extremos**: incorporado como módulo de eje/perfil/secciones, manteniendo su lógica y funcionamiento.
3. **Base técnica integrada**: expone la información de ambos módulos para futuras conexiones con hidrología, hidráulica, sedimentos y socavación.

## Despliegue

Main file path:

```text
app.py
```

Python:

```text
3.11
```

Incluye configuración Streamlit Cloud con `fileWatcherType = "none"` y dependencias fijadas para reducir riesgo de `Segmentation fault`.


## Corrección v1.1
- Se corrigió `NameError: name 're' is not defined` en el módulo de cuenca y morfometría.
- Se mantiene integrado el módulo Eje Cauce y Secciones v15 con geometría ajustada a extremos.

## HIDROSED_V1 revisión compila OK
- Corrección confirmada: `import re` está en las importaciones globales de `app.py`.
- Se reemplazó además la lectura de radios de ajuste por una lectura robusta sin `re.split` en el módulo de morfometría.
- Verificación realizada: `python -m py_compile app.py` ejecutado correctamente.
- Mantiene módulo de eje cauce y secciones con lógica v15 y conectividad longitudinal tipo HEC-RAS.
