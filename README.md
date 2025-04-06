# Installing uv package manager
```
curl -LsSf https://astral.sh/uv/install.sh | sh
```

# Project setup
1. Create and Initialize project
```
# Create a new directory for our project
uv init mcp-server
cd mcp-server

# Create virtual environment and activate it
uv venv
source .venv/bin/activate  # On Windows use: .venv\Scripts\activate

# Install dependencies
uv add "mcp[cli]" httpx
```

2. Add Content in mcp servr file 
```
main.py
```

3. Start the server
```
uv run main.py
```

# Edit config `claude_desktop_config.json`
```
{
    "mcpServers" : {
        "filesystem" : {
            "command" : "uv",
            "args" : [
                "--directory",
                "D:\\claude_mcp\\mcp-server",
                "run",
                "main.py"
            ]
        }
    }    
}
```