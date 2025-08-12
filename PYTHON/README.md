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

---

# Ejemplo Ejercicio Básico.

**Ejemplo básico en Python** pensado para el área de **Recursos Humanos (RRHH)**, explicado paso a paso, para que puedas entender cómo funciona y cómo adaptarlo a tus necesidades.  

En este caso, haremos un **pequeño programa que gestione empleados**, permitiendo:  
- **Registrar empleados**  
- **Listarlos**  
- **Calcular la edad promedio**  

***

## 📂 Ejemplo: Mini Sistema de Gestión de Empleados (RRHH)

```python
from datetime import datetime

# Lista para almacenar los empleados
empleados = []

# Función para registrar un empleado
def registrar_empleado(nombre, fecha_nacimiento, puesto):
    empleado = {
        "nombre": nombre,
        "fecha_nacimiento": fecha_nacimiento,
        "puesto": puesto
    }
    empleados.append(empleado)
    print(f"Empleado '{nombre}' registrado con éxito.")

# Función para mostrar todos los empleados
def mostrar_empleados():
    if not empleados:
        print("No hay empleados registrados.")
        return
    print("\n📋 Lista de Empleados:")
    for i, emp in enumerate(empleados, 1):
        print(f"{i}. {emp['nombre']} - {emp['puesto']} - Nacido en {emp['fecha_nacimiento']}")

# Función para calcular la edad promedio de los empleados
def edad_promedio():
    if not empleados:
        print("No hay empleados para calcular la edad.")
        return
    total_edades = 0
    for emp in empleados:
        fecha_nac = datetime.strptime(emp['fecha_nacimiento'], "%Y-%m-%d")
        edad = (datetime.now() - fecha_nac).days // 365
        total_edades += edad
    promedio = total_edades / len(empleados)
    print(f"📊 La edad promedio de los empleados es: {promedio:.1f} años.")

# Ejecución de ejemplo
registrar_empleado("Ana Pérez", "1995-05-20", "Analista de RRHH")
registrar_empleado("Luis Gómez", "1989-11-15", "Desarrollador")
registrar_empleado("María Torres", "1992-03-10", "Contadora")

mostrar_empleados()
edad_promedio()
```

***

## 📖 Explicación paso a paso:

1. **Importación de librerías**  
   - Usamos `datetime` para calcular la edad de los empleados a partir de su fecha de nacimiento.

2. **Base de datos sencilla**  
   - En este caso usamos una **lista en memoria** (`empleados`), pero fácilmente se podría conectar a Excel, CSV o una base de datos real.

3. **Funciones principales**:
   - `registrar_empleado()` → Guarda los datos en la lista.
   - `mostrar_empleados()` → Lista todos los empleados registrados.
   - `edad_promedio()` → Calcula la edad media de todos los empleados.

4. **Ejecución de prueba**  
   - Registramos tres empleados con datos ficticios.
   - Mostramos la lista y calculamos la edad promedio.

***

## 💡 Posibles mejoras:
- Guardar y leer empleados desde un archivo Excel o CSV.
- Agregar eliminación y actualización de datos.
- Integrar control de asistencia o cálculo de días trabajados.
- Crear interfaz gráfica con `tkinter` o aplicación web con `Flask` o `Django`.

***

**RETO**
Como analista de recursos humanos piense en nuevas funcionalidades que podría tener este esqueleto de herramienta y comparte su nombre y objeto en:

https://excalidraw.com/#json=4-fhjee-6Wi9fYbAmaEhn,6SSFWJymjks8TgraUWIb-A



