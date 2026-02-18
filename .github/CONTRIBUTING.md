# Reglas para contribuir

![Workflow](assets/AyPS.png)

El espacio de trabajo puede dividirse en tres áreas:

1. **Upstream**: es el repositorio de la clase, solo los profesores tienen acceso directo a colaborar y modificar los elementos del repositorio. Aqui se crean las ramas asociadas a tareas (*Issues*) que se deberán resolver mediante *Pull Requests*.
2. **Origin**: es el **Fork** del proyecto. Desde este repositorio se harán los *Pull Request* para darle solución a los *Issues*. Sirve como respaldo del trabajo realizado en **Local** para poder trabajar en otras computadoras.
3. **Local**: es el clon del proyecto en la computadora local. Este se gestiona con Git y es donde se editan los archivos, se resuelven conflictos y se crean las ramas *develop* para no interferir en el trabajo de los demas.

# Flujo de Trabajo (Workflow)

Este proyecto utiliza un esquema de **Fork & Pull**. Todos los colaboradores trabajan en sus propias copias y proponen cambios al repositorio central mediante Pull Requests.




1. **Sincronizar**: Antes de empezar, actualiza tu rama `main` local con el repositorio principal:
   ```bash
   git checkout main
   git pull upstream main
   git push origin main
   ```

   Existe la opción de primero sincronizar el **Fork** en Github y luego sincronizar con tu repositorio:
   ```bash
   git checkout main
   git pull origin main
   ```

2. **Crear rama**: Crea una rama para tu tarea (vinculada a un Issue de GitHub):
   ```bash
   git checkout -b feature/nombre-descriptivo
   ```

3. **Desarrollar y Publicar**: Despues de que termines de trabajar, has commit y sube tu trabajo a tu repositorio en Github
   ```bash
   git push origin feature/nombre-descriptivo
   ```
   Luego, abre un **Pull Request** en GitHub desde tu fork hacia el repositorio original: `alfjosue1997/Signal-Processing-2026-2`.

------------------------------------------------------------------------

# Normas de colaboración

## Recomendaciones Generales

-   **Limpieza**: No subir resultados numéricos masivos ni archivos temporales.
-   **Compatibilidad**: Mantener compatibilidad con la versión acordada de FreeFlyer.

## Estándar de Commits
Cada commit debe ser **atómico** (una sola tarea lógica) y seguir el formato de **Conventional Commits**:

`tipo: descripción breve en imperativo`

**Tipos comunes:**
- `feat`: Nueva funcionalidad (ej. `feat: agregar propagador J2`).
- `fix`: Corrección de un error (ej. `fix: corregir ruta relativa`).
- `docs`: Cambios en documentación.
- `style`: Formato (espacios, comas) sin cambios lógicos.
- `refactor`: Reestructuración de código sin cambiar funcionalidad.
- `test`: Añadir o corregir pruebas.
- `chore`: Tareas de mantenimiento (ej. `chore: actualizar .gitignore`).

## Manejo de Conflictos (.MissionPlan)
Los archivos de FreeFlyer guardan tanto la lógica como la configuración visual (zoom, posición de ventanas), lo que genera conflictos difíciles de resolver en Git.

1.  **Comunicación**: Avisa al equipo antes de modificar un Mission Plan central para evitar ediciones simultáneas.
2.  **Evitar "Ruido" Visual**: Si abres un archivo solo para revisar o consultar, **no guardes los cambios** al cerrar.
3.  **Limpieza**: Evita hacer commit de cambios que solo afecten a etiquetas de vista (ej. `<View>`, `<WindowPosition>`) si no has modificado la lógica.

## Estrategia de ramas

-   `main`: versión estable y validada
-   `feature/*`: desarrollo de nuevas capacidades
-   `analysis/*`: estudios exploratorios

------------------------------------------------------------------------

