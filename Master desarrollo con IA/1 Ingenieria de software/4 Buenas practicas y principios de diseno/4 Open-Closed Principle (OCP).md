**Categoría P.A.R.A:** #Arquitectura #Desarrollo #Diseño #SOLID #Metodologia 

**Temas Relacionados:** [[Arquitectura de Software]], [[Principios SOLID]], [[Deuda Técnica]], [[Patrones de Diseño]]

---

## 🧠 Conceptos Fundamentales (Definiciones Cortas)

- **Principio Abierto/Cerrado (OCP):** Directriz que establece que las entidades de software deben estar **abiertas para la extensión** pero **cerradas para la modificación**.
    
- **Extensibilidad:** Capacidad de un sistema para incorporar nuevos módulos o funcionalidades manteniendo el núcleo operativo intacto y protegido.
    
- **Soberanía Técnica:** Estado arquitectónico donde el coste marginal de añadir nuevas "features" es predecible y no compromete la integridad del negocio.
    
- **Código Frágil:** Software que requiere cambios en sus clases base para adaptarse a nuevas demandas, generando tests repetitivos y aumento de [[Deuda Técnica]].
    
- **Composición vs. Edición:** Transición de modificar código existente a ensamblar nuevos comportamientos mediante la "enchufe" de clases en estructuras validadas.
    

---

## 🛠️ Aplicación Técnica / Arquitectura

La implementación del OCP busca transformar la base de código en un sistema resiliente mediante las siguientes estrategias:

1. **Abstracción de Contratos:** Los arquitectos deben definir [[Interfaces]] o clases abstractas que actúen como contratos, permitiendo que el sistema espere comportamientos sin conocer su implementación específica.
    
2. **Uso de Patrones de Comportamiento:** Implementar patrones como **Strategy** o **Command** para permitir la variabilidad de la lógica de negocio sin alterar el flujo principal.
    
3. **Segregación de Comportamiento:** Aislar métodos específicos (ej. sistemas de pago o descuentos) para limitar el "radio de explosión" de errores, asegurando que un fallo en una extensión no afecte al núcleo global.
    
4. **Identificación de "Baterías de Cambios":** Detectar elementos con alta frecuencia de variación (impuestos, canales de notificación) para aplicarles el cierre técnico prioritariamente.
    
5. **Evitar la Sobreingeniería:** Aplicar abstracciones solo cuando exista una necesidad real de variabilidad, evitando complejizar componentes que no lo requieren.
    

---

## ❓ Preguntas de Autoevaluación

1. ¿Cómo redefine el OCP la "economía del desarrollo" en términos de asignación de recursos?
    
2. ¿Qué diferencia técnica existe entre la mentalidad de 'edición' y la de 'composición' según el texto?
    
3. ¿Cuál es el indicador principal para justificar la creación de una abstracción y evitar la sobreingeniería?
    
4. ¿Por qué se afirma que el OCP reduce el tiempo en los ciclos de QA?
    

---

## 🎯 Respuestas

1. Permite desplazar el esfuerzo del equipo: en lugar de dedicar el **80% de los recursos** a gestionar errores por cambios en el núcleo, estos se enfocan en crear valor real mediante nuevas variantes operativas.
    
2. La edición implica desmantelar procesos que ya funcionan (riesgoso), mientras que la composición se basa en "enchufar" nuevas clases a una estructura ya validada a través de contratos definidos.
    
3. La abstracción debe justificarse únicamente por una **necesidad real de variabilidad** identificada en los componentes.
    
4. Porque al priorizar la extensión sobre la modificación, se reduce drásticamente el tiempo dedicado a las **regresiones**, ya que el código estable permanece inalterado.