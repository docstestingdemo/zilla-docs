

  # What is Zilla?

Zilla is a multi-protocol edge and service proxy designed to streamline, secure, and manage event-driven architectures. It offers several key features and benefits:

## Key Features

1. **Multi-Protocol Support**: Zilla supports various network and application protocols, including HTTP, Kafka, SSE, MQTT, gRPC, and WebSocket.

2. **Stateless and Cloud-Native**: Zilla is stateless, highly memory efficient, and scales horizontally to support millions of concurrently connected clients.

3. **Protocol Mapping**: Zilla treats every protocol as a stream, simplifying the mapping between different protocols.

4. **Schema Support**: Zilla supports Protobuf, Avro, and JSON Schema payloads for message validation and translation.

5. **API Specification Support**: Zilla supports OpenAPI and AsyncAPI specifications for message validation and API creation.

6. **Security**: Zilla can terminate TLS and supports JWT-based authorization for REST, SSE, and MQTT endpoints/services.

7. **Observability**: Zilla provides metrics exposure via Prometheus, logs events to stdout, and supports OpenTelemetry for both metrics and logging.

## Use Cases

Zilla can be used as:

1. **Service Proxy (Sidecar)**: Deployed in front of existing services to add metrics, logging, message validation, and authentication.

2. **AsyncAPI Kafka Gateway**: Abstracts Apache Kafka for web applications, IoT clients, and non-Kafka microservices.

## Benefits

- Streamlines event-driven architectures
- Replaces custom code, Kafka Connect, MQTT brokers, and other integration middleware
- Saves time and reduces DevOps burden
- Removes complexity from architectures

## Target Users

- Data platform/Kafka integration engineers
- Application developers without Kafka expertise
- API architects driving business functionality via AsyncAPI schemas

Zilla is available under the Aklivity Community License, with a commercial version (Zilla Plus) offering additional enterprise integrations and support.

  