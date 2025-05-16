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

## RabbitMQ

### Simulation slow subscriber
![](images/1.png)

## Impact of Slowing Down the Subscriber

In the image above, the **Subscriber** was intentionally slowed down by introducing a **1-second delay** in processing each message.

### Key Observations:

- This delay reduced the Subscriber's ability to keep up with incoming messages.
- Since the **Publisher** continued sending messages at a faster rate, the **message broker** began **queuing** the incoming data.
- As a result, the number of **queued messages** in the broker increased over time.

In this specific case, after running the Publisher **twice**, the total number of queued messages in the message broker reached **6**.

This demonstrates how **imbalanced message rates** between Publisher and Subscriber can lead to **message buildup** in the broker.

