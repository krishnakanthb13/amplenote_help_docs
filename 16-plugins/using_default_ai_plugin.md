# Using the default AmpleAI plugin

> [← Help Index](../00-index.md) · Category: [Plugins](./index.md) · [Source ↗](https://www.amplenote.com/help/using_default_ai_plugin)

## Using the AmpleAI plugin

The AmpleAI plugin is developed by Amplenote staff to help users leverage large language models. "[The most updated plugin documentation is located on the plugin's marketplace page](https://www.amplenote.com/plugins/75h72w8xghmHDdr8p5FiX6fh)" with additional details available here.

---

## 🪄 AmpleAI: Features

Functionality is organized by invocation method.

### 🔍 Search Agent

This tool helps users find historical notes on specific topics. Access it via `/search` in the slash menu or Quick Open (Cmd-O/Ctrl-O).

**How it works:** The agent generates keywords from your input and collects relevant notes. Most searches complete in approximately 30 seconds.

**Use cases:**
- Link research topics together without requiring tags
- Discover poorly named or untagged notes
- Reduce naming effort for future discoverability

**Example:** A note titled "Christmas 2027" becomes discoverable when searching "Gift ideas."

---

## App Option (Slash menu or Quick Open) Features

Accessible by typing `/` followed by the command or using Quick Open:

- **Add Provider API key**: Configure keys for Google/Gemini, OpenAI/ChatGPT, Anthropic/Claude, Grok, or Deepseek
- **AI Search Agent**: Access the search functionality
- **Question & answer** (aka `Answer`): Ask the LLM a question
- **Converse/Chat** (aka `Converse (chat) with AI`): Have multi-turn conversations
- **Show AI Usage by Model**: View LLM usage statistics since last restart
- **Look up available Ollama models**: Verify Ollama installation and availability

---

## Text Selection Features

Select text and choose options from the rightmost toolbar icon:

- **Thesaurus**: Get 10 contextual synonyms
- **Answer question**: AI-generated response to highlighted questions
- **Complete a sentence**: Predict following text
- **Revise**: Suggestions for text improvement
- **Rhymes with**: Find 10 words that rhyme with selection

---

## Note option features

Available from the triple-dot menu when a note is open:

- **Sort groceries**: Arrange grocery items by store aisle
- **Revise**: Suggest note improvements
- **Summarize**: Condense note content

---

## Evaluation/Insert text features

Triggered by entering `{` followed by commands:

- **Complete**: Answer questions or finish thoughts
- **Continue**: Generate similar-style text
- **Image from preceding**: Generate DALL-E images from preceding text
- **Image from prompt**: Create images from user-entered prompts
- **Suggest tasks**: Recommend tasks based on note title/content

---

## 🏦 Search models available

| API Label | Provider | Input Price ($/1M) | Output Price ($/1M) | Release Date | Notes |
|-----------|----------|-------------------|-------------------|--------------|-------|
| GPT-5.2 (Default) | OpenAI | $1.75 | $14.00 | Aug 2025 | Flagship agentic model. Cached input: $0.175. |
| GPT-5.2 Pro | OpenAI | $21.00 | $168.00 | Aug 2025 | High-precision/Zero-failure tier. No cached discount listed. |
| GPT-5 Mini | OpenAI | $0.25 | $2.00 | Aug 2025 | High-throughput. Cached input: $0.025. Replaces GPT-4o mini. |
| GPT-4.1 | OpenAI | $3.00 | $12.00 | Apr 2025 | Mid-cycle update. Cached input: $0.75. Fine-tuning available. |
| GPT-4.1 Mini | OpenAI | $0.80 | $3.20 | Apr 2025 | Cached input: $0.20. |
| GPT-4.1 Nano | OpenAI | $0.20 | $0.80 | Apr 2025 | Edge/Ultra-light tier. Cached input: $0.05. |
| o4-mini | OpenAI | $1.10 | $4.40 | Apr 2025 | Reasoning model. Cached input: $0.28–$1.00 depending on region. |
| o3 | OpenAI | $2.00 | $8.00 | ~Apr 2025 | Global pricing. Cached input: $0.50. |
| o3-pro | OpenAI | $20.00 | $80.00 | June 2025 | Specialized reasoning. Note: Sources indicate variance ($20-$60). |
| o1 | OpenAI | $15.00 | $60.00 | Dec 2024 | Early reasoning flagship. Cached input: $7.50. |
| Gemini 3.0 Pro (Default) | Google | ~$1.25* | ~$10.00* | Nov 2025 | Est. based on 2.5 Pro pricing & "Paid Tier" tiers. |
| Gemini 2.5 Pro | Google | $1.25 | $10.00 | June 2025 | Standard PayGo. Grounding add-ons extra. |
| Gemini 2.5 Flash | Google | $0.10* | $0.40* | June 2025 | Est. based on low-tier pricing blocks. |
| Gemini 2.0 Flash | Google | ~$0.10* | ~$0.40* | Feb 2025 | High-speed multimodal. |
| Grok 4 (Default) | xAI | $3.00 | $15.00 | July 2025 | Frontier reasoning model. Tool calls $5/1k. |
| Grok 4.1 Fast | xAI | $0.20 | $0.50 | Nov 2025 | Market Floor. Price applies to reasoning & non-reasoning modes. |
| Grok 3 | xAI | $3.00 | $15.00 | Feb 2025 | Replaced by Grok 4. Pricing mirrored in legacy access. |
| Sonar Pro | Perplexity | $3.00 | $15.00 | Feb 2025 | Includes search. Plus request fee ($6–$14/1k). |
| Sonar | Perplexity | $1.00 | $1.00 | Feb 2025 | Llama 3.3 based. Plus request fee ($5–$12/1k). |
| Sonar Deep Research | Perplexity | $2.00 | $8.00 | 2025 | Specialized for long-form report generation. |
| Claude Opus 4.5 | Anthropic | $15.00 | $75.00 | Late 2025 | For heavy reasoning tasks |
| Claude Sonnet 4.5 (Default) | Anthropic | — | — | — | Anthropic best for multipurpose workload |
| Claude Opus 4 | Anthropic | $15.00 | $75.00 | Late 2025* | Data via comparative report; direct pricing page not in snippets. |

---

## Choosing an AI backend

"As of 2026, we recommend setting up AmpleAI with multiple AI providers, like OpenAI (ChatGPT), Anthropic (Claude), and Google (Gemini)." Users can call `Add provider API key` repeatedly to add keys for multiple providers.

Technical users may connect Ollama for local models, though the documentation notes that frontier models offer sufficient power and cost-effectiveness that typical users won't benefit from this option.

**Note:** OpenAI is currently the only supported provider for image generation. Additional provider integrations are planned for Q1 2026.

### Express setup

For users with existing accounts at any supported provider:
1. Install the AmpleAI plugin
2. Run any feature
3. Paste your API key when prompted
4. The system securely persists the key for future use

### OpenAI setup

1. Sign up at https://platform.openai.com/signup
2. Visit https://platform.openai.com/account/api-keys
3. Verify account credits are available

### Gemini, Anthropic, Grok, Deepseek setup

"When you initiate the `Add AI provider` action after installing AmpleAI, we'll provide you the link to follow to retrieve your API key."

### Ollama setup

1. Install Ollama from https://ollama.ai/download
2. Install an LLM: `ollama run mistral`
3. Stop the resident server (Quit from toolbar)
4. Run this command in console:

```
OLLAMA_ORIGINS=https://plugins.amplenote.com ollama serve
```

5. Test via Quick Open → "Look up available Ollama models"

If unsuccessful, run `ps aux | grep ollama` to find and kill existing servers, then retry.

---

## Setting up Ollama

Follow the steps outlined above. The documentation notes that "mistral" offers optimal results as of early 2024.

---

## AmpleAI Rationale & Roadmap

The plugin is offered separately from Amplenote's default installation for several reasons:

- **Demonstrate plugin potential**: "We want to give our programmer (or aspiring programmer)-users a living, breathing example of how powerful a plugin can be."
- **Support rapid AI evolution**: "If we build & test an AI integration with our usual level of rigor, there is a good chance that in 6-12 months that code will be deprecated."
- **Crowdsource prompt optimization**: "There are no prompt engineering experts, so anyone might discover newer, more effective, prompts to contribute back to the code."
- **Eliminate markups**: By allowing user-selected LLM backends, Amplenote offers lowest-cost access without platform markups
- **Dogfood opportunities**: Using the plugin API internally ensures reliable evolution

---

## AmpleAI Source Repo

The plugin is open source. "[Check out its open source Github repo here](https://github.com/alloy-org/ai-plugin/)."
