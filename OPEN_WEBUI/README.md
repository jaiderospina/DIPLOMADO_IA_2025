## Guía Rápida de Open WebUI 🚀

**Open WebUI** es una plataforma de interfaz de usuario de IA autoalojada, extensible y fácil de usar, que puede funcionar completamente sin conexión. Permite interactuar con diferentes modelos de lenguaje (LLMs) y facilita la integración de diversas APIs compatibles como Ollama y OpenAI.

### Funcionalidades Principales

- **Instalación sencilla:** Compatible con Docker, Kubernetes y pip (Python).
- **Compatibilidad amplia:** Soporta Ollama, APIs tipo OpenAI, integración fácil con LMStudio, GroqCloud, Mistral, OpenRouter y más.
- **Control de usuarios y permisos:** Roles y permisos granulados, con seguridad reforzada y experiencias personalizadas.
- **App web responsive y PWA:** Experiencia fluida en escritorio y móvil, incluso como aplicación web progresiva con acceso offline.
- **Soporte Markdown y LaTeX:** Ideal para respuestas ricas en formato y matemáticas.
- **Llamadas de voz/video integradas**, generación de imágenes, integración nativa de Python y editor de código.
- **RAG local:** Soporta Retrieval Augmented Generation, permitiendo cargar archivos y hacer consultas avanzadas.
- **Búsqueda web:** Integra motores como SearXNG, Google, Brave, DuckDuckGo, Bing, entre otros.
- **Multilenguaje e internacionalización:** Interfaz disponible en varios idiomas.
- **Actualización continua y soporte comunitario.**

### Instalación Rápida

#### Opción 1: Python pip

1. Asegúrate de usar **Python 3.11**.
2. Instala con pip:

   ```bash
   pip install open-webui
   ```
3. Ejecuta el servidor:

   ```bash
   open-webui serve
   ```
4. Accede a la interfaz en [http://localhost:8080](http://localhost:8080).

#### Opción 2: Docker (Recomendado)

- Si tienes Ollama en tu equipo:
   ```bash
   docker run -d -p 3000:8080 --add-host=host.docker.internal:host-gateway -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
   ```

- Para usar Open WebUI + Ollama todo en uno (con GPU):
   ```bash
   docker run -d -p 3000:8080 --gpus=all -v ollama:/root/.ollama -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:ollama
   ```

- Para conexión remota con Ollama, agrega la variable de entorno:
   ```bash
   docker run -d -p 3000:8080 -e OLLAMA_BASE_URL=https://direccion-servidor -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
   ```

- Solo para OpenAI API:
   ```bash
   docker run -d -p 3000:8080 -e OPENAI_API_KEY=tu_clave_api -v open-webui:/app/backend/data --name open-webui --restart always ghcr.io/open-webui/open-webui:main
   ```

**Acceso:** Después de la instalación, ve a [http://localhost:3000](http://localhost:3000).

### Recomendaciones y Consejos

- **Montaje de volumen (-v):** Imprescindible para evitar pérdida de base de datos.
- **GPU:** Usa imágenes `:cuda` si deseas aceleración por GPU en Linux/WSL (instala CUDA toolkit).
- **Actualización:** Utiliza Watchtower para mantener tu contenedor Docker al día.
- **Modo offline:** Define `HF_HUB_OFFLINE=1` si trabajas sin Internet.

### Recursos y Soporte

- **Documentación**: Revisa la documentación de Open WebUI para temas avanzados de configuración, integración y desarrollo.
- **Comunidad y ayuda:** Únete a su Discord para soporte directo o abre un issue en GitHub.
- **Licencia:** BSD-3-Clause modificada (se debe mantener el branding de "Open WebUI").

### Resumen Visual

| Instalación      | Comando principal                                                                                |
|------------------|-------------------------------------------------------------------------------------------------|
| Python/pip       | `pip install open-webui` / `open-webui serve`                                                   |
| Docker + Ollama  | `docker run ... ghcr.io/open-webui/open-webui:ollama`                                           |
| Solo OpenAI API  | `docker run ... -e OPENAI_API_KEY=... ghcr.io/open-webui/open-webui:main`                       |
| Acceso           | http://localhost:3000 o http://localhost:8080 según instalación                                 |

**Open WebUI** es ideal para quienes buscan una solución robusta, autoalojada y con control total sobre su infraestructura de IA, listas para despliegue corporativo o entornos experimentales avanzados.

- https://github.com/open-webui/open-webui
- https://4geeks.com/es/interactive-coding-tutorial/instalando-ollama-y-openwebui