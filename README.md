# TrunkBasedDevelopment

# 💻 Propuesta para la Gestión de Código en Microservicios usando Trunk Based Development (TBD)

El desarrollo basado en troncos es una práctica de gestión de control de versiones en la que los desarrolladores fusionan pequeñas actualizaciones de forma frecuente en un "tronco" o rama principal.
El desarrollo basado en troncos es una práctica obligatoria de la CI y la CD. Permite a los desarrolladores crear ramas de corta duración con pequeñas confirmaciones, a diferencia de otras estrategias de ramas de funciones de larga duración.

## Estructura de Ramas 

### Rama Principal
- `main` como la rama principal. Esta rama siempre debe estar en un estado de despliegue listo, y todos los cambios deben ser integrados aquí después de haber sido revisados y probados adecuadamente.
### Ramas de Funcionalidad
- Crea ramas cortas y de vida breve para el desarrollo de nuevas funcionalidades. Nombrar estas ramas usando el prefijo `feature` seguido de una breve descripción de la funcionalidad:
- `feature/nueva-funcionalidad`
### Ramas de Corrección de Errores
- Para la corrección de errores, usa el prefijo `bugfix` seguido de una breve descripción del error a corregir:
- `refactor/mejora-rendimiento`
### Ramas de Hotfix
- Para solucionar problemas críticos en producción, usa el prefijo `hotfix`:
- `hotfix/parche-urgente
- Estas ramas son utilizadas únicamente para resolver problemas urgentes y deben fusionarse a `main` inmediatamente después de la corrección.
### Convenciones de Nombres
- Usa nombres descriptivos y consistentes para servicios y ramas.
- Evita abreviaciones y nombres ambiguos.
### Pruebas y CI/CD
- Pruebas
  Implementa pruebas unitarias para asegurar que cada componente funcione correctamente.
  Implementa pruebas de integración para asegurar que los componentes funcionen bien juntos.
- CI/CD
  Usa herramientas de CI/CD (GitHub Actions) para automatizar el proceso de integración y despliegue.
  Utiliza despliegues continuos (Continuous Deployment) cuando sea posible, para mantener el software siempre listo para ser lanzado.
## Buenas Prácticas 
- Pequeños Commits: Realiza commits pequeños y frecuentes para facilitar la revisión y el rastreo de cambios.
- Revisiones de Código: Realiza revisiones de código (code reviews) sistemáticas para mejorar la calidad del código y compartir conocimiento entre el equipo.
- Documentación: Documenta las funcionalidades y cambios importantes en el código y en las herramientas de documentación del proyecto.
- Seguridad: Asegura que las prácticas de seguridad estén integradas en el desarrollo y despliegue, incluyendo la gestión de secretos y la configuración segura de los servicios.
## Reglas de Versionamiento
- Versión Inicial (0.y.z):
  Durante el desarrollo inicial, se utiliza la versión 0.y.z. En esta etapa, todo puede cambiar sin previo aviso, por lo que es común que se vean incrementos en el número menor (`y`) y de parche (`z`).
- Cambio Mayor:
  Cuando realices un cambio que rompe la compatibilidad con versiones anteriores, incrementa el número mayor (`x`):
    Ejemplo: `1.0.0` a `2.0.0`
- Cambio Menor:
  Cuando añadas una nueva funcionalidad de manera retrocompatible, incrementa el número menor (`y`):
    jemplo: `1.1.0` a `1.2.0`
- Corrección de Errores:
  Cuando realices correcciones de errores que no afectan la compatibilidad con versiones anteriores, incrementa el número de parche (`z`):
    Ejemplo: `1.1.1` a `1.1.2`



  
