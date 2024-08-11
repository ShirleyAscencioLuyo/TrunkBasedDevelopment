🌲 Trunk Based Development (TBD) para la Gestión de Código en Microservicios
📋 Introducción
El Trunk Based Development (TBD) es una metodología de control de versiones en la cual los desarrolladores integran pequeñas actualizaciones de código de manera frecuente en una rama principal o "tronco". Esta práctica es esencial para implementar Integración Continua (CI) y Despliegue Continuo (CD), permitiendo que las ramas sean de corta duración con cambios pequeños y manejables. A diferencia de las estrategias tradicionales de ramas largas, el TBD reduce riesgos y facilita el despliegue rápido y seguro.

🌳 Estructura de Ramas
🏷️ Rama Principal (main)
Descripción: La rama main es el núcleo del proyecto, siempre debe estar en un estado listo para producción. Todos los cambios, ya sean nuevas funcionalidades o correcciones de errores, deben integrarse aquí después de una revisión y pruebas exhaustivas.
🛠️ Ramas de Funcionalidad (feature/*)
Propósito: Desarrollar nuevas características.
Convención de Nombre: feature/nombre-descriptivo
Ejemplo: feature/integracion-login
Duración: Estas ramas deben ser de corta vida, cerrándose una vez que la funcionalidad ha sido integrada en main.
🐞 Ramas de Corrección de Errores (bugfix/*)
Propósito: Corregir errores existentes.
Convención de Nombre: bugfix/nombre-descriptivo
Ejemplo: bugfix/correccion-bug-login
Duración: Se utilizan para resolver problemas antes de que el código llegue a producción.
🔥 Ramas de Hotfix (hotfix/*)
Propósito: Solucionar problemas críticos directamente en producción.
Convención de Nombre: hotfix/nombre-descriptivo
Ejemplo: hotfix/parche-seguridad-critico
Duración: Estas ramas se crean solo para resolver problemas urgentes y se fusionan inmediatamente a main.
🧑‍💻 Buenas Prácticas
🔄 Pequeños Commits
Realiza commits pequeños y frecuentes para facilitar la revisión y el rastreo de cambios. Esto también ayuda a detectar problemas más rápidamente.
👩‍💻👨‍💻 Revisiones de Código
Implementa revisiones de código (code reviews) sistemáticas para mejorar la calidad del código y fomentar el intercambio de conocimientos entre los miembros del equipo.
🗒️ Documentación
Asegúrate de documentar todas las funcionalidades nuevas y los cambios importantes. Mantén la documentación actualizada y accesible para todos los desarrolladores.
🔐 Seguridad
Incorpora prácticas de seguridad desde el inicio, como la gestión de secretos y la configuración segura de servicios. Las revisiones de seguridad deben ser parte del flujo de trabajo.
🔄 Pruebas y CI/CD
🧪 Pruebas
Unitarias: Aseguran que cada componente funcione correctamente por separado.
Integración: Verifican que los diferentes componentes del sistema funcionen correctamente juntos.
🚀 CI/CD
Herramientas: Utiliza GitHub Actions para automatizar el proceso de integración y despliegue.
Despliegue Continuo: Cuando sea posible, implementa despliegue continuo para mantener el software en un estado listo para producción.
🔢 Reglas de Versionamiento
Versión Inicial (0.y.z)
Uso: Durante la fase de desarrollo inicial, se usa la versión 0.y.z. Todo puede cambiar sin previo aviso, y es común que se incrementen tanto el número menor (y) como el de parche (z).
Cambio Mayor
Uso: Cuando realices un cambio que rompa la compatibilidad con versiones anteriores, incrementa el número mayor (x).
Ejemplo: 1.0.0 a 2.0.0.
Cambio Menor
Uso: Cuando añadas nuevas funcionalidades de manera retrocompatible, incrementa el número menor (y).
Ejemplo: 1.1.0 a 1.2.0.
Corrección de Errores
Uso: Para correcciones de errores que no afectan la compatibilidad, incrementa el número de parche (z).
Ejemplo: 1.1.1 a 1.1.2.
