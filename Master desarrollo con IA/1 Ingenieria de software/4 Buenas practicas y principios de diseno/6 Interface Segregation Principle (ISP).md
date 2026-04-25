**Categoría P.A.R.A:** #Arquitectura #Desarrollo #Diseño #SOLID #Metodologia

**Temas Relacionados:** [[Acoplamiento]], [[Cohesión]], [[Diseño de Interfaces]], [[Testing Unitario]], [[Arquitectura de Software]]

---

## 🧠 Conceptos Fundamentales (Definiciones Cortas)

- **Principio de Segregación de Interfaces (ISP):** Establece que ningún cliente debe ser obligado a depender de métodos que no utiliza, fragmentando interfaces monolíticas en unidades específicas.
    
- **Interfaces Monolíticas:** Abstracciones "gordas" o generales que fuerzan a los implementadores a incluir lógica o métodos irrelevantes para su propósito.
    
- **Dependencias Ociosas:** Lastre operativo que ocurre cuando un componente arrastra funciones innecesarias, dificultando el escalado y la mantenibilidad.
    
- **Soberanía Técnica de Módulos:** Capacidad de cada componente para poseer exactamente las herramientas necesarias para su función, minimizando efectos secundarios imprevistos.
    
- **Cohesión Funcional:** El equilibrio ideal en la división de interfaces donde se evita la fragmentación excesiva (un método por interfaz) manteniendo la lógica agrupada con sentido.
    

---

## 🛠️ Aplicación Técnica / Arquitectura

La implementación del ISP transforma el desarrollo en una ingeniería de precisión mediante las siguientes tácticas:

- **Fragmentación en Unidades Cohesivas:** Dividir interfaces grandes en interfaces pequeñas y específicas (ej. separar una interfaz `Trabajador` en `Comensal` y `Ejecutor` para que un robot no necesite "saber comer").
    
- **Optimización de Mocks para Testing:** Utilizar interfaces pequeñas (como `Readable`) para simplificar la creación de simulacros en pruebas unitarias, evitando configurar funciones de escritura o borrado innecesarias.
    
- **Composición sobre Herencia:** Emplear interfaces pequeñas para "componer" objetos con múltiples habilidades específicas, similar a piezas de Lego, superando la rigidez de las jerarquías de clases.
    
- **Detección de Malas Abstracciones:** Si varias clases ignoran los mismos métodos de una interfaz, esta debe dividirse de inmediato para restaurar la salud del diseño.
    
- **Aprovechamiento de Paradigmas Modernos:** En lenguajes como **Go**, utilizar el polimorfismo implícito para abrazar interfaces basadas en el comportamiento real y no en contratos burocráticos.
    

---

## ❓ Preguntas de Autoevaluación

1. ¿Qué relación existe entre la violación del ISP y la generación de deuda técnica en un sistema que crece?
    
2. ¿Cuál es el riesgo de caer en la "fragmentación atómica" al intentar aplicar este principio?
    
3. ¿Cómo facilita la segregación de interfaces los ciclos de feedback y la ejecución de QA?
    
4. Desde el punto de vista de la "soberanía técnica", ¿por qué es crítico definir correctamente las fronteras de comunicación entre componentes?
    

---

## 🎯 Respuestas

1. Las interfaces monolíticas fuerzan a los clientes a depender de métodos que jamás ejecutarán, lo cual se ignora al inicio pero se convierte en una deuda asfixiante que genera rigidez y efectos secundarios imprevistos al intentar escalar.
    
2. Crear una interfaz por cada método incrementa la **complejidad cognitiva** del sistema; el objetivo es buscar un equilibrio basado en la **cohesión funcional**.
    
3. Reduce la fragilidad de los tests unitarios y acelera las suites de pruebas al permitir crear mocks mucho más sencillos que solo implementan los métodos estrictamente necesarios para la prueba.
    
4. Porque permite modificar o evolucionar una pieza del sistema sin comprometer la integridad de todo el ecosistema, asegurando que cada módulo sea independiente y eficiente.