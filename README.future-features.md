
# eventflowsys – Unplanned & Possible Future Features

This document lists **possible, uncommitted ideas** for the future of eventflowsys. These are not planned or promised features—just a collection of creative directions the project could take. Community feedback and real-world needs will shape what (if any) get built.

## Unplanned Ideas & Possibilities

- **Event Persistence & Replay**: Persist messages to disk or database and replay them for new subscribers or debugging.
- **Dead Letter Queue**: Automatically move undeliverable messages to a dead letter queue for inspection or reprocessing.
- **Message Filtering & Transformation**: Allow subscribers to filter or transform messages before handling.
- **Wildcard & Pattern Subscriptions**: Subscribe to multiple groups/topics using wildcards or regex patterns.
- **Message Acknowledgement & Retry**: Require explicit ack from handlers, with configurable retry logic.
- **Event Tracing & Correlation**: Add correlation IDs and tracing hooks for distributed debugging.
- **Plugin System**: Dynamically load/unload event handler plugins at runtime.
- **Event Schema Validation**: Register and enforce schemas for message types.
- **Batching & Scheduling**: Support for message batching and scheduled (delayed) delivery.
- **Multi-tenancy & Isolation**: Isolate groups of subscribers for multi-tenant scenarios.
- **Cloud Broker Integration**: Optional adapters for RabbitMQ, Kafka, Azure Service Bus, etc.
- **Security & Rate Limiting**: Message encryption, signing, and per-group/subscriber rate limiting.
- **Custom Priority Strategies**: Allow pluggable strategies for message prioritization.
- **Lifecycle Event Hooks**: Hooks for bus startup, shutdown, and other lifecycle events.
- **Cloud Broker Adapters**: Integrate with RabbitMQ, Kafka, Azure Service Bus, and more.
- **Automated Testing Utilities**: Tools for simulating, testing, and validating event flows.
- **Jupyter/Notebook Integration**: Interactive event bus usage and visualization in notebooks.
- **Advanced Monitoring/Observability**: More built-in metrics, tracing, and logging for all bus operations (no dashboard/CLI planned).
- **Distributed Event Bus**: Multi-process or multi-host event bus for distributed systems.
- **WebSocket/REST API Integration**: Allow event bus to send/receive over network protocols.
- **Graph-based Routing**: Support for complex event routing and transformation graphs.
- **Event Sourcing Patterns**: Support for event sourcing and CQRS architectures.
- **AI/ML Event Handlers**: Integrate with AI/ML models for smart event processing.
- **Mobile/IoT Adapters**: Support for lightweight event bus usage on mobile or IoT devices.
- **Visual Debugging Tools**: Export event flow for visualization in external tools.
- **Zero-Config Mode**: Auto-discover and wire up services with minimal setup.

---

*This is a living list of ideas, not a roadmap. Suggestions welcome!*
