# Raster Digital Divide — Brecha Digital Territorial Cusco

## Descripción
Análisis geoespacial que mide la brecha digital territorial en la región Cusco, Perú, cruzando datos de luces nocturnas NASA VNL 2025 (proxy de urbanización) con cobertura móvil OSIPTEL 2019 (proxy de acceso a internet).

**Pregunta de investigación:** ¿Qué zonas de Cusco tienen población activa pero carecen de conectividad móvil?

## Dependencias
```bash
pip install -r requirements.txt
```

## Cómo ejecutar
1. Descarga los rasters en `data/` desde el Drive del curso
2. Abre `notebooks/digital_divide_cusco.ipynb`
3. Ejecuta todas las celdas en orden

## Archivos de salida
| Archivo | Descripción |
|---------|-------------|
| `vnl_norm.tif` | Luces nocturnas normalizadas [0-1] |
| `conn_norm.tif` | Conectividad normalizada [0-1] |
| `ibd_brecha_digital.tif` | Índice de Brecha Digital [-1, 1] |
| `clasificacion_brecha.tif` | Clasificación territorial 4 clases |
| `dashboard_brecha_digital.png` | Dashboard final completo |

## Hallazgos principales
El 90.8% del territorio cusqueño cae en la categoría de Brecha Crítica, sin luz ni conectividad. La ciudad de Cusco y el corredor Urubamba-Quillabamba concentran casi toda la actividad urbana y la cobertura móvil. La correlación de Pearson entre VNL y conectividad (r=0.46, p<0.001) confirma que la conectividad sigue patrones urbanos pero con cobertura incompleta incluso en zonas iluminadas.