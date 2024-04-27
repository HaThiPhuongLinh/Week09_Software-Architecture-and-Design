# SA Event-Driven Order Management System

## Overview

> The SA Event-Driven Order Management System is a system built on an event-driven architecture using Apache ActiveMQ as the messaging broker.
It allows clients to submit order information, which is then processed by three services: Inventory, Delivery, and Payment.
These services subscribe to a shared topic, "inventory.topic_01", to receive order information and then parses the JSON message using Gson into Java objects and performs further processing based on the information it requires.

![image](https://github.com/HaThiPhuongLinh/Week09_Software-Architecture-and-Design/assets/109422010/7edbcc82-7076-40b5-b65d-c1b0ea66de53)

## Features

- **Event-Driven Architecture**: The system follows an event-driven architecture where order information is published to a topic, and services react to these events asynchronously.

![image](https://github.com/HaThiPhuongLinh/Week09_Software-Architecture-and-Design/assets/109422010/ec022cb8-57c2-4e80-b07e-3ebd23da7350)

- **Apache ActiveMQ**: Utilizes Apache ActiveMQ as the messaging broker for reliable and scalable message delivery.
- **Decoupled Services**: Inventory, Delivery, and Payment services are decoupled and independently process order information based on their specific responsibilities.
- **JSON Parsing**: Gson library is used to parse JSON messages received from the client into Java objects for further processing.


