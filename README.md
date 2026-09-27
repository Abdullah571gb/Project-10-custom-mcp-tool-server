# 🔌 Project 10: Custom MCP Tool Server

A complete Model Context Protocol (MCP) server exposing 6 custom tools, 2 resources, and 2 prompt templates — built to work as a universal AI tool backend across multiple frameworks and platforms.

---

## 📌 What This Project Does

This project builds a standalone MCP server that any MCP-compatible AI system can plug into and use — instead of building tools separately for every framework, this server exposes them once and connects everywhere.

---

## 🧰 MCP Tools Built

| Tool | Function |
|------|----------|
| **get_weather** | Current weather for any city |
| **get_tech_news** | Latest AI and tech headlines |
| **calculate** | Mathematical calculations |
| **qualify_lead** | BANT-based lead scoring |
| **get_study_progress** | Learning journey tracker |
| **format_automation_report** | Professional report formatting |

---

## 📦 MCP Resources

- `automation://learning-progress`
- `automation://tool-stack`

---

## 💬 MCP Prompts

- `qualify_lead_prompt`
- `daily_briefing_prompt`

---

## ⚙️ How It Connects
            Custom MCP Server
            (6 Tools, 2 Resources, 2 Prompts)
                    │
  ┌─────────────────┼─────────────────────┐
  ↓                 ↓                       ↓

Python Agents n8n (via HTTP Any MCP-compatible
(LangChain, via wrapper + ngrok) client (via stdio)
tool wrappers)


One server, multiple ways to connect — no need to rebuild tools separately for each framework.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **Python MCP SDK** | Builds the MCP server itself |
| **Flask** | Exposes tools over HTTP for n8n |
| **ngrok** | Makes the local server reachable externally |
| **LangChain** | Connects Python agents to the MCP tools |
| **n8n HTTP Request Node** | Calls MCP tools from n8n workflows |

---

## 💡 Why MCP Matters

MCP works like a universal connector for AI tools — build a tool once, and it becomes usable across any framework or AI client that supports the protocol, rather than rebuilding the same tool separately for every platform.

---

## 📷 Screenshots

![MCP Server Code](mcp-server-code.png)
*Python code defining the MCP tools, resources, and prompts*

![Tool in Action](output-tool-demo.png)
*Example of a tool being called and returning a result*

![n8n Integration](output-n8n-integration.png)
*n8n calling an MCP tool via the HTTP wrapper*

---

## 🎯 Key Learning

How to design and build an MCP server that exposes tools, resources, and prompts in a standardized way — and how to connect that single server to multiple different clients (Python agents, n8n, and any MCP-compatible tool) without duplicating logic.

---

## 👤 Author

Built by Abdullah as part of a self-directed AI Automation learning program.
