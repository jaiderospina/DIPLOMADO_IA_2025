# Manual de instalación de LM Studio y ejemplos básicos de uso

LM Studio es una aplicación de escritorio diseñada para ejecutar modelos de lenguaje (LLM) localmente en Windows, macOS y Linux. Permite aprovechar el hardware propio para la inferencia y chat con IA, sin depender de servicios en la nube.

***

## Instalación de LM Studio

### Instalación en Windows

1. **Descargar el instalador**
   - El usuario debe acceder a la página oficial de LM Studio y descargar el instalador para Windows.

   [descarga](/images/download.jpg)

2. **Ejecutar el instalador**
   - Una vez descargado, se ejecuta el archivo instalador (`.exe`).



3. **Seguir el asistente**
   - El asistente de instalación guiará a través de los pasos necesarios. Solo hay que aceptar los términos y condiciones, elegir la ruta de instalación y finalizar.

[](/images/lmstudio.gif)

4. **Iniciar la aplicación**
   - Tras instalar, LM Studio estará disponible en el menú de inicio y podrá abrirse desde allí.

[](/images/1.jpg)

[](/images/2.jpg)

[](/images/3.jpg)


[](/images/4.jpg)


[](/images/5.jpg)

[](/images/6.jpg)

[](/images/7.jpg)


[](/images/8.jpg)


[](/images/9.jpg)

[](/images/10.jpg)
### Instalación en macOS

1. **Descargar el instalador**
   - Se debe descargar el archivo `.dmg` de la página oficial de LM Studio.
2. **Montar el disco**
   - Se hace doble clic sobre el `.dmg` descargado para montarlo.
3. **Mover LM Studio a Aplicaciones**
   - En la ventana que aparece, se arrastra el ícono de LM Studio a la carpeta de Aplicaciones.
4. **Abrir la aplicación**
   - Desde la carpeta Aplicaciones, se puede abrir LM Studio. La primera vez, es posible que macOS muestre un mensaje de seguridad; se debe aceptar.
5. **Conceder permisos**
   - Si el sistema lo solicita, se otorgan permisos para ejecutar la aplicación.

### Instalación en Linux (usando AppImage)

1. **Descargar la AppImage**
   - Se descarga el archivo `.AppImage` más reciente desde el sitio oficial.
2. **Hacer ejecutable la AppImage**
   - En la terminal, se ejecuta:
     ```bash
     chmod +x LM_Studio-*.AppImage
     ```
3. **Extraer el contenido (opcional)**
   - Para mayor control, se puede extraer el contenido:
     ```bash
     ./LM_Studio-*.AppImage --appimage-extract
     cd squashfs-root
     ```
4. **Ajustar permisos para Chrome Sandbox**
   - En la carpeta extraída, se ejecuta:
     ```bash
     sudo chown root:root chrome-sandbox
     sudo chmod 4755 chrome-sandbox
     ```
5. **Ejecutar LM Studio**
   - Se inicia el programa con:
     ```bash
     ./lm-studio
     ```

***

## Ejemplos básicos de uso

### Ejemplo 1: Usar LM Studio para chatear con un modelo

1. La persona abre LM Studio en su computadora.
2. Accede a la pestaña *"Discover"* para explorar modelos disponibles.
3. Busca y selecciona un modelo, como “Mistral-7B-Instruct” o “Meta-Llama-3.1-8B-Instruct”.
4. Hace clic en *"Download"* para descargar el modelo elegido.
5. Una vez descargado, lo selecciona y pulsa *"Launch"*.
6. En la ventana de chat, puede escribir una pregunta, por ejemplo:  
   > Hola, ¿puedes explicarme qué es el aprendizaje automático?
7. El modelo responde en tiempo real, localmente, sin necesidad de conexión a la nube.

### Ejemplo 2: Acceder a LM Studio desde el propio código (API local)

1. LM Studio se inicia en modo servidor local (esto suele ser por defecto).
2. Desde un entorno de desarrollo Python, es posible conectarse a la API local de LM Studio, por ejemplo:

```python
from openai import OpenAI
client = OpenAI(base_url="http://localhost:1234/v1", api_key="lm-studio")

response = client.chat.completions.create(
    model="lmstudio-community/qwen2.5-7b-instruct",
    messages=[{"role": "user", "content": "¿Cuál es la capital de Francia?"}]
)
print(response.choices[0].message.content)
```

Esto permite automatizar consultas a modelos de IA locales directamente desde código propio.

***

**Notas adicionales:**
- LM Studio recomienda modelos compatibles según el hardware detectado.
- Desde la aplicación es posible explorar y descargar modelos de distintas capacidades.
- Para tareas avanzadas, se recomienda consultar la documentación oficial y la integración en proyectos personalizados.