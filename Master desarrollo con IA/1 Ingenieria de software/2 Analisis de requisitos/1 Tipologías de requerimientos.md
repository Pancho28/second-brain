**Categoría P.A.R.A:** #Diseño #Desarrollo 

**Temas Relacionados:** [[Ingeniería de Requisitos]], [[Metodologías Ágiles]], [[Arquitectura de Software]], [[Gobernanza de Proyectos]]

---

### 🧠 Conceptos Fundamentales

- **Gestión de Requisitos:** Proceso de mediación estratégica que filtra la subjetividad del usuario mediante viabilidad, utilidad y rigor cuantitativo. Actúa como la fase primaria del [[Control de Calidad]].
    
- **Requisitos Funcionales:** Acciones específicas que el sistema debe ejecutar, constituyendo el núcleo operativo (pagos, registros, integraciones).
    
- **Reglas de Negocio:** Normas lógicas volátiles y parametrizables que rigen la operación técnica, como protocolos legales o cálculos de comisiones.
    
- **Requisitos No Funcionales (RNF):** Atributos de calidad que definen la experiencia, incluyendo [[Rendimiento]], [[Seguridad]], [[Usabilidad]] y [[Disponibilidad]].
    
- **Restricciones:** Marcos normativos tecnológicos y legales (ej. [[GDPR]], ISO) que delimitan el diseño y viabilidad del producto.
    
- **Historias de Usuario:** Unidad fundamental de comunicación ágil estructurada en Rol-Objetivo-Beneficio para centrar el desarrollo en el valor de negocio.
    
- **Criterios de Aceptación (Given-When-Then):** Lenguaje estandarizado que elimina ambigüedades y funciona como pre-diseño de pruebas para la automatización.
    
- **Priorización MoSCoW:** Herramienta de gobernanza para alinear expectativas directivas con la capacidad técnica de entrega.
    

---

### 🛠️ Aplicación Técnica / Arquitectura

Para transformar visiones etéreas en **contratos operativos claros**, se debe seguir un flujo de ingeniería de valor:

1. **Cuantificación de Métricas:** Eliminar términos subjetivos (ej. "rápido") y sustituirlos por métricas cuantitativas verificables.
    
2. **Validación de Trazabilidad:** Asegurar que cada requisito permita entender su origen e impacto ante modificaciones en el ecosistema.
    
3. **Parametrización de Reglas:** Separar la función técnica estable de la regla de negocio volátil para mantener la agilidad del sistema.
    
4. **Implementación de BDD (Behavior Driven Development):** Utilizar el formato _Given-When-Then_ para convertir conversaciones en requerimientos verificables y transparentes.
    

---

### ❓ Preguntas de Autoevaluación

1. ¿Por qué se afirma que un requisito bien definido es la primera fase del control de calidad?
    
2. ¿Cuál es la diferencia crítica entre un requisito funcional y una regla de negocio en términos de estabilidad?
    
3. ¿Cómo impacta el uso del formato "Given-When-Then" en el ciclo de vida del desarrollo de software?
    
4. ¿Qué diferencia a un sistema "funcionalmente completo" de uno "estratégicamente útil"?
    

---

### 🎯 Respuestas

1. Porque establece una métrica clara que sustituye a la opinión, permitiendo que la entrega sea verificable y reduciendo fricciones por ambigüedades desde el inicio.
    
2. La función técnica suele ser estable, mientras que la regla de negocio es volátil; por ello, esta última debe ser parametrizada para permitir cambios rápidos sin alterar la estructura del sistema.
    
3. Actúa como un pre-diseño de pruebas que elimina interpretaciones erróneas y facilita la automatización del proceso de validación.
    
4. La utilidad estratégica depende de los requisitos no funcionales; un sistema puede ejecutar todas sus funciones pero fracasar si su latencia es inaceptable o su interfaz es críptica.