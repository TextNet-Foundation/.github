# TNet

[![License: GPL v3+](https://img.shields.io/badge/License-GPLv3%2B-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Project](https://img.shields.io/badge/project-active-blue.svg)]()

**TNet** is a decentralized, text-oriented network built around lightweight protocols and human-readable communication over TCP. It provides a simple foundation for publishing, browsing, and serving text documents and binary resources without depending on the conventional web stack.

## Overview

TNet separates service discovery from content transfer and uses dedicated protocols for different kinds of resources.

The project focuses on:

- **Readable protocols** — request and response messages are designed to be understandable and easy to inspect.
- **Separation of concerns** — service discovery, text documents, and binary resources are handled by distinct protocols.
- **Lightweight clients and servers** — the network is intended to remain practical for terminal-based software and modest systems.
- **Self-hosting** — services can be operated independently.
- **Evolving security model** — TLS and SSH transport options are part of the ongoing protocol development.

TNet can be used for terminal-based browsing, low-bandwidth environments, self-hosted text services, long-term document archives, and experimentation with decentralized network protocols.

## Core protocols

TNet defines three core protocols:

| Protocol | Default port | Purpose |
|----------|--------------|---------|
| **UTNP** | 34 | Universal Text Negotiation Protocol — discovers services and negotiates which protocol a client should use. |
| **TMUTP** | 100 | TMkUp Transfer Protocol — transfers text documents written in TMkUp. |
| **TBIP** | 81 | TNet Binary Information Protocol — transfers binary resources such as images, audio, and video. |

All three protocols use TCP. UTNP is responsible for discovering the appropriate service endpoint; TMUTP and TBIP handle the corresponding resource transfers. Default ports can be adjusted in server configuration.

Full protocol documentation and version history are available in the [TNet-Protocols repository](https://github.com/TextNet-Foundation/TNet-Protocols).

## TMkUp

**TMkUp** is the markup language used to create text documents for TNet. It builds on familiar lightweight-markup concepts and adds features intended for interactive, richly formatted documents.

Its feature set includes:

- Headings, paragraphs, lists, tables, and code blocks.
- Text styling and ANSI color tags.
- Information blocks, color blocks, and spoilers.
- Interactive forms and form controls.
- Footnotes, comments, and variables.

See the [TMkUp repository](https://github.com/TextNet-Foundation/TMkUp) for the language documentation.

## Implementations and tools

- **[TBrowser](https://github.com/TextNet-Foundation/TBrowser)** — a terminal-based TNet browser written in Rust. It renders TMkUp documents, displays supported images in the terminal, and provides keyboard-driven navigation.
- **[tnet-tools](https://github.com/TextNet-Foundation/tnet-tools)** — a collection of Rust tools that includes UTNP, TMUTP, and TBIP servers, as well as a UTNP client. The servers support static resources and scripting.

See each repository for its current features, requirements, and build instructions.

## Documentation

- [TNet-Protocols](https://github.com/TextNet-Foundation/TNet-Protocols) — UTNP, TMUTP, and TBIP specifications.
- [TMkUp](https://github.com/TextNet-Foundation/TMkUp) — markup language documentation.
- [TBrowser](https://github.com/TextNet-Foundation/TBrowser) — browser usage and configuration.
- [tnet-tools](https://github.com/TextNet-Foundation/tnet-tools) — server and client tools, configuration, and scripting.

## Contributing

TNet is an evolving project. Contributions, testing, protocol discussions, and implementation work are welcome. Explore the repositories above to find the part of the project you are interested in.
