{
  "$schema": "https://opencode.ai/config.json",
  "provider": {
    "myprovider": {
      "npm": "@ai-sdk/openai-compatible",
      "name": "Llama.cpp",
      "options": {
        "baseURL": "http://192.168.18.195:8080/v1",
        "apiKey": "123456789"
      },
      "models": {
        "Qwen3.6-35B-A3B": {
          "name": "Qwen3.6-35B-A3B",
          "modalities": {
            "input": ["text", "image"]
          },
          "limit": {
            "context": 128000,
            "output": 65536
          }
        }
      }
    }
  },
  "mcp": {
    "context7": {
      "type": "remote",
      "url": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "YOUR_API_KEY"
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
