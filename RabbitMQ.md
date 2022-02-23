# RabbitMQ

An implementation of the AMQP message model (Advanced Message Queueing Protocol)

- decouple
- scalable
- performant

binding

## Benefits
### Flexibility 
largely comes from different types of exchanges available
- fanout
- direct (if routing key matches with the binding key)
- topic (partial mapping)
- header
- default (routing key tied to the queue name itself)

the way the message moves through the system is largely a part of the message metadata

It is the application and the developer has a lot of control with the way messages move through the system rather than the broker administrator

### Cloud friendly 
- can deploy an instance of it on Docker or other containerization software
- can run as a cluster: fault tolerant, highly available and have high throughput

### Cross language communication

### Security

### Acks
prevents the system from losing any messages

### Management

### Plug-in