# Manual en Markdown: Cómo Instalar Python en Windows 11 (Referencia al vídeo de Tutoliber)

> Basado en el video “[#1 CÓMO INSTALAR PYTHON Windows 11 en 2025 | Paso a Paso para Novatos](https://www.youtube.com/watch?v=9NXl3KMWnjo)” de Tutoliber[1].



[![Cómo instalar Python en Windows 11 (2025) | Tutoliber](https://img.youtube.com/vi/9NXl3KMWnjo/hqdefault.jpg)](https://www.youtube.com/watch?v=9NXl3KMWnjo)



## Tabla de Contenido
- [Introducción](#introducción)
- [Descargar el Instalador de Python](#descargar-el-instalador-de-python)
- [Instalar Python en Windows 11](#instalar-python-en-windows-11)
- [Configurar Variable de Entorno](#configurar-variable-de-entorno)
- [Verificar la Instalación](#verificar-la-instalación)
- [Comprobar Python en la Terminal](#comprobar-python-en-la-terminal)
- [Código para Embeber el Video en GitHub](#código-para-embeber-el-video-en-github)

***

## Introducción

Este manual está dirigido a principiantes y explica paso a paso cómo instalar **Python** en **Windows 11**. Es ideal si deseas comenzar a programar, hacer análisis de datos o desarrollar proyectos con Python.[1]

***

## Descargar el Instalador de Python

1. Abre tu navegador favorito.
2. Ve a la página oficial: [https://www.python.org](https://www.python.org).
3. Haz clic en la pestaña **Downloads** o **Descargas**.
4. Descarga la última versión de Python para Windows (por ejemplo, “Download Python 3.13”).
5. Guarda el archivo en una carpeta fácil de ubicar (como "Descargas").[1]

***

## Instalar Python en Windows 11

1. Busca el archivo descargado en tu computadora.
2. Da **doble clic** sobre el instalador para abrirlo.
3. Marca las siguientes opciones antes de instalar:
    - **Add Python to PATH** (Añadir Python a la variable de entorno)
    - **Use admin privileges** (Usar privilegios de administrador para la instalación)
4. Haz clic en **Install Now**.
5. Espera a que termine la instalación. Verás un mensaje indicando que se completó exitosamente.[1]

***

## Configurar Variable de Entorno

Si olvidaste marcar "Add Python to PATH" durante la instalación:
- Abre el menú de búsqueda y busca "Variables de entorno".
- Edita la variable de entorno `Path` agregando la ruta donde está instalado Python (ejemplo: `C:\Users\TuUsuario\AppData\Local\Programs\Python\Python3x\` y la subcarpeta `Scripts`).
- Guarda los cambios y reinicia la terminal.[1]

***

## Verificar la Instalación

1. Haz clic en el ícono de **buscar** en la barra de tareas de Windows.
2. Escribe `cmd` para abrir la terminal de Windows (símbolo de sistema).
3. En la terminal, escribe:

   ```
   python
   ```

4. Si la instalación fue correcta, aparecerá la versión de Python y los tres símbolos `>>>`, indicando que puedes empezar a programar.[1]

***

## Comprobar Python en la Terminal

Puedes probar un primer programa sencillo, escribiendo:

```python
print("Hello World")
```

Si ejecuta correctamente y ves `Hello World` en pantalla, tu instalación está lista para usarse.[1]

***
