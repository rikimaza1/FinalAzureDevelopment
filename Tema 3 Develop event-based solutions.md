# Tema 3

## Develop event-based solutions

*1.-* ¿Qué son las soluciones basadas en eventos y cómo se diferencian de las arquitecturas tradicionales basadas en solicitudes y respuestas? 

    Las soluciones basadas en eventos son un enfoque de arquitectura de software en el que los componentes del sistema se comunican a través de eventos, en lugar de solicitudes y respuestas. En este enfoque, los componentes del sistema envían y reciben eventos, que son notificaciones de que algo ha sucedido en el sistema. Los eventos pueden ser generados por cualquier componente del sistema y pueden ser consumidos por cualquier otro componente que esté interesado en ellos. 
    Las arquitecturas tradicionales basadas en solicitudes y respuestas implican que un componente del sistema envía una solicitud a otro componente y espera una respuesta. Este enfoque puede ser menos escalable y menos flexible que las soluciones basadas en eventos, ya que los componentes del sistema están más acoplados y dependen más unos de otros. 

*2.-* ¿Cuál es el papel de Azure Event Grid en la implementación de soluciones basadas en eventos y cómo se integra con otros servicios de Azure?

    Permite la creación de soluciones basadas en eventos de manera sencilla y escalable. Su papel principal es actuar como un enrutador de eventos, permitiendo la comunicación entre diferentes servicios y aplicaciones en tiempo real. Event Grid se integra con una amplia variedad de servicios de Azure, como Azure Functions, Azure Logic Apps, Azure Event Hubs, Azure Storage, Azure Service Bus, entre otros. Esto permite que los eventos generados por estos servicios sean enviados a Event Grid y distribuidos a los suscriptores correspondientes. Además, Event Grid también se integra con servicios externos a Azure, como GitHub, Azure DevOps, y otros servicios de terceros, lo que permite la creación de soluciones híbridas y la integración con sistemas existentes.

*3.-* ¿Cuáles son los beneficios y casos de uso comunes de Azure Event Hub en el procesamiento y análisis de flujos masivos de eventos en tiempo real?

    Azure Event Hub es una plataforma de procesamiento de eventos en tiempo real que permite la ingestión y procesamiento de grandes volúmenes de datos de eventos en tiempo real. Algunos de los beneficios y casos de uso comunes de Azure Event Hub son: 
    
    1. Escalabilidad: Azure Event Hub puede manejar grandes volúmenes de eventos en tiempo real y escalar automáticamente para manejar picos de tráfico. 
    
    2. Integración: Azure Event Hub se integra con una amplia variedad de herramientas y servicios de Azure, como Azure Stream Analytics, Azure Functions, Azure Logic Apps, y más. 
    
    3. Análisis en tiempo real: Azure Event Hub permite el análisis en tiempo real de los datos de eventos, lo que permite a los usuarios tomar decisiones en tiempo real basadas en los datos.
    
    4. IoT: Azure Event Hub es una plataforma popular para la ingestión y procesamiento de datos de IoT, lo que permite a los usuarios monitorear y analizar los datos de sensores en tiempo real. 
    
    5. Registro de eventos: Azure Event Hub permite el registro de eventos para fines de auditoría y cumplimiento.

*1.-* You need to store the user agreements.
Where should you store the agreement after it is completed?
    
    A. Azure Storage queue
    B. Azure Event Hub
    C. Azure Service Bus topic
    D. Azure Event Grid topic

    Correct Answer: B 

    Explanation:

    Azure Event Hub is used for telemetry and distributed data streaming.This service provides a single solution that enables rapid data retrieval for real-time processing as well as repeated replay of stored raw data. It can capture the streaming data into a file for processing and analysis. It has the following characteristics: low latency capable of receiving and processing millions of events per second at least once delivery.

*2.-* You are developing a solution that will use Azure messaging services. You need to ensure that the solution uses a publish-subscribe model and eliminates the need for constant polling. What are two possible ways to achieve the goal? 

Each correct answer presents a complete solution. 

NOTE: Each correct selection is worth one point.
   
    A. Service Bus
    B. Event Hub
    C. Event Grid
    D. Queue
    Correct Answer: AC Section: (none) Explanation
    Explanation/Reference:
    Explanation:
    It is strongly recommended to use available messaging products and services that support a publish- subscribe model, rather than building your own. In Azure, consider using Service Bus or Event Grid. Other technologies that can be used for pub/sub messaging include Redis, RabbitMQ, and Apache Kafka.

*3.-* You are developing an e-commerce solution that uses a microservice architecture. You need to design a communication backplane for communicating transactional messages between various parts of the solution. Messages must be communicated in first-in-first-out (FIFO) order.

What should you use?
    
    A. Azure Storage Queue
    B. Azure Event Hub
    C. Azure Service Bus D. Azure Event Grid
    Correct Answer: A Section: (none) Explanation
    Explanation/Reference:
    Explanation:
    As a solution architect/developer, you should consider using Service Bus queues when:
    Your solution requires the queue to provide a guaranteed first-in-first-out (FIFO) ordered delivery.
