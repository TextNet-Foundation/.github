# TNet

[![License: GPL v3+](https://img.shields.io/badge/License-GPLv3%2B-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Spec Version](https://img.shields.io/badge/spec-v1.0-lightgrey.svg)]()
[![Status](https://img.shields.io/badge/status-stable-brightgreen.svg)]()

TNet is a decentralized text network built on lightweight protocols for efficient, human-readable communication. It provides an alternative to the modern web for text-oriented services, with a focus on simplicity, performance, and compatibility.

## Overview

TNet consists of a set of protocols and tools that enable browsing and serving text and binary information over TCP. The core design principles are:

- Minimal overhead and human-readable wire formats.
- Separation of concerns: discovery, text transfer, binary transfer.
- Compatibility with existing text protocols where possible.
- Extensibility through versioned specifications.

The network is intended for:
- Terminal-based browsing.
- Low-bandwidth environments.
- Long-term archival of text documents.
- Experimentation with decentralized protocols.

## Protocols

TNet currently defines three core protocols:

| Protocol | Port | Purpose |
|----------|------|---------|
| **UTNP** | 34 | Universal Text Negotiation Protocol — service discovery and protocol negotiation. |
| **TMUTP** | 100 | TMkUp Transfer Protocol — transfer of TMkUp documents. |
| **TBIP** | 81 | TNet Binary Information Protocol — transfer of images, audio, video. |

All protocols use plain-text request/response formats over TCP. Full specifications are available in the [TNet Protocols repository](https://github.com/TextNet-Foundation/TNet-Protocols).

## TMkUp

TMkUp is the markup language used for text documents in TNet. It combines the simplicity of Markdown with ANSI colors, interactive forms, and structured blocks. Key features:

- Headings, lists, tables, code blocks.
- ANSI color tags (`{red}...{/red}`).
- Info blocks, color blocks, spoilers.
- Forms with text fields, checkboxes, radio buttons, selects.
- Footnotes, comments, variables.

See the [TMkUp v2.0 specification](https://github.com/TextNet-Foundation/TMkUp) for details.

## Implementations

- **[TBrowser](https://github.com/TextNet-Foundation/TBrowser)** — terminal browser for TNet written in Rust.
- Server implementations are planned; contributions are welcome.

## Documentation

- [TNet Protocols Specification](https://github.com/TextNet-Foundation/TNet-Protocols) — UTNP, TMUTP, TBIP.
- [TMkUp v2.0 Specification](https://github.com/TextNet-Foundation/TMkUp).
- [TBrowser README](https://github.com/TextNet-Foundation/TBrowser) — usage and configuration.

## Building

Each implementation has its own build instructions. For TBrowser, see its repository.

## Contributing & Contact

To help the project grow and contribute, please write to me, TimeStop34, the creator of this project.
