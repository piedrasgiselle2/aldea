# Numeria — versión aula con Modo Docente

Esta versión integra:

- personaje persistente;
- progreso persistente;
- mapa de Numeria;
- lugares bloqueados y desbloqueados;
- Modo Docente;
- códigos de apertura para habilitar misiones clase a clase.

## Cómo funciona

### Estudiantes

El personaje se guarda en:

`numeria_player`

El progreso general se guarda en:

`numeria_progress`

Aunque cierren el navegador, el personaje y los lugares ya desbloqueados permanecen en ese dispositivo mientras no se borren los datos del navegador.

### Modo Docente

El PIN inicial es:

`3141`

Podés cambiarlo en `script.js` buscando:

`const TEACHER_PIN = "3141";`

Desde Modo Docente podés ver el código correspondiente a cada lugar. Compartís el código recién cuando quieras habilitar esa misión.

Ejemplo:

- Granja → `TRIGO-21`
- Laboratorio → `POCION-34`
- Herrería → `HIERRO-47`
- Mercado → `MONEDA-58`
- Feria Real → `FERIA-69`
- Castillo → `CORONA-82`

Los estudiantes escriben el código en el mapa y el lugar queda desbloqueado en su navegador.

## Importante: límite de GitHub Pages

GitHub Pages es una web estática. No existe una base central que permita que la docente haga clic una vez y automáticamente se actualicen todos los dispositivos.

Por eso esta versión usa **códigos de apertura**: vos decidís cuándo compartirlos.

Para un control central real —por ejemplo, que desde tu computadora habilites “Laboratorio” y aparezca automáticamente en los 30 dispositivos— hace falta agregar una base de datos como Firebase o Supabase.

## Seguridad

El PIN del Modo Docente en una web estática sirve para evitar accesos accidentales, pero no es seguridad fuerte porque el código fuente del sitio es público.

Para una implementación escolar ordinaria suele ser suficiente como control pedagógico. Para seguridad real se necesita autenticación y backend.

## Publicar en GitHub Pages

1. Creá un repositorio.
2. Subí `index.html`, `styles.css`, `script.js` y `README.md`.
3. Settings → Pages.
4. Deploy from a branch.
5. Seleccioná `main` y `/root`.
6. Guardá.
