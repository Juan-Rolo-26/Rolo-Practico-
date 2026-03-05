# TP1 — 5 productos/servicios reales que usan Machine Learning

## 1) Satellogic — (Argentina) 

**Qué problema resuelve con ML**  
Monitoreo *a escala* de cambios en el territorio (infraestructura, actividad, cambios en zonas de interés) sin que un analista tenga que revisar manualmente toneladas de imágenes satelitales. La idea es pasar de “mirar fotos” a “detectar señales de cambio”.

**Qué tipo de ML usa (y por qué creemos que es ese tipo)**  
**Supervisado** (principal).  
Porque “detectar” cosas en imágenes (objetos, huellas, cambios relevantes) suele entrenarse con ejemplos etiquetados: *esto es un puerto*, *esto es una pista*, *esto cambió vs. antes*. En visión por computadora, lo típico es clasificación/detección/segmentación con datos rotulados.

**Qué datos probablemente necesita**  
- Imágenes satelitales multiespectrales/ópticas y sus metadatos (fecha, ángulo, resolución, ubicación).   
- Etiquetas/verdad-terreno (por ejemplo: “obra nueva”, “vehículos”, “deforestación”, etc.) para entrenar modelos.  
- Historial temporal por zona (series de tiempo) para detectar “cambio vs. normalidad”.

---

## 2) Kavak — pricing + inspección asistida Mexico

**Qué problema resuelve con ML**  
Reducir incertidumbre y fraude en autos usados:  
- Estimar **precios justos** y actualizados.  
- Asistir inspecciones (detección de fallas/daños) y mejorar decisiones de compra/venta. 

**Qué tipo de ML usa (y por qué creemos que es ese tipo)**  
**Supervisado** (principal).  
- Precio: es un problema clásico de **regresión supervisada** (predecir un número) con ventas históricas.  
- Inspección/daños: suele ser **clasificación/detección supervisada** (daño sí/no, severidad, tipo de daño) con ejemplos previamente etiquetados.

**Qué datos probablemente necesita**  
- Historial de ventas (precio real de cierre, fecha, región).  
- Atributos del auto: marca, modelo, versión, año, km, caja, motor, equipamiento, color, siniestros, etc.  
- Datos de inspección: checklist, mediciones, diagnósticos, fotos/videos del vehículo.  
- Variables de mercado: inflación/localización/demanda estacional.

---

## 3) Stripe — **Radar** 

**Qué problema resuelve con ML**  
Detectar y frenar pagos fraudulentos en tiempo real asignando scores de riesgo con señales de comportamiento y red de pagos.

**Qué tipo de ML usa (y por qué creemos que es ese tipo)**  
**Supervisado** (principal).  
Porque el objetivo típico es predecir una etiqueta: **fraude / no fraude** (clasificación) usando ejemplos históricos (transacciones que terminaron en contracargo, disputa, confirmación de fraude, etc.). Además, se re-entrena con datos nuevos porque los patrones de fraude cambian. :contentReference

**Qué datos probablemente necesita**  
- Datos de transacción: monto, moneda, comercio, rubro, frecuencia, hora.  
- Señales de identidad/dispositivo: IP, geolocalización aproximada, user-agent, fingerprint, cookies.  
- Señales del medio de pago: BIN, país emisor, verificaciones (CVC/AVS), historial de intentos. 
- Resultado posterior: contracargos, reembolsos, disputas (labels para entrenar).

---

## 4) DeepL — traductor neuronal (NMT)

**Qué problema resuelve con ML**  
Traducción automática de texto con buena fluidez y contexto usando redes neuronales entrenadas con grandes volúmenes de textos traducidos.

**Qué tipo de ML usa (y por qué creemos que es ese tipo)**  
**Supervisado**.  
La traducción neuronal se entrena típicamente con **pares (oración origen → oración destino)**, que es supervisión directa: el modelo aprende a predecir la traducción correcta dada la entrada. DeepL mismo menciona entrenamiento con “millones de textos traducidos”. 

**Qué datos probablemente necesita**  
- Corpora paralelos (ej.: EN–ES) con millones de pares de oraciones.  
- Datos monolingües para mejorar fluidez/estilo (según arquitectura).  
- Diccionarios/terminología (dominios técnicos) y feedback de calidad.

---

## 5) Duolingo — **Birdbrain** (personalización del aprendizaje)

**Qué problema resuelve con ML**  
Personalizar el aprendizaje: ajustar ejercicios y dificultad para que el usuario practique lo que más necesita según su desempeño y probabilidad de olvidar. Duolingo describe Birdbrain como un modelo que aprende “de y sobre” cada estudiante para adaptar la experiencia.

**Qué tipo de ML usa (y por qué creemos que es ese tipo)**  
**Supervisado** (principal).  
Porque el sistema puede aprender a **predecir** resultados como: “¿va a responder bien?”, “¿qué tan difícil será este ejercicio?”, “¿qué probabilidad tiene de recordar X?” usando datos históricos donde la “etiqueta” es si el usuario respondió correcto/incorrecto, tiempo de respuesta, etc. (labels observables).

**Qué datos probablemente necesita**  
- Historial del usuario: aciertos/errores por tipo de ejercicio, intentos, tiempo de respuesta. :contentReference
- Trazas de práctica: cuándo practicó, intervalos entre repasos (señales para memoria).  
- Metadatos de contenido: tema, unidad, habilidad, dificultad estimada, idioma base/destino.


## Cierrre mio sin IA
En general las empresas (start ups) utilizan la IA y el Machine Learning para poder analizar datos mas comunmente y automatizar procesos q deberia llevar mucho tiempo de analisis de datos, hoy en dia se usan muchos los datos tanto para vender datos como para obtener inforamacion, es muy importante. 