  # Tema 4: Implement containerized solutions
  
  ## ¿Cuál es la diferencia entre Azure Container Registry, Azure Container Instances y Azure Container Apps?	

    La diferencias que existen son: Azure Container Registry es un servicio de registro de contenedores, Azure Container Instances es un servicio de ejecución de contenedores y Azure Container Apps es un servicio sin servidor para implementar aplicaciones basadas en eventos en contenedores.

  ## ¿Cómo se utiliza Azure Container Registry para almacenar y gestionar imágenes de contenedores?

    Para utilizar Azure Container Registry (ACR) para almacenar y gestionar imágenes de contenedores, puedes seguir estos pasos:

    - Crear un Azure Container Registry: En el portal de Azure, crea un nuevo Azure Container Registry en la suscripción y grupo de recursos adecuados. Proporciona un nombre único para el registro y selecciona la ubicación geográfica.

    - Autenticación y autorización: Configura las opciones de autenticación y autorización para el registro. Puedes elegir entre diferentes métodos de autenticación, como el uso de una clave de acceso o la integración con Azure Active Directory.

    - Construir y etiquetar imágenes: Utiliza una herramienta de construcción de imágenes de contenedores, como Docker, para crear tus imágenes de contenedores. Asegúrate de etiquetar las imágenes con el nombre completo del registro de ACR y la etiqueta correspondiente.

    - Iniciar sesión en el registro: Utiliza el comando docker login para iniciar sesión en tu registro de ACR desde tu máquina local o desde la máquina de desarrollo donde se encuentra la imagen de contenedor.

    - Subir las imágenes al registro: Utiliza el comando docker push para subir las imágenes etiquetadas al registro de ACR. Esto transferirá las imágenes desde tu máquina local al registro en Azure.

    - Administrar imágenes y etiquetas: En el portal de Azure o a través de la CLI de Azure, puedes administrar las imágenes y etiquetas en tu registro de ACR. Puedes ver, eliminar o agregar etiquetas a las imágenes existentes, y también configurar políticas de retención y escaneo de vulnerabilidades.

    - Implementar imágenes de contenedor: Utiliza las imágenes almacenadas en tu registro de ACR para implementar contenedores en otros servicios, como Azure Container Instances o Azure Kubernetes Service (AKS). Puedes hacer referencia a las imágenes por su nombre y etiqueta en los archivos de configuración o durante la creación de recursos.

    Siguiendo estos pasos, podrás utilizar Azure Container Registry para almacenar y gestionar tus imágenes de contenedores de manera segura y eficiente.

  ## ¿Cuál es el propósito y la ventaja de utilizar Azure Container Instances para ejecutar contenedores sin necesidad de administrar una infraestructura subyacente?	

    Azure Container Instances (ACI) te permite ejecutar contenedores sin preocuparte por la infraestructura subyacente. No necesitas administrar servidores virtuales o clústeres de contenedores. Puedes iniciar rápidamente tus contenedores, escalarlos según sea necesario y pagar solo por el tiempo de ejecución y los recursos utilizados. ACI es fácil de integrar con otros servicios de Azure. En resumen, ACI simplifica la ejecución de contenedores sin complicaciones de administración y con mayor flexibilidad y eficiencia.