# Garcia-s
Sistema_De_Gestion_De_Biblioteca

## 1. Descripción del Caso de Uso
El sistema es una web diseñada para optimizar el control del inventario bibliográfico, facilitando el registro, préstamo y devolución de libros en una biblioteca. Su objetivo es mejorar la experiencia del personal administrativo y reducir los errores en el control de existencias.

---

## 2. Objetivos
* **2.1.** Administrar de forma eficiente el estado de los libros (disponible, prestado).
* **2.2.** Autorizar el registro de libros (título, autor, año, código único) y la gestión de usuarios.
* **2.3.** Garantizar la seguridad mediante la autenticación y el respaldo automático de datos (RNF3).

---

## 3. Requerimientos Esenciales
A continuación, se resumen los requerimientos funcionales (RF) y no funcionales (RNF) clave del sistema:

| Tipo | ID | Descripción (v2) |
| :--- | :--- | :--- |
| **Funcional** | RF1 | Registrar nuevos libros y sus metadatos. |
| **Funcional** | RF2 | Registrar préstamos y devoluciones (con validación de estado). |
| **No Funcional**| RNF1 | Requiere **autenticación** con usuario y contraseña para funciones administrativas. |
| **No Funcional**| RNF3 | Generación de copias de seguridad **diarias y automáticas**. |

---

## 4. Tabla de Pruebas
Se verifica la trazabilidad entre el requerimiento y el resultado esperado:

| ID Prueba | Requerimiento | Caso de Prueba | Resultado Esperado |
| :--- | :--- | :--- | :--- |
| **PT-001** | RF1 | Registro exitoso de un nuevo libro. | Libro registrado exitosamente en la base de datos. |
| **PT-002** | RF2 | Registro de préstamo de libro disponible. | Préstamo registrado y libro marcado como "prestado". |
| **PT-003** | RF3 | Registro de devolución de un libro prestado. | Estado del libro cambia a "disponible". |

---

## 5. Propuesta de Mantenimiento
Se propone un Mantenimiento Correctivo y Preventivo para asegurar la integridad de los datos:

* **Correctivo:** Eliminar el defecto lógico que permite prestar un libro que ya está prestado (inconsistencia de estado).
* **Preventivo:** Fortalecer la lógica de devolución (RF3) para garantizar que la actualización del estado del libro sea 100% fiable.

---

## 6. Reflexión sobre el Control de Versiones de Git
El control de versiones de Git es fundamental para la documentación técnica (DRS, Plan de Pruebas y README) porque garantiza la trazabilidad y la confiabilidad. Permite ubicar la evolución de los requerimientos desde la v1 a la v2 y auditar exactamente cuándo y por qué se aprobaron o modificaron las especificaciones, lo cual es vital para el mantenimiento futuro.
