# 🏠 El sueño de la casa propia ya murió — y los datos lo prueban

Visualización interactiva sobre la (in)accesibilidad de la vivienda en México, construida con **4,244,769 avalúos** del Índice SHF de Precios de la Vivienda (2018T1–2025T4).

> De **$552,165** en 2018 a **$1,233,200** en 2025: **+123%**, mientras la inflación acumulada fue de ~46%. Descontada la inflación, una casa cuesta hoy **53% más** que en 2018.

## ¿Qué incluye?

| Sección | Contenido |
|---|---|
| **01 · Panorama** | Precio mediano nacional por trimestre, crecimiento anual vs inflación (INPC) y volumen de avalúos |
| **02 · Distribución** | Histograma de precios, composición por clase de vivienda y brecha entre segmentos |
| **⚡ Calculadora** | ¿Puedes comprar? Simula cuánto tardas en juntar el enganche **considerando que el precio sigue subiendo**, y qué porcentaje de tu ingreso se iría en la mensualidad |
| **03 · Geografía** | Precio mediano por estado, comparador interactivo y años de salario mínimo para pagar una casa |
| **04 · Modelos** | Proyecciones a 2027 con **Prophet** y **XGBoost**, validación y comparación |
| **05 · Hallazgos** | Seis conclusiones del análisis |

## Uso

Es un solo archivo HTML, sin build ni dependencias que instalar.

```bash
git clone https://github.com/axrg/Burbuja-Inmobiliaria-Mexico-SHF.git
cd Burbuja-Inmobiliaria-Mexico-SHF
open index.html        # macOS  ·  en Windows: start index.html
```

Para publicarlo gratis: **Settings → Pages → Deploy from branch → `main` / root**.

## Tecnología

- HTML + CSS + JavaScript sin frameworks
- [Plotly.js 2.27](https://plotly.com/javascript/) para las gráficas (CDN)
- Tipografías: Bebas Neue, Syne y JetBrains Mono (Google Fonts)
- Gráficas con carga diferida, diseño responsivo y soporte para `prefers-reduced-motion`

## Fuentes

- **Avalúos:** [Índice SHF de Precios de la Vivienda](https://transparencia.shf.gob.mx) — Sociedad Hipotecaria Federal
- **Inflación:** [INPC, INEGI](https://www.inegi.org.mx/temas/inpc/) (diciembre–diciembre)
- **Salario mínimo:** [CONASAMI](https://www.gob.mx/conasami) — $278.80/día en 2025
- **Tasa hipotecaria de referencia:** 11.46% anual promedio

## Limitaciones

- El Índice SHF solo cubre viviendas con **crédito hipotecario formal**. El mercado informal, la renta y la autoconstrucción no están representados.
- Las clases Económica, Social, Interés Social y Popular suman apenas ~3% de los registros.
- Las proyecciones son estimaciones de modelos con solo 32 puntos trimestrales; no son pronósticos garantizados.
- La calculadora es ilustrativa: supone ingreso y ahorro constantes y no incluye gastos notariales, seguros ni comisiones.

## Cambios respecto a la versión original ([axrg/SHF](https://github.com/axrg/SHF))

- Inflación real por año (INPC) en lugar de una referencia fija de 6.5%; inflación acumulada corregida a ~46%
- Nuevo indicador de crecimiento real (+53%)
- Corregido el ticker (39 años de salario mínimo = casa completa en CDMX, no el enganche)
- Gráfica de validación alineada al trimestre correcto
- Histograma normalizado por ancho de tramo
- Calculadora con alza de precios, enganche, plazo y tasa configurables
- Comparador de estados con botones (funciona en celular)
- Mejor contraste, accesibilidad, metadatos para redes y carga diferida de gráficas

## Autor

Análisis y desarrollo: **Xcaret** · Mejoras de visualización con Claude
