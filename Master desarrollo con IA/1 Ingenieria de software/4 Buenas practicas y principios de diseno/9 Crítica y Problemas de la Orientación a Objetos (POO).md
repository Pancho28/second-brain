**Categoría P.A.R.A:** #Desarrollo #Diseño #Metodologia #Paradigmaprogrmacion 

**Temas Relacionados:** [[Composición vs Herencia]], [[Deuda Técnica]], [[Paradigma Funcional]], [[Encapsulamiento]], [[Patrones de Diseño]]

---

## 🧠 Conceptos Fundamentales (Definiciones Cortas)

- **Jerarquías Rígidas:** Estructuras de herencia profundas donde cualquier modificación en la clase raíz provoca un efecto dominó incontrolable en las subclases, comprometiendo la escalabilidad.
    
- **Composición sobre Herencia:** Estándar de diseño moderno que favorece la construcción de sistemas mediante funcionalidades desacopladas y orquestadas, en lugar de taxonomías forzadas.
    
- **Encapsulación Cosmética:** Práctica ineficiente de saturar el código con `getters` y `setters` automáticos sin lógica de negocio, lo que aumenta la verbosidad sin proteger realmente la integridad de los datos.
    
- **Estado Mutable Compartido:** Riesgo técnico inherente a la POO donde múltiples objetos pueden alterar los mismos datos, dificultando la predictibilidad y el testing.
    
- **Multiparadigma:** Enfoque arquitectónico que integra lo mejor de la POO con la programación funcional, utilizando funciones puras para transformaciones de datos y clases solo para gestión de estado complejo.
    

---

## 🛠️ Aplicación Técnica / Arquitectura

Para mitigar las deficiencias de la POO tradicional y construir sistemas resilientes, se deben aplicar las siguientes estrategias:

- **Inyección de Dependencias (Constructor):** Implementar siempre la inyección a través del constructor para eliminar el acoplamiento fuerte y permitir la sustituibilidad en pruebas unitarias.
    
- **Adopción de Funciones Puras:** Priorizar el paradigma funcional en procesos de automatización y transformaciones **ETL (Extract, Transform, Load)** para eliminar efectos secundarios y mejorar el rendimiento.
    
- **Descarte de Clases de Utilidad:** Si un conjunto de funciones no mantiene un estado interno, deben implementarse como funciones independientes en lugar de agruparlas en clases estáticas innecesarias.
    
- **Auditoría de Patrones Clásicos:** Analizar críticamente los 23 patrones de diseño originales; muchos (como el _Singleton_ o el _Iterator_) han sido superados por capacidades nativas de lenguajes modernos.
    
- **Refactorización de Interfaces:** Evitar la creación de interfaces extensas para funcionalidades que no tienen múltiples implementaciones previstas a corto plazo, reduciendo la sobreingeniería.
    

---

## ❓ Preguntas de Autoevaluación

1. ¿Por qué la "composición sobre la herencia" se considera el estándar de oro para evitar el efecto dominó en sistemas complejos?
    
2. ¿Qué impacto negativo tiene la "encapsulación cosmética" en la mantenibilidad de un repositorio a largo plazo?
    
3. ¿En qué escenarios específicos el paradigma funcional supera en eficiencia a la programación orientada a objetos?
    
4. ¿Cuál es el criterio técnico para decidir si una funcionalidad debe residir en una clase o ser una función pura?
    

---

## 🎯 Respuestas

1. Porque permite modularidad mediante piezas independientes que se orquestan según la necesidad del negocio, evitando que cambios en una base compartida (raíz) rompan accidentalmente comportamientos en ramas inferiores no relacionadas.
    
2. Aumenta innecesariamente el volumen de código y la complejidad cognitiva sin aportar valor real a la protección de datos, convirtiendo el código en un activo rígido y difícil de auditar.
    
3. En scripts de automatización y procesos de transformación de datos (ETL), donde la ausencia de efectos secundarios y la inmutabilidad garantizan una ejecución predecible y paralelizable.
    
4. Si la funcionalidad no requiere mantener un estado interno (memoria de datos entre llamadas), debe ser una función pura. La clase solo se justifica cuando existe una necesidad estructural de gestionar un estado complejo.