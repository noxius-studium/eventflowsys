
# eventflowsys

**eventflowsys** is a modern, extensible Python package for building robust event-driven systems. It provides both threaded and async event bus implementations, advanced subscription and messaging features, and a flexible logger injection base class. Designed for professional use, it follows SOLID principles and is suitable for a wide range of applications—from microservices to desktop apps.

---

## Key Features

- **Threaded & Async Event Buses**: Choose between thread-safe (synchronous) and asyncio-based (asynchronous) event bus implementations.
- **Group-based Subscriptions**: Organize services into named groups and deliver messages to targeted audiences.
- **Priority & TTL Messaging**: Control message delivery order and expiration with priority and time-to-live support.
- **Broadcast Support**: Instantly send messages to all groups.
- **Event Hooks**: Register custom hooks for subscribe, unsubscribe, message delivery, and error events.
- **Metrics & Tracking**: Monitor delivered, failed, pending, and expired messages. Query which services have not yet read a message.
- **Custom Error Handling**: Built-in error classes for robust, granular error management.
- **Logger Injection**: Abstract base class for dependency-injected loggers using loguru, supporting custom or default logging.
- **SOLID Principles**: Clean, extensible, and maintainable architecture.

---

## Installation

```bash
pip install eventflowsys
```

---

## Quick Start

### Threaded Event Bus Example
```python
from eventflowsys import ThreadedServiceBus

bus = ThreadedServiceBus()
def callback(msg_id, data):
    print(f"Received: {data}")
bus.subscribe("group1", "serviceA", callback)
bus.publish("group1", "hello world")
```

### Async Event Bus Example
```python
from eventflowsys import AsyncServiceBus
import asyncio

async def main():
    bus = AsyncServiceBus()
    async def callback(msg_id, data):
        print(f"Received: {data}")
    await bus.subscribe("group1", "serviceA", callback)
    await bus.publish("group1", "hello async world")
asyncio.run(main())
```

### LoggerInjectable Example
```python
from eventflowsys import LoggerInjectable

class MyService(LoggerInjectable):
    def perform_action(self):
        self.logger.info("Action performed!")

service = MyService()
service.perform_action()
```

---

## File Structure

- `logger_Injectable.py`: Base class for logger injection
- `bus/base_bus.py`: Abstract event bus interface and message definition
- `bus/async_bus.py`: Asyncio-based event bus implementation
- `bus/thread_bus.py`: Threaded event bus implementation

---

## Documentation

See `README.documentation.md` for advanced usage, architecture diagrams, and a full API reference.

---

## Contributing

Contributions, suggestions, and issues are welcome! Please see the documentation for guidelines.

---

## License

MIT License
