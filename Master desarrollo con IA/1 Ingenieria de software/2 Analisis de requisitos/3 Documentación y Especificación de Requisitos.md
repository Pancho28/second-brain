**Categoría P.A.R.A:** #Diseño #Herramienta #Metodologia 

**Temas Relacionados:** [[Ciclo de Vida del Software]], [[Arquitectura de Software]], [[Gestión de Proyectos]], [[Documentación Técnica]]

---

### 🧠 Conceptos Fundamentales

- **Deuda Técnica de Requisitos:** Ambigüedad en las especificaciones que genera una falta de precisión técnica y compromete la mantenibilidad a largo plazo.
    
- **Activo Estratégico Vivo:** Concepto que define a los requisitos no como notas estáticas, sino como conocimiento dinámico que permite reconstruir la lógica de negocio años después.
    
- **Design Docs:** Documento maestro de preconcepción que actúa como plano arquitectónico para evaluar alternativas, pros, contras y definir los "no objetivos" para evitar el _scope creep_.
    
- **RFC (Request for Comments):** Proceso de propuesta técnica que democratiza la toma de decisiones y fomenta un ciclo de retroalimentación colectiva antes de escribir código.
    
- **Happy Path:** Definición del camino principal o comportamiento esperado del sistema dentro de un caso de uso.
    
- **Punto Único de Verdad:** Herramientas y metodologías que minimizan la fricción entre _stakeholders_ e ingeniería mediante una fuente de información centralizada y coherente.
    

---

### 🛠️ Aplicación Técnica / Arquitectura

Para transformar una necesidad abstracta en una **solución ejecutable y trazable**, se deben implementar las siguientes capas de formalización:

1. **Atomización en Ticketing:** Traducir historias de usuario en tareas ejecutables dentro de sistemas como Jira o Azure Boards, asignando IDs únicos y fuentes de origen trazables.
    
2. **Modelado Visual:** Utilizar diagramas de flujo para complementar los casos de uso, reduciendo la carga cognitiva del equipo de desarrollo al visualizar flujos alternativos y casos de error.
    
3. **Diseño Preventivo (Fase RFC):** Lanzar propuestas en modo "proposal" para validar riesgos tecnológicos y alcanzar consensos antes de la implementación.
    
4. **Trazabilidad Integral:** Establecer una conexión bidireccional entre el ticket de trabajo, el repositorio de código y la documentación de alto nivel.
    
5. **Supervisión de IA:** Emplear inteligencia artificial para la redacción y síntesis documental, manteniendo siempre una supervisión humana crítica sobre la lógica técnica.
    

---

### ❓ Preguntas de Autoevaluación

1. ¿Cuál es la función principal de definir los "no objetivos" en un _Design Doc_?
    
2. ¿Por qué se considera que una documentación desfasada es más peligrosa que la ausencia de la misma?
    
3. ¿Qué elementos son críticos para dar robustez a un caso de uso más allá del "Happy Path"?
    
4. ¿Cuál es el límite recomendado de especificidad técnica (código) dentro de la fase de diseño?
    

---

### 🎯 Respuestas

1. Evitar el crecimiento descontrolado del alcance o _scope creep_, delimitando claramente qué no intentará resolver el proyecto.
    
2. Porque induce a errores basados en información incorrecta, mientras que la falta de ella obliga a una validación directa de la realidad técnica actual.
    
3. La documentación de los flujos alternativos y los casos de error, lo que permite prever el comportamiento del sistema ante situaciones no ideales.
    
4. No se deben incluir fragmentos de código específicos; esa profundidad pertenece exclusivamente a la fase de desarrollo e implementación, no al diseño conceptual o arquitectónico.