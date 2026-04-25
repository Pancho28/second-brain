**Categoría P.A.R.A:** #Arquitectura #Desarrollo #Metodologia #SOLID #Diseño 

**Temas Relacionados:** [[SOLID]], [[Cohesión]], [[Mantenibilidad]], [[Composición sobre Herencia]]

---

🧠 **Conceptos Fundamentales**

- **[[Single Responsibility Principle]] (SRP)**: Mecanismo de mitigación de riesgos que establece que cada módulo del sistema debe poseer soberanía técnica absoluta sobre su dominio, respondiendo únicamente a una fuente de cambio legítima.
    
- **Fuente de Cambio (Stakeholder)**: La responsabilidad no se define por las tareas ejecutadas, sino por el actor o stakeholder que solicita la modificación. Un sistema está mal diseñado si un cambio en marketing afecta al mismo fichero que un cambio en seguridad.
    
- **[[Cohesión]]**: Objetivo técnico de agrupar elementos que cambian por las mismas razones y separar aquellos que cambian por motivos distintos.
    
- **Modificación en Cascada**: "Code smell" u omisión de cohesión donde un cambio simple (ej. actualizar un proveedor de email) requiere tocar múltiples capas del sistema (datos, lógica, presentación).
    
- **[[Composición Estratégica]]**: Técnica que permite transformar bloques monolíticos en ecosistemas de componentes intercambiables mediante la inyección de dependencias.
    

---

🛠️ **Aplicación Técnica / Arquitectura**

La implementación del SRP permite una **escalabilidad horizontal real** y una reducción del **Time-to-Market** siguiendo estos pasos estratégicos:

1. **Aislamiento de Dominios**: Separar lógicas dispersas (negocio, persistencia, notificaciones) en módulos independientes para evitar que errores en un componente (ej. validación) afecten a otros (ej. logística).
    
2. **Sustitución de Componentes**: Utilizar modelos basados en composición para que piezas como "motores de impuestos" sean intercambiables sin poner en riesgo la lógica central del sistema.
    
3. **Optimización del Testeo**: Implementar dobles de prueba ([[Mocks]]) para validar hipótesis de negocio de forma aislada, reduciendo drásticamente los costes de QA.
    
4. **Evaluación del ROI**: Evitar la parálisis por exceso de granularidad; el SRP no busca funciones pequeñas _per se_, sino funciones con un único motivo de cambio.
    

---

❓ **Preguntas de Autoevaluación**

1. ¿Cuál es el malentendido histórico más común al aplicar la "S" de SOLID y qué consecuencia operativa tiene?
    
2. ¿Cómo se distingue una "tarea ejecutiva" de una "razón de cambio" según el texto?
    
3. ¿Por qué el SRP se considera una "póliza de seguro" contra la obsolescencia técnica en el mercado actual?
    

🎯 **Respuestas**

1. Confundir la simplicidad operativa con la atomicidad funcional, lo que lleva a fragmentar el código en micro-funciones irrelevantes que generan ruido procesal y parálisis por exceso de granularidad.
    
2. Las tareas son la lista de acciones que ejecuta un módulo, mientras que la razón de cambio está vinculada directamente al actor o stakeholder (ej. Marketing vs. IT) que tiene autoridad para solicitar modificaciones en dicha lógica.
    
3. Porque asegura que cada pieza de la arquitectura tenga una misión clara y aislada, permitiendo que el sistema se adapte a cambios de dirección estratégica con un coste operativo mínimo y fiabilidad máxima.