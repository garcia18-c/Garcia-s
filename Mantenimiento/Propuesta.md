# Propuesta de Mantenimiento para Sistema de Gestión de Biblioteca

## 1. Tipo de Mantenimiento Propuesto
**Correctivo y Preventivo**.

## 2. Justificación
* **Correctivo:** Se requiere corregir el **defecto lógico** principal: la posibilidad de registrar un préstamo (RF2) de un libro cuyo estado ya es "prestado", causando inconsistencia en la base de datos.
* **Preventivo:** Se necesita fortalecer el módulo de devolución (RF3) para **garantizar** que el estado del libro cambie siempre de forma correcta y confiable a "disponible".

## 3. Tareas Clave
1. **Validación Correctiva:** Implementar una **validación estricta** antes de registrar un préstamo (RF2) que rechace la solicitud si el libro no está en estado "disponible".
2. **Fortalecimiento Preventivo:** Revisar la función de devolución (RF3) para asegurar la **actualización confiable** del estado del libro a "disponible".
