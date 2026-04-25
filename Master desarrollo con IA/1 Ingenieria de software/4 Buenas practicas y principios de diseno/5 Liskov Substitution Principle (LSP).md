**Categoría P.A.R.A:** #Arquitectura #Desarrollo #Diseño #SOLID #Metodologia

**Temas Relacionados:** [[Jerarquía de Clases]], [[Polimorfismo]], [[Contratos de Software]], [[Refactorización]]

---

## 🧠 Conceptos Fundamentales (Definiciones Cortas)

- **Principio de Sustitución de Liskov (LSP):** Norma que establece que una subclase debe ser intercambiable por su clase base sin alterar el comportamiento esperado ni la estabilidad del sistema.
    
- **Confianza Arquitectónica:** Estado en el que el diseño permite inyectar nuevas funcionalidades con la certeza de que los contratos establecidos no serán vulnerados.
    
- **Contrato Semántico:** Conjunto de expectativas sobre el comportamiento de un método (ej. que no lance excepciones inesperadas si la base promete éxito) que debe respetarse en toda la jerarquía.
    
- **Código Defensivo:** Lastre operativo consistente en validaciones constantes insertadas por temor a que una subclase rompa el sistema al ser utilizada.
    
- **Dilema del Cuadrado y el Rectángulo:** Ejemplo clásico donde una relación matemáticamente correcta falla arquitectónicamente si las restricciones de la subclase violan las propiedades de la clase base.
    

---

## 🛠️ Aplicación Técnica / Arquitectura

Para garantizar la sustituibilidad y evitar la fragilidad estructural, se deben seguir estos lineamientos:

- **Validación de Intercambiabilidad:** Realizar la pregunta crítica: ¿Es posible reemplazar el objeto base por este subtipo en cualquier parte del sistema sin añadir validaciones adicionales?.
    
- **Elevación de la Abstracción:** En lugar de "parchear" subclases con métodos vacíos o excepciones, se debe rediseñar la jerarquía separando comportamientos específicos en nuevas abstracciones (ej. separar aves que vuelan de las que nadan).
    
- **Uso de Interfaces Comunes:** Ante jerarquías forzadas, crear una interfaz base que capture solo los atributos o métodos realmente compartidos (ej. el área) para evitar forzar comportamientos no pertenecientes a la subclase.
    
- **Eliminación de Métodos Nulos:** Evitar la creación de métodos que solo sirven para cumplir un requisito de herencia pero que no ejecutan lógica o lanzan errores de "no implementado".
    

---

## ❓ Preguntas de Autoevaluación

1. ¿Por qué se considera que el cumplimiento del LSP es un requisito previo indispensable para aplicar el principio de Abierto/Cerrado (OCP)?
    
2. ¿Qué síntoma en el código indica que una jerarquía de clases ha sido forzada conceptualmente?
    
3. ¿Cómo afecta la violación del LSP a la velocidad de iteración de un equipo de desarrollo?
    
4. Desde una perspectiva de gestión de riesgos, ¿cuál es el peligro de lanzar excepciones en una subclase para métodos que la base define como exitosos?
    

---

## 🎯 Respuestas

1. Porque el polimorfismo es el motor de la extensibilidad; si las piezas no son intercambiables de forma segura (Liskov), extender el sistema mediante nuevas clases (OCP) generará errores impredecibles.
    
2. Cuando una subclase necesita anular un método del padre lanzando una excepción o dejándolo vacío porque el comportamiento no le corresponde.
    
3. La reduce significativamente, ya que obliga a los desarrolladores a conocer la implementación interna de cada componente para asegurar que el sistema no se rompa, en lugar de confiar en el contrato de la interfaz.
    
4. Representa una violación del contrato semántico que genera un comportamiento inesperado, convirtiendo la arquitectura en una fuente de fallos en lugar de un activo estratégico.