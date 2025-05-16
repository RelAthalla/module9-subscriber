## AMQP Overview

**AMQP** stands for **Advanced Message Queuing Protocol**.  
It is an open standard protocol for message-oriented middleware. AMQP enables systems to communicate by sending messages through queues, supporting **reliable, asynchronous communication** between distributed applications.

AMQP is commonly used with message brokers like **RabbitMQ**.

---

## Understanding `guest:guest@localhost:5672`

- **guest** (first) – Username for authentication  
- **guest** (second) – Password for authentication  
- **localhost** – Hostname (refers to the local machine)  
- **5672** – Port number used by AMQP brokers (like RabbitMQ) for client connections

This means:
> Connect to an AMQP broker running on your local machine (`localhost`) at port `5672`, using the username `guest` and password `guest`.

