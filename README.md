# Ejercicio de Ramificaciones y Fusiones en Git

Este repositorio es un ejemplo práctico de cómo utilizar ramificaciones y fusiones en Git para manejar múltiples tareas en un proyecto de desarrollo web. El ejercicio simula un flujo de trabajo común en el que se trabaja en una nueva funcionalidad mientras se resuelve un problema crítico.

## Pasos realizados

1. **Inicialización del repositorio**:
   - Se creó un repositorio Git y se añadió un archivo `index.html` como base del sitio web.

2. **Creación de una rama para una nueva funcionalidad**:
   - Se creó la rama `nueva-funcionalidad` para desarrollar una nueva característica (página "Acerca de nosotros").

3. **Manejo de un problema crítico**:
   - Se recibió una llamada informando de un problema crítico.
   - Se cambió a la rama `main` y se creó una nueva rama llamada `hotfix-problema-critico` para solucionar el problema.
   - Se corrigió el error en `index.html` y se fusionó la rama `hotfix-problema-critico` en `main`.

4. **Regreso a la nueva funcionalidad**:
   - Se volvió a la rama `nueva-funcionalidad` para continuar con el desarrollo de la nueva característica.
   - Se añadió una página "Contacto" y se fusionaron los cambios de `main` para incluir la corrección crítica.

5. **Fusión final**:
   - Una vez completada la nueva funcionalidad, se fusionó la rama `nueva-funcionalidad` en `main`.

## Estructura del repositorio

- `index.html`: Página de inicio del sitio web.
- `about.html`: Página "Acerca de nosotros" (nueva funcionalidad).
- `contact.html`: Página "Contacto" (nueva funcionalidad).

## Comandos utilizados

A continuación, se muestran los comandos más importantes que se utilizaron durante el ejercicio:

```bash
# Inicializar el repositorio
git init

# Crear el primer commit
echo "<h1>Bienvenido al sitio web</h1>" > index.html
git add index.html
git commit -m "Primer commit: sitio web inicial"

# Crear una rama para la nueva funcionalidad
git checkout -b nueva-funcionalidad

# Añadir página "Acerca de nosotros"
echo "<h1>Acerca de nosotros</h1>" > about.html
git add about.html
git commit -m "Añadir página 'Acerca de nosotros'"

# Cambiar a la rama main para manejar el problema crítico
git checkout main

# Crear una rama para el hotfix
git checkout -b hotfix-problema-critico

# Corregir el error en index.html
echo "<h1>Bienvenido al sitio web (corregido)</h1>" > index.html
git add index.html
git commit -m "Corregir error crítico en la página de inicio"

# Fusionar el hotfix en main
git checkout main
git merge hotfix-problema-critico

# Volver a la rama de la nueva funcionalidad
git checkout nueva-funcionalidad

# Fusionar main en nueva-funcionalidad para incluir la corrección
git merge main

# Añadir página "Contacto"
echo "<h1>Contacto</h1>" > contact.html
git add contact.html
git commit -m "Añadir página 'Contacto'"

# Fusionar nueva-funcionalidad en main (opcional)
git checkout main
git merge nueva-funcionalidad
