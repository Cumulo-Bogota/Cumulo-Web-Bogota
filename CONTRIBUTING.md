# Cómo Contribuir

Si estás leyendo esto, probablemente hagas parte de Cúmulo VIP y tengas la tarea de mantener este sitio web, o tal vez simplemente quieras aportar a su desarrollo o incluso hacer correcciones. Dependiendo de qué tan profundas sean las modificaciones necesitarás saber más o menos cosas, pero aquí encontrarás todo lo necesario.

## Índice

- [Edición básica](#edición-básica)
- [Edición avanzada](#edición-avanzada)
- [Committing changes](#committing-changes)


---

## Edición básica

Consiste en

- Corregir errores de ortografía
- Mejorar la redacción
- Agregar nuevo contenido (texto o imágenes)

Puedes editar el contenido directamente desde GitHub o desde tu dispositivo, para ello necesitarás una cuenta y permisos de escritura, para obtenerlos puedes contactar al administrador del sitio.

### Editando desde GitHub

Sigue estos pasos

1. Navega hasta el archivo que desees editar
2. Haz clic en *Edit* (✏️) y realiza tus cambios
3. Revisa tus cambios en *Preview* 
4. Una vez estés conforme, debes guardar los cambios en un *Commit*, para ello haz clic en *Commit Changes...*, escribe un mensaje siguiendo la estructura explicada en [esta guía](#committing-changes) y listo!


---

## Edición avanzada

Consiste en

- Modificar la estructura de la página (HTML)
- Cambiar los estilos de algún elemento (CSS) (colores, fuentes, tamaños, dimensiones, disposición en el espacio, etc.)
- Añadir nuevas funcionalidades (scripts de JavaScript)

Seguramente querrás ver como afectan tus cambios al resultado final, por lo que se recomienda que instales herramientas como un editor de texto plano (Visual Studio Code, Sublime Text, Neovim), Git, Ruby y jekyll, esto varía dependiendo de la plataforma:

**Windows** 
- Windows Package Manager CLI: `winget install RubyInstallerTeam.Ruby.{MAJOR}.{MINOR}` (`MAJOR` y `MINOR` corresponden a la versión, e.g. 3.2) 
- Chocolatey Package Manager: `choco install ruby` 
- [Ruby Installer](https://rubyinstaller.org/), [Git](https://git-scm.com/install/)

**Linux** 

- Arch Linux: `sudo pacman -S code git ruby` 
- Debian: `sudo apt-get install git ruby-full` 
- Mint: `` 
- Ubuntu: `sudo apt-get install git ruby-full` 

**Android** 
```bash
pkg install neovim git ruby
```

Asegurate de tener a Git y Ruby en tu PATH, luego desde una terminal (CMD, Alacritty, GNOME terminal, Kitty, Termux, etc.) ejecuta en la ubicación deseada el comando
```bash
git clone https://github.com/Cumulo-Bogota/Cumulo-Web-Bogota.git
```
para clonar los archivos de la página web en tu máquina, luego entra al directorio creado con 
```bash
cd Cumulo-Web-Bogota
```
también será necesario correr
```bash
gem install bundler jekyll
```
una vez terminado corre el siguiente comando en el directorio del proyecto
```bash
bundle exec jekyll serve --config _config.yml,_config_dev.yml --port 4000 --livereload
```
y en cualquier navegador accede a la dirección `127.0.0.1:4000` 

Cada vez que guardes cambios localmente la página se actualizará de manera automática, una vez termines de realizar los cambios súbelos a GitHub.


---

## Committing changes

Algunas convenciones a tener en cuenta

- `config` para cambios en la configuración del sitio
- `docs` para cambios en la documentación
- `feat` para nuevas funcionalidades
- `fix` para arreglos
- `looks` para cambios en el CSS o el diseño gráfico en general
- `new` para nuevos archivos agregados
- `refactor` para re-estructuraciones del código
- `style` para ajustes estilísticos del código (indentaciones, espacios)

intenta mantener los mensajes de los commits cortos y descriptivos.
