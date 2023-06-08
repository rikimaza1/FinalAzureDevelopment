# Tema 5

## Implement API Management

*1.-* ¿Qué es Azure API Management y cuál es su propósito en el desarrollo de aplicaciones?

    Azure API Management es un servicio de Microsoft Azure que permite a los desarrolladores crear, publicar, administrar y proteger APIs (interfaces de programación de aplicaciones) de manera fácil y segura. Su propósito es simplificar la gestión de las APIs, permitiendo a los desarrolladores centrarse en la creación de aplicaciones y servicios, en lugar de preocuparse por la infraestructura y la seguridad de las APIs. Con Azure API Management, los desarrolladores pueden controlar el acceso a sus APIs, establecer límites de uso, monitorear el rendimiento y analizar el uso de las APIs, lo que les permite mejorar continuamente sus aplicaciones y servicios.

*2.-* ¿Cuáles son los beneficios de utilizar Azure API Management para gestionar APIs en una arquitectura de microservicios?

    Algunos de los beneficios de utilizar Azure API Management para gestionar APIs en una arquitectura de microservicios son:
    
    1. Centralización y control: Azure API Management permite centralizar y controlar el acceso a las APIs de los microservicios, lo que facilita la gestión y el monitoreo de las mismas.
    
    2. Escalabilidad: Azure API Management es altamente escalable, lo que permite manejar grandes volúmenes de tráfico y adaptarse a las necesidades de crecimiento de la empresa. 
    
    3. Seguridad: Azure API Management ofrece una capa de seguridad adicional para las APIs, lo que ayuda a proteger los microservicios de posibles ataques externos. 
    
    4. Monetización: Azure API Management permite monetizar las APIs, lo que puede generar ingresos adicionales para la empresa. 
    
    5. Analítica: Azure API Management ofrece herramientas de analítica avanzada que permiten obtener información valiosa sobre el uso de las APIs, lo que puede ayudar a mejorar su rendimiento y eficiencia.

*3.-* ¿Cómo se configura y se utiliza Azure API Management para controlar el acceso y la seguridad de las APIs?

    Para configurar y utilizar Azure API Management para controlar el acceso y la seguridad de las APIs, se pueden seguir los siguientes pasos: 
    
    1. Crear una instancia de Azure API Management en el portal de Azure. 
    
    2. Crear una API en la instancia de API Management. 
    
    3. Configurar las políticas de seguridad y acceso para la API, como autenticación, autorización y límites de uso. 
    
    4. Crear usuarios y grupos de usuarios en la instancia de API Management. 
    
    5. Asignar permisos de acceso a los usuarios y grupos para la API. 
    
    6. Configurar los endpoints de la API para que se comuniquen con los sistemas de backend. 
    
    7. Publicar la API para que los desarrolladores puedan acceder a ella a través de la instancia de API Management. Una vez configurada la instancia de API Management y la API, se pueden utilizar las herramientas de monitoreo y análisis para supervisar el uso de la API y detectar posibles problemas de seguridad o rendimiento. 
    Además, se pueden implementar políticas adicionales para proteger la API contra ataques y garantizar su disponibilidad y rendimiento.

*1.-* You need to authenticate the user to the corporate website as indicated by the architectural diagram. 

Which two values should you use? 

Each correct answer presents part of the solution.

NOTE: Each correct selection is worth one point.
    
    A. ID token signature
    B. ID token claims
    C. HTTP response code
    D. Azure AD endpoint URI
    E. Azure AD tenant ID
    Correct Answer: AD 

    Explanation:

    A: Claims in access tokens
    JWTs (JSON Web Tokens) are split into three pieces:
    Header - Provides information about how to validate the token including information about the type of token and how it was signed.
    Payload - Contains all of the important data about the user or app that is attempting to call your service. Signature - Is the raw material used to validate the token.
    E: Your client can get an access token from either the v1.0 endpoint or the v2.0 endpoint using a variety of protocols.
    Scenario: User authentication (see step 5 below)
    The following steps detail the user authentication process:
    1. The user selects Sign in in the website.
    2. The browser redirects the user to the Azure Active Directory (Azure AD) sign in page.
    3. The user signs in.
    4. Azure AD redirects the user’s session back to the web application. The URL includes an access token. 5. The web application calls an API and includes the access token in the authentication header. The
    application ID is sent as the audience (‘aud’) claim in the access token. 6. The back-end API validates the access token.

*2.-* Your company is developing an Azure API.
You need to implement authentication for the Azure API. You have the following requirements:
All API calls must be secure.
Callers to the API must not send credentials to the API.

Which authentication mechanism should you use?
    
    A. Basic
    B. Anonymous
    C. Managed identity 
    D. Client certificate
    Correct Answer: C 

    Explanation:
    Use the authentication-managed-identity policy to authenticate with a backend service using the managed identity of the API Management service. This policy essentially uses the managed identity to obtain an access token from Azure Active Directory for accessing the specified resource. After successfully obtaining the token, the policy will set the value of the token in the Authorization header using the Bearer scheme.

*3.-* You are a developer for a SaaS company that offers many web services. All web services for the company must meet the following requirements:
Use API Management to access the services A6319EC1AC83D57E5BA185C098116365
Use OpenID Connect for authentication Prevent anonymous usage
A recent security audit found that several web services can be called without any authentication. Which API Management policy should you implement?
    
    A. jsonp
    B. authentication-certificate C. check-header
    D. validate-jwt
    Correct Answer: D 

    Explanation:
    
    Add the validate-jwt policy to validate the OAuth token for every incoming request.
    Incorrect Answers:
    A: The jsonp policy adds JSON with padding (JSONP) support to an operation or an API to allow cross- domain calls from JavaScript browser-based clients. JSONP is a method used in JavaScript programs to request data from a server in a different domain. JSONP bypasses the limitation enforced by most web browsers where access to web pages must be in the same domain.
    JSONP - Adds JSON with padding (JSONP) support to an operation or an API to allow cross-domain calls from JavaScript browser-based clients.