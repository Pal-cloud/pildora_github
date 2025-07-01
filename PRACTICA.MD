# Práctica: Tu Primer Pull Request en GitHub

¡Bienvenido/a a la sección de práctica! Este documento te guiará a través de los pasos fundamentales para realizar tu primer Pull Request (PR) en GitHub. Un PR es la forma estándar de contribuir a proyectos de código abierto o de colaborar en equipos.

**Objetivo:** Modificar un archivo en un repositorio ajeno (o propio para practicar, así te puedes ganar la insignias del pull shark) y proponer tus cambios para que sean integrados.

---

## Pasos para Realizar un Pull Request

Sigue estos pasos detallados para completar tu práctica. Te recomendamos tener el PDF "Hitgub: insignias, logros y pull requests" a mano, ya que complementa esta guía con explicaciones más profundas.

### 1. **Encuentra un Repositorio para Practicar**

Para esta práctica, puedes usar un repositorio simple que permita contribuciones, o incluso crear uno propio para simular el proceso.

**Sugerencia:** Si no tienes uno, puedes buscar repositorios de "first-timers-only" o "good first issue" en GitHub, o simplemente crear un repositorio de prueba en tu propia cuenta.

### 2. **Haz un "Fork" del Repositorio**

* **¿Qué es un Fork?** Es una copia personal de un repositorio que se guarda en tu propia cuenta de GitHub. Esto te permite hacer cambios sin afectar el repositorio original.
* **Cómo hacerlo:**
    1.  Ve a la página principal del repositorio en GitHub que quieres practicar.
    2.  Busca el botón **"Fork"** (normalmente en la esquina superior derecha de la página) y haz clic en él.
    3.  Confirma la creación del fork. Ahora tendrás una copia del repositorio en tu perfil (ej. `tu_usuario/nombre_del_repositorio`).

### 3. **Clona tu Fork a tu Máquina Local**

Ahora que tienes tu propia copia (fork) del repositorio, la descargarás a tu computadora para poder trabajar en ella.

* **Cómo hacerlo:**
    1.  En tu fork de GitHub, haz clic en el botón verde **"Code"**.
    2.  Copia la URL HTTPS (o SSH si ya lo tienes configurado).
    3.  Abre tu terminal (Git Bash, CMD, PowerShell).
    4.  Navega a la carpeta donde quieres guardar el proyecto (ej. `cd Documentos/GitHub_Proyectos`).
    5.  Ejecuta el comando `git clone` seguido de la URL que copiaste:
        ```bash
        git clone [https://github.com/tu_usuario/nombre_del_repositorio.git](https://github.com/tu_usuario/nombre_del_repositorio.git)
        ```
    6.  Navega al directorio del repositorio clonado:
        ```bash
        cd nombre_del_repositorio
        ```

### 4. **Crea una Nueva Rama (Branch)**

Es una buena práctica crear una nueva rama para tus cambios, en lugar de trabajar directamente en la rama `main` (o `master`). Esto mantiene tu trabajo organizado y facilita la gestión de los PRs.

* **Cómo hacerlo:**
    1.  En tu terminal, dentro del directorio del repositorio, crea una nueva rama:
        ```bash
        git checkout -b mi-nueva-caracteristica
        ```
        (Puedes reemplazar `mi-nueva-caracteristica` por un nombre descriptivo de tus cambios, ej. `añadir-saludo`, `corregir-typo`).
    2.  Verifica que estás en la nueva rama:
        ```bash
        git branch
        ```
        (Deberías ver un asterisco `*` junto al nombre de tu nueva rama).

### 5. **Realiza tus Cambios**

Ahora es el momento de hacer las modificaciones que quieres proponer.

* **Cómo hacerlo:**
    1.  Abre los archivos del repositorio en tu editor de texto favorito (VS Code, Sublime Text, Notepad++, etc.).
    2.  Realiza los cambios que desees. Por ejemplo, puedes añadir una línea de texto a un archivo `README.md` existente, corregir un error tipográfico, o añadir un nuevo archivo simple.
    3.  **Guarda los cambios** en tu editor.

### 6. **Añade y Confirma tus Cambios (Add & Commit)**

Git necesita saber qué cambios quieres guardar y por qué.

* **Cómo hacerlo:**
    1.  En tu terminal, verifica los cambios que has hecho:
        ```bash
        git status
        ```
        (Verás los archivos modificados en rojo).
    2.  Añade los archivos modificados al "staging area" (área de preparación):
        ```bash
        git add .
        # O git add nombre_del_archivo_modificado.ext
        ```
    3.  Confirma los cambios con un mensaje descriptivo (el "commit message"):
        ```bash
        git commit -m "Añadir saludo de bienvenida a la práctica de PR"
        ```

### 7. **Sube tus Cambios a tu Fork en GitHub (Push)**

Tus cambios están guardados localmente. Ahora necesitas subirlos a tu fork en GitHub.

* **Cómo hacerlo:**
    ```bash
    git push origin mi-nueva-caracteristica
    # Reemplaza 'mi-nueva-caracteristica' por el nombre de tu rama
    ```
    Si es la primera vez que subes esta rama, Git podría pedirte que uses `--set-upstream origin mi-nueva-caracteristica`.

### 8. **Crea el Pull Request (PR)**

¡Este es el paso final para proponer tus cambios al repositorio original!

* **Cómo hacerlo:**
    1.  Una vez que hayas hecho `git push`, GitHub te mostrará un mensaje en tu terminal con un enlace directo para crear el PR. Si no lo ves, ve a tu fork en GitHub.
    2.  En la página de tu fork, verás un recuadro o un botón que dice **"Compare & pull request"** o "Contribute". Haz clic en él.
    3.  **Revisa los cambios:** Asegúrate de que los cambios que se muestran son los que quieres proponer.
    4.  **Escribe un Título y Descripción:**
        * **Título del PR:** Debe ser conciso y claro (ej., "Feat: Añadir mensaje de bienvenida" o "Fix: Corregir error tipográfico en README").
        * **Descripción del PR:** Explica en detalle qué cambios has hecho y por qué. Si el PR resuelve un `Issue` existente, puedes enlazarlo aquí (ej. `Closes #123`).
    5.  Haz clic en el botón verde **"Create pull request"**.

---

¡Felicidades! Has creado tu primer Pull Request. Ahora el mantenedor del repositorio original puede revisar tus cambios, hacer comentarios y, si todo está bien, fusionarlos con el repositorio principal.

---

## ¡Tu Feedback es Importante!

Si tienes alguna pregunta durante esta práctica o encuentras alguna dificultad, por favor, abre un `Issue` en este repositorio o contacta al creador. ¡Tu experiencia nos ayuda a mejorar!
