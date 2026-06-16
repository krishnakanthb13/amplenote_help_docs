# Plugin Example: AI Plugin

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/example_plugin_ai)

## Overview

AmpleAI is an AI plugin for Amplenote that provides access to multiple LLM providers including OpenAI, Anthropic, Google Gemini, Grok, and DeepSeek, plus local Ollama support.

## Key Features

### App Option Features (Quick Open/Slash Menu)
- **Note Search**: AI agent searches notes and generates summaries
- **Question & Answer**: Ask questions to configured LLM
- **Converse/Chat**: Back-and-forth conversations with context memory
- **Provider Management**: Switch between favorite AI models

![Question and answer feature](https://images.amplenote.com/c6cf84d6-ceb4-11ed-a7db-d2ab91c23399/016e6e31-a256-4109-ad5b-aff3b622e3e2.jpg)

### Selected Text Features
- **Thesaurus**: Get 10 contextual synonym suggestions
- **Answer Question**: AI answers highlighted questions
- **Complete Sentence**: Generate text continuations
- **Revise**: Request improvement suggestions
- **Rhymes With**: Find 10 rhyming words

![Selected text toolbar options](https://images.amplenote.com/c6cf84d6-ceb4-11ed-a7db-d2ab91c23399/53eb85c9-e7d3-4a7f-92e3-b68fa595113c.png)

![Thesaurus feature](https://images.amplenote.com/c6cf84d6-ceb4-11ed-a7db-d2ab91c23399/847c257f-1954-454f-8b78-41ce7e1b6927.png)

![Revise feature](https://images.amplenote.com/c6cf84d6-ceb4-11ed-a7db-d2ab91c23399/fb6395c8-eca2-4c8d-b6a2-7bcabc0d14fd.jpg)

![Rhymes with feature](https://images.amplenote.com/c6cf84d6-ceb4-11ed-a7db-d2ab91c23399/79cb5b01-6516-4c72-bb85-c6b0095b33eb.png)

### Note Option Features
- **Sort Groceries**: Organize grocery lists by store aisle
- **Revise**: Suggest improvements for entire note
- **Summarize**: Create note summaries

![Sort groceries demo](https://images.amplenote.com/f8671754-e091-11ed-83b5-a2c43e1aef0c/76aec2a1-6d95-4c85-8139-c6ae8996514c.gif)

![Summarize feature](https://images.amplenote.com/c6cf84d6-ceb4-11ed-a7db-d2ab91c23399/0d91610f-b58c-4f6d-9de1-b0c59a898f6c.jpg)

### Evaluation/Insert Text Features
- **Complete**: Finish thoughts from preceding text
- **Continue**: Continue in similar style
- **Image Generation**: Create images from prompts
- **Suggest Tasks**: Generate relevant task suggestions

![Continue feature](https://images.amplenote.com/c6cf84d6-ceb4-11ed-a7db-d2ab91c23399/adb11c01-6f67-48a9-91a2-719d4f03f854.png)

![Image from preceding feature](https://images.amplenote.com/c6cf84d6-ceb4-11ed-a7db-d2ab91c23399/0372bf67-ed76-4cd5-9862-3f7d178463c3.png)

![Suggest tasks feature](https://images.amplenote.com/c6cf84d6-ceb4-11ed-a7db-d2ab91c23399/60aa8016-aa7a-461b-bdc4-e0183bcb55c1.png)

## Configuration

### Supported Providers and API Keys

| Provider | API Key Location |
|----------|-----------------|
| **OpenAI** | https://platform.openai.com/account/api-keys |
| **Anthropic** | https://console.anthropic.com/settings/keys |
| **Gemini** | https://aistudio.google.com/app/api-keys |
| **Grok** | https://console.x.ai/team/default/api-keys |
| **DeepSeek** | https://platform.deepseek.com/api_keys |
| **Ollama** | Local installation required |

### Default Models
- OpenAI: gpt-5.2
- Anthropic: claude-sonnet-4-5
- Gemini: gemini-3-pro-preview
- Grok: grok-4-1-fast
- DeepSeek: deepseek-chat

### Plugin Settings
- **Preferred AI Models**: Comma-separated list (e.g., "gpt-5.1, claude-sonnet-4-5")
- **Search Result Tag**: Default is `plugins/ample-ai/search-results`

## Version History

**January 2026**: Improvements to complete/continue actions across providers

**December 2025**: Added Agent Search feature; improved note searching with common keywords

**December 8, 2025**: Added Anthropic, Gemini, and Grok as remote provider options; updated default LLM models

**June 2024 and earlier**: Progressive feature additions including streaming, JSON responses, image generation, thesaurus, and grocery sorting

## Installation

Access the plugin through:
- [Plugin Directory](https://www.amplenote.com/plugins/75h72w8xghmHDdr8p5FiX6fh)
- [Direct Install Link](https://www.amplenote.com/account/plugins?source-token=75h72w8xghmHDdr8p5FiX6fh)
- [Public Note View](https://public.amplenote.com/75h72w8xghmHDdr8p5FiX6fh)

## Technical Details

The plugin includes sophisticated code for:
- JSON parsing and error recovery from LLM responses
- Stream handling across multiple provider formats
- Token limit management per model
- Request retry logic with timeout handling
- Search agent functionality with multi-phase ranking

---

**Note**: Full implementation code is available in the source; this documentation covers user-facing features and configuration.
