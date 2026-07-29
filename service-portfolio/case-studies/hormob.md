# HorMob — Offline-first AI-enabled Mobile Platform

## Status

**MVP / active architecture development**

## Executive summary

HorMob is an offline-first mobile platform direction for secure field work. It combines locally available maps and structured layers with controlled synchronization, communications and future AI-assisted workflows.

## Why it was needed

Field applications cannot assume permanent connectivity. Users may still need maps, operational layers, reference packages and communication capabilities when the network is weak, unavailable or restricted. The architecture must also control how data is packaged, stored, updated and synchronized.

## Solution direction

```text
Desktop or server package preparation
        ↓
Versioned offline package
        ↓
Secure delivery to the mobile device
        ↓
Local maps, layers and operational data
        ↓
Offline use
        ↓
Controlled synchronization when connected
        ↓
Messaging, RTC and AI-enabled services
```

## Planned platform capabilities

- offline base map and structured JSON layers;
- controlled package updates over a trusted connection;
- private and group messaging;
- audio and video calls and rooms;
- field object and UAV display on the map;
- click-to-open live stream workflow;
- server-side services integrated with existing secure infrastructure;
- future AI assistance for knowledge, workflow and situational data.

## Alexander Gubenko's contribution

- defined the offline-first product direction and operating constraints;
- designed the relationship between mobile packages, synchronization and server services;
- connected mapping, secure communications, RTC and AI into one platform architecture;
- planned reuse of existing Matrix, LiveKit and server infrastructure;
- organized the implementation as an MVP with staged expansion;
- established the repository and development workflow for the project.

AI assistance is used for architecture analysis, code generation, review and documentation. Product direction, integration decisions, infrastructure ownership and validation remain Alexander's responsibility.

## Technology direction

- Android mobile application
- offline maps and versioned data packages
- JSON-based operational layers
- Matrix messaging
- LiveKit real-time communications
- secure backend APIs
- Linux server infrastructure
- VPN-controlled update paths where required

The public portfolio will distinguish implemented MVP components from planned capabilities.

## Key decisions

### Offline-first rather than online-with-cache

**Reason:** loss of connectivity is a normal operating condition, not an exceptional failure.

### Reuse secure communication infrastructure

**Reason:** messaging and RTC are complex security and operational domains; integrating validated services is preferable to reimplementing them unnecessarily.

### Package-based map and layer delivery

**Reason:** versioned packages make field availability, rollback and controlled updates easier to reason about.

## Current result

The server foundation, integration direction and Android development environment have been prepared, and the project has a defined staged architecture. Public claims will be updated as individual mobile capabilities become reproducibly demonstrable.

## Evidence to publish

- sanitized mobile screenshots;
- package preparation example;
- offline/online state demonstration;
- architecture and synchronization diagram;
- map and layer sample using non-sensitive data;
- short video showing operation in an emulator or device.

## Security and redaction

The public case excludes operational locations, customer data, protected map layers, service credentials, real infrastructure addresses and sensitive deployment details.

## Next steps

1. Complete a reproducible offline map package.
2. Demonstrate loading and viewing structured layers without connectivity.
3. Define package signing, versioning and update validation.
4. Add a safe public communication demo.
5. Document measurable offline and recovery scenarios.