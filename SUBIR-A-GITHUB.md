# Cómo subir el prototipo de VeloKliniK a GitHub y obtener el enlace público

Repositorio de destino (ya creado, vacío): https://github.com/JoanMarti/veloklinik-prototipo

Enlace público final: **https://joanmarti.github.io/veloklinik-prototipo/**

## Qué hay en el paquete

| Archivo | Para qué sirve |
|---|---|
| `veloklinik-prototipo.zip` | Solo los archivos del proyecto (sin historial git). Ideal para subir desde la web de GitHub arrastrando. |
| `veloklinik-prototipo-v2-repo.tar.gz` | El proyecto como repositorio git, con 2 commits y el remoto ya configurado. Ideal para subir desde la terminal. |

Contenido del proyecto:

```
index.html          Página completa
README.md           Descripción del proyecto
assets/
  hero.jpg          Foto del héroe
  europaallee.jpg   Foto de la sucursal Europaallee
  altstetten.jpg    Foto de la sucursal Altstetten
  sattel.jpg        Foto de la sucursal Sattel
```

Ignora el archivo `veloklinik-prototipo-repo.tar.gz` (sin "v2"): es la primera versión del prototipo.

---

## Opción A — Desde la web de GitHub (sin terminal)

1. Descomprime `veloklinik-prototipo.zip`. Deben quedar `index.html`, `README.md` y la carpeta `assets`.
2. Abre https://github.com/JoanMarti/veloklinik-prototipo y pulsa **uploading an existing file**.
3. Arrastra `index.html`, `README.md` y la carpeta `assets` completa a la ventana. No arrastres el `.zip`: GitHub no lo descomprime.
4. Espera a que terminen de subirse las 4 fotos, escribe un mensaje de commit (por ejemplo, "Prototipo VeloKliniK v2") y pulsa **Commit changes**.

## Opción B — Desde la terminal (conserva el historial)

1. Descomprime el paquete:
   ```bash
   tar -xzf veloklinik-prototipo-v2-repo.tar.gz
   cd veloklinik-prototipo
   ```
   En Windows 10 y 11 el comando `tar` ya viene incluido.
2. Sube el proyecto. El remoto ya apunta a tu repositorio, así que basta con:
   ```bash
   git push -u origin main
   ```
   Si el remoto no estuviera configurado:
   ```bash
   git remote add origin https://github.com/JoanMarti/veloklinik-prototipo.git
   git push -u origin main
   ```
3. Si GitHub pide credenciales, usa tu usuario y un *personal access token* (no la contraseña de la cuenta), o inicia sesión con GitHub CLI (`gh auth login`).

---

## Activar el enlace público (GitHub Pages)

Este paso es igual con las dos opciones.

1. En el repositorio, abre **Settings → Pages**.
2. En *Build and deployment*, elige **Source: Deploy from a branch**.
3. Selecciona la rama **main** y la carpeta **/ (root)**, y pulsa **Save**.
4. Espera 1 o 2 minutos y recarga la página de Pages: aparecerá el aviso *Your site is live at…*.
5. Abre https://joanmarti.github.io/veloklinik-prototipo/ y comprueba que se ven el héroe, las fotos de las tres sucursales y el selector de idiomas.

El repositorio tiene que ser **público** para que cualquier persona pueda abrir el enlace sin iniciar sesión en GitHub (en cuentas gratuitas, Pages solo funciona con repositorios públicos).

---

## Antes de enviárselo al cliente

- **Fotos:** el héroe es de otro taller y las de las sucursales vienen de Google Maps o de capturas. Sirven como referencia del prototipo, pero conviene sustituirlas por fotos propias de VeloKliniK. Para hacerlo, reemplaza los archivos de `assets/` conservando el nombre.
- **Horarios y reseñas:** los horarios son de ejemplo y las reseñas son ficticias (están etiquetadas como tal en la web). Hay que cambiarlos por datos reales antes de una publicación final.
- **Repositorio público:** cualquiera con el enlace verá también el código y las fotos del repositorio.
- **Actualizar la web más adelante:** sube de nuevo los archivos cambiados (arrastrándolos en la web de GitHub o con `git add`, `git commit` y `git push`). Pages se actualiza solo en uno o dos minutos.
