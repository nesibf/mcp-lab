## Step 1. Clone the repo
```bash
git clone https://github.com/toktechteam/mcp-lab.git
cd mcp-lab
```

## Step 2. Setup environment
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

## Step 3. Start Kubernetes locally (kind/minikube)
```bash
kind create cluster --name mcp-lab
```

## Step 4. Run the agent
```bash
python server.py
python agent.py
python web_server.py
```

Now open web_interface.html and try: “Show me pods failing in dev namespace”

## What’s happening under the hood
- User → natural language query
- AI Agent → interprets intent (OpenAI GPT)
- MCP Protocol → validates & enforces RBAC
- Kubernetes → executes safely
- Web UI → displays response
