# Manual Básico: Cómo Instalar tu Propio Entorno Local Tipo ChatGPT

Este manual guiará a través de los pasos para configurar un entorno de inteligencia artificial similar a ChatGPT directamente en tu máquina, utilizando modelos de lenguaje abiertos como Llama 3, sin necesidad de APIs externas o conexión a internet constante. 

Para más detalla ir al vídeo de refrencia haciendo clic sobre el minuto de interés.

## 1\. ¿Qué Aprenderás a Configurar?

  * **Entorno Local de ChatGPT**: Instalarás un sistema que te permitirá generar respuestas de modelos de IA directamente desde tu computadora.
  * **Combinación de Modelos**: Aprenderás a integrar modelos abiertos (como Llama 3) con modelos cerrados de OpenAI (GPT-3.5, GPT-4) si lo deseas, usando una clave API de OpenAI.
  * **Interfaz Gráfica**: Configurarás una interfaz de usuario intuitiva similar a ChatGPT.

## 2\. Programas Necesarios

Para llevar a cabo esta configuración, necesitarás los siguientes programas:

  * **Ollama**: \[[02:02](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=122)\]
      * **Función**: Simplifica la descarga y gestión de diversos modelos de IA abiertos en tu máquina.
      * **Dónde encontrar modelos**: Puedes explorar modelos disponibles en [ollama.com/models](https://ollama.com/models) \[[02:28](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=148)\].
  * **Open Web UI**: \[[02:43](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=163)\]
      * **Función**: Proporciona una interfaz gráfica similar a ChatGPT, con características como importación/exportación de archivos, cambio entre modelos y creación de múltiples cuentas.
  * **Docker**: \[[03:06](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=186)\]
      * **Función**: Es un requisito previo para instalar Open Web UI, ya que se utiliza para ejecutar la interfaz gráfica.
      * **Instalación de Docker**: El video menciona un tutorial separado para instalar Docker en Windows, Linux y Mac \[[03:16](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=196)\].

## 3\. Pasos de Instalación

Sigue estos pasos para configurar tu entorno:

### 3.1 Instalar Ollama \[[03:28](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=208)\]

1.  Descarga el instalador de Ollama desde [ollama.com/download](https://ollama.com/download) para tu sistema operativo.
2.  Ejecuta el instalador y sigue las instrucciones.

### 3.2 Descargar un Modelo de IA \[[04:04](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=244)\]

1.  Abre tu terminal (Símbolo del sistema o PowerShell en Windows).
2.  Usa el comando de Ollama para descargar un modelo. Por ejemplo, para descargar Llama 3:
    ```bash
    ollama pull llama3
    ```

### 3.3 Instalar Open Web UI \[[05:07](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=307)\]

1.  **Asegúrate de tener Docker instalado y funcionando.**
2.  Utiliza el comando Docker específico proporcionado en la documentación de Open Web UI para lanzar la aplicación web. Este comando generalmente se encuentra en la página de GitHub o documentación de Open Web UI.

## 4\. Uso de la Interfaz (Open Web UI)

Una vez instalado, puedes acceder y usar tu entorno de IA local:

### 4.1 Acceder a la Interfaz \[[06:04](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=364)\]

1.  Abre tu navegador web.
2.  Navega a la dirección: `localhost:3000`

### 4.2 Primeros Pasos \[[06:09](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=369)\]

1.  **Crear una cuenta**: La primera vez que accedas, deberás crear una cuenta (esta cuenta es local para tu máquina).
2.  **Seleccionar un modelo**: \[[06:32](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=392)\] Una vez dentro, selecciona el modelo deseado (por ejemplo, Llama 3) de la interfaz para comenzar a hacer preguntas.

### 4.3 Funcionalidades Básicas \[[07:08](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=428)\]

  * **Continuar respuestas**: Si el modelo se detiene, puedes pedirle que continúe.
  * **Información de la respuesta**: Visualiza detalles como tokens utilizados y tiempo de carga.
  * **Editar preguntas**: Modifica tus preguntas para obtener mejores respuestas.
  * **Subir archivos**: Sube archivos para que el modelo los lea y los utilice como contexto.

## 5\. Características Avanzadas

El video también destaca funcionalidades más avanzadas para personalizar tu experiencia:

  * **Archivos de Modelo (Model Files)**: \[[07:42](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=462)\] Crea archivos personalizados para adaptar el comportamiento de los modelos.
  * **Prompts Guardados**: \[[07:52](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=472)\] Guarda prompts o instrucciones de uso frecuente para reutilizarlos fácilmente.
  * **Documentos**: \[[08:02](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=482)\] Sube documentos para que el modelo los consulte y utilice en sus respuestas.
  * **Configuración (Settings)**: \[[08:20](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=500)\]
      * Personaliza temas y el idioma de la interfaz.
      * Añade un prompt genérico que se aplique a todos tus chats.
      * Gestiona las conexiones y configuraciones del sistema.
  * **Integración con API de OpenAI**: \[[09:01](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=541)\] Conecta tu clave API de OpenAI para usar modelos GPT junto con tus modelos locales.
  * **Múltiples Modelos Simultáneamente**: \[[10:48](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=648)\] Haz una pregunta y recibe respuestas de diferentes modelos al mismo tiempo.

## 6\. Añadir Más Modelos \[[11:56](http://www.youtube.com/watch?v=BnL-XrzxSZE&t=716)\]

Puedes descargar modelos adicionales en cualquier momento usando el comando `ollama pull [nombre_del_modelo]` en tu terminal. Una vez descargados, aparecerán automáticamente en la interfaz de Open Web UI.

-----

Este manual te proporciona una guía completa para empezar a utilizar tu propio entorno de IA local. ¡Disfruta explorando las capacidades de los modelos de lenguaje abiertos\!

