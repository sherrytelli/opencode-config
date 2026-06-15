# OpenCode Setup Instructions

To set up OpenCode with the provided configuration, follow these steps:

1. **Create a file** named `~/.config/opencode/opencode.json`.
2. **Paste the following JSON configuration in the opencode.json file:**

```json
{
  "myprovider": {
    "npm": "@ai-sdk/openai-compatible",
    "name": "Llama.cpp",
    "options": {
      "baseURL": "http://ip-adderss/v1",
      "apiKey": "123456789"
    },
    "models": {
      "Qwen3.6-35B-A3B": {
        "name": "Qwen3.6-35B-A3B",
        "limit": {
          "context": 128000,
          "output": 65536
        }
      }
    }
  },
  "mcp": {
    "context7": {
      "type": "remote",
      "url": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "API-KEY"
      },
      "enabled": true
    },
    "playwright": {
      "type": "local",
      "command": [
        "npx",
        "@playwright/mcp@latest"
      ],
      "enabled": true
    },
    "ddg-search": {
      "type": "local",
      "command": [
        "uvx",
        "duckduckgo-mcp-server"
      ],
      "enabled": true
    }
  }
}
```

3. **Ensure you have the required dependencies installed**, such as `@ai-sdk/openai-compatible` and 
`Llama.cpp`.

4. **Run the setup script** (if provided) to initialize OpenCode with your configuration.

