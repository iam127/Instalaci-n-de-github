1. Crear un repositorio en GitHub

Ve a GitHub
 → botón New repository.

Ponle un nombre (ejemplo: mi_proyecto_django).

Opcional: añade una descripción.

Decide si será público o privado.

No marques nada más (ni README, ni .gitignore, ni licencia).

Haz clic en Create repository.

2. Preparar tu proyecto localmente

Abre una terminal en la carpeta raíz de tu proyecto Django (donde está el manage.py).

Ejecuta:

git init
git branch -M main
git add .
git commit -m "Primer commit - Proyecto Django"

3. Conectar con GitHub

En tu nuevo repositorio de GitHub verás una URL parecida a:

🔹 HTTPS:

git remote add origin https://github.com/TU_USUARIO/mi_proyecto_django.git


🔹 SSH (si configuraste llaves SSH):

git remote add origin git@github.com:TU_USUARIO/mi_proyecto_django.git

4. Subir el proyecto
git push -u origin main

5. Archivos recomendados a ignorar

Crea un archivo .gitignore en la raíz y pon:

# Entornos virtuales
venv/
.env/

# Archivos de compilación Python
__pycache__/
*.pyc
*.pyo

# Archivos de Django
db.sqlite3
media/
staticfiles/

# Configuración del IDE
.vscode/
.idea/


_________________CAMBIO_______________________________

🔹 Ver tu configuración actual

En la terminal escribe:

git config --global user.name
git config --global user.email

🔹 Cambiar los datos a los de tu GitHub

Configura tu nombre y correo igual a los de tu cuenta de GitHub:

git config --global user.name "TuNombreDeUsuario"
git config --global user.email "tu_correo_de_github@example.com"


⚠️ Importante: El correo debe ser el que aparece en GitHub → Settings → Emails.
(Si usas la opción de "Keep my email addresses private", GitHub te da un correo estilo 12345678+usuario@users.noreply.github.com y puedes usar ese).

🔹 Configuración solo para un proyecto (opcional)

Si no quieres cambiarlo en toda tu PC, solo en tu proyecto Django:

git config user.name "TuNombreDeUsuario"
git config user.email "tu_correo_de_github@example.com"

🔹 Confirmar los cambios

Cada commit nuevo llevará tu nombre y correo correctos.
Puedes revisar con:

git log

_______________________________________COOMMIT___________________

git status
git add .
git commit -m "Creación del proyecto Django con configuración inicial"
git push origin main
