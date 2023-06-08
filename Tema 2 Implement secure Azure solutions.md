# Tema 2: Implement secure Azure solutions

### ¿Qué es Azure Key Vault y cómo se utiliza para proteger secretos y claves criptográficas?

- Azure Key Vault es un servicio en la nube para el almacenamiento de los secretos y el acceso a estos de forma segura. Un secreto es todo aquello cuyo acceso desea controlar de forma estricta, como las claves API, las contraseñas, los certificados o las claves criptográficas.

- El servicio Azure Key Vault cifra sus secretos cuando los agrega y los descifra automáticamente cuando los lee. La clave de hoja de cifrado de la jerarquía de claves es única para cada almacén de claves. La clave raíz del cifrado de la jerarquía de claves es única en el mundo de la seguridad y su nivel de protección varía entre regiones.

- Azure Key Vault permite a las aplicaciones y los usuarios de Microsoft Azure almacenar y usar varios tipos de datos de secretos y claves: claves, secretos y certificados. Las claves, los secretos y los certificados se conocen colectivamente como "objetos".

### ¿Cuál es el papel de las Identidades Administradas (Managed Identities) en la seguridad de Azure?

-Las identidades administradas (Managed Identities) son una característica de Azure Active Directory que proporciona una identidad segura para los servicios que se ejecutan en Azure. Con Managed Identities, no es necesario almacenar credenciales en el código o en archivos de configuración.

- Las identidades administradas eliminan la necesidad de administrar credenciales en el código. En lugar de ello, se asigna una identidad a un recurso de Azure durante el aprovisionamiento. La identidad se puede usar para autenticar con cualquier servicio que admita Azure Active Directory.

### ¿Cómo se configuran y se utilizan Azure Key Vault y las Identidades Administradas?

1. _Azure Key Vault_:

   1. _Configuración_

      - Se puede crear desde el MarketPlace de Azure Portal buscando Key Vault y configurando los parametros de la plantillas.
      - Por Azure CLI:

      ```
      az keyvault create \
          --resource-group <resource-group> \
          --name <your-unique-vault-name>
      ```

      - PorwerShell

      ```
      New-AzKeyVault -Name <your-unique-vault-name> -ResourceGroupName <resource-group>
      ```

   2. _Utilización_

   - Se utiliza para almacenar y recuperar secretos y claves de forma segura. se puede utilizar Azure Key Vault en los siguientos casos:

     - Desde tus aplicaciones o servicios en Azure, puedes autenticarte y acceder al Key Vault para obtener secretos o claves en tiempo de ejecución.

     - Puedes integrar Azure Key Vault con otros servicios de Azure, como Azure Functions o Azure App Service, para acceder a los secretos y claves almacenados en el Key Vault durante la ejecución de tus aplicaciones. 3.

2. _Identidades Administradas_:

- _Configuración_: Las Identidades Administradas son entidades de seguridad que puedes crear en Azure para asignarles permisos y utilizarlas para autenticarte en otros servicios. Para configurar una Identidad Administrada, sigue estos pasos:

      - Navega hasta el recurso (por ejemplo, una función de Azure) donde deseas habilitar una Identidad Administrada.
      - Busca la sección de "Identidad" en la configuración del recurso y habilita una Identidad Administrada.
      - Guarda los cambios y asegúrate de que se haya creado la Identidad Administrada.

- _Utilización_:
- Una vez habilitada una Identidad Administrada, se puede utilizar para authentificacion y acceder a otros servicios, como Azure Key Vault. se puede utilizar Identidades Administradas en los siguientes casos :

  - Configurar el acceso y los permisos en el Key Vault para permitir que la Identidad Administrada acceda a los secretos o claves necesarios.
  - Desde tu aplicación o servicio en Azure, puedes obtener un token de autenticación usando la Identidad Administrada y utilizarlo para acceder a otros servicios protegidos, como Key Vault, sin necesidad de administrar explícitamente las credenciales.
