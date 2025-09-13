# Awesome Scientific MCP


> A curated list of awesome MCP (Model Context Protocol) servers designed for scientific discovery.

This project aims to provide a foundational ecosystem of MCP for building "AI Scientist" systems capable of autonomous scientific discovery.

---

## Motivation

We are in an era of AI for Science. Building AI systems capable of autonomous scientific exploration is key to the next scientific revolution. As argued in the paper *Autonomous Scientific Discovery Through Hierarchical AI Scientist Systems*, a rich ecosystem of specialized, composable MCP servers is a necessary cornerstone for creating hierarchical, autonomous "AI Scientists". These servers act as standardized digital lab equipment, empowering AI agents to perform complex scientific tasks.

However, efficiently expanding this ecosystem is a challenge. To address this, the research in *Code2MCP: Automatically Convert GitHub Repository to MCP Server* explores methods to automatically convert the vast number of existing scientific code repositories into standardized MCP services. This dramatically lowers the barrier for researchers to contribute their tools, making it possible to integrate valuable scientific code into AI workflows.

---

## What is MCP (Model Context Protocol)?

MCP (Model Context Protocol) is an open-source standard for connecting AI applications to external systems.

Using MCP, AI applications like Claude Code or Cursor can connect to data sources (e.g. local files, databases), tools (e.g. search engines, calculators) and workflows (e.g. specialized prompts)—enabling them to access key information and perform tasks.

Think of MCP like a **USB-C port for AI applications**. Just as USB-C provides a standardized way to connect electronic devices, MCP provides a standardized way to connect AI applications to external systems.


---

## How to Use an MCP Server

You can integrate MCP servers into AI-powered development environments to extend their capabilities. The `[mcp]` address is the installable endpoint for the tool.

### In Claude Code
https://docs.anthropic.com/en/docs/claude-code/mcp

MCP servers can be configured in three different ways depending on your needs:

Option 1: Add a remote SSE server:
SSE (Server-Sent Events) servers provide real-time streaming connections. Many cloud services use this for live updates.

```
# Basic syntax
claude mcp add --transport sse <name> <url>

# Real example: Connect to Linear
claude mcp add --transport sse linear https://mcp.linear.app/sse

# Example with authentication header
claude mcp add --transport sse private-api https://api.company.com/mcp \
  --header "X-API-Key: your-key-here"
```

Option 2: Add a remote HTTP server
HTTP servers use standard request/response patterns. Most REST APIs and web services use this transport.

```
# Basic syntax
claude mcp add --transport http <name> <url>

# Real example: Connect to Notion
claude mcp add --transport http notion https://mcp.notion.com/mcp

# Example with Bearer token
claude mcp add --transport http secure-api https://api.example.com/mcp \
  --header "Authorization: Bearer your-token"
```



---

## MCP Servers

The following categories are based on the classification from nature.com.

### Physical sciences

* **IO Aerospace**: A Model Context Protocol (MCP) server for aerospace and astrodynamics calculations, providing tools for celestial body ephemeris, orbital mechanics, and space mission analysis. [code](https://github.com/IO-Aerospace-software-engineering/mcp-server) [mcp](https://mcp.io-aerospace.org/sse)




### Earth and environmental sciences

*(This section is currently empty. Contributions are welcome!)*

### Biological sciences

* **BioMCP**: BioMCP is an open source (MIT License) toolkit that empowers AI assistants and agents with specialized biomedical knowledge. [code](https://github.com/genomoncology/biomcp)

* **biothings-mcp**: This server implements the Model Context Protocol (MCP) for BioThings, providing a standardized interface for accessing and manipulating biomedical data.  [code](https://github.com/longevity-genie/biothings-mcp)
### Health sciences

* **Pubmed MCP**: A server for searching the Pubmed biomedical literature database. [code](https://github.com/user/repo) [mcp](https://pubmed-mcp.replit.app)

* **gget-mcp**: MCP (Model Context Protocol) server for the gget bioinformatics library. [code](https://github.com/longevity-genie/gget-mcp)

* **opengenes-mcp**: MCP (Model Context Protocol) server for OpenGenes database. [code](https://github.com/longevity-genie/opengenes-mcp)

* **synergy-age-mcp**: MCP (Model Context Protocol) server for SynergyAge database.[code](https://github.com/longevity-genie/synergy-age-mcp) [paper](https://www.nature.com/articles/s41597-020-00710-z)

* **fhir-mcp-server**: The FHIR MCP Server is a Model Context Protocol (MCP) server that provides seamless integration with FHIR APIs. [code](https://github.com/wso2/fhir-mcp-server)

* **medical-mcp**: A Model Context Protocol (MCP) server that provides comprehensive medical information by querying multiple authoritative medical APIs including FDA, WHO, PubMed, and RxNorm. [code](https://github.com/JamesANZ/medical-mcp)

* **omop_mcp**: Model Context Protocol (MCP) server for mapping clinical terminology to Observational Medical Outcomes Partnership (OMOP) concepts using Large Language Models (LLMs). [code](https://github.com/OHNLP/omop_mcp) [paper](https://arxiv.org/abs/2509.03828)

### Scientific community and society

* **Arxiv Search MCP**: A server for searching on the ArXiv.org preprint server. [code](https://github.com/user/repo) [mcp](https://your-mcp-server-url.com)
* **Tavily Search MCP**: A server for web searches using the Tavily API, which is optimized for research and LLMs. [code](https://github.com/user/repo) [mcp](https://your-mcp-server-url.com)

---

## How to Contribute

Contributions are welcome! If you have developed or know of a scientific MCP server not yet on this list, please help us add it.

Please follow these steps:

1.  **Fork** this repository.
2.  Create a **new branch** for your changes.
    ```bash
    git checkout -b feature/add-awesome-mcp
    ```
3.  Add your MCP server under the relevant category in `README.md`, keeping the list in alphabetical order. Please adhere to the following format:
    ```markdown
    - **MCP Name**: A brief, one-sentence description of the server's function. [code](https://github.com/user/repo) [paper](https://example.com/paper.pdf) [mcp](https://your-mcp-server-url.com)
    ```
4.  **Commit** your changes.
    ```bash
    git commit -m 'feat: Add [MCP Name]'
    ```
5.  **Push** to the branch.
    ```bash
    git push origin feature/add-awesome-mcp
    ```
6.  Create a new **Pull Request**.

We will review your contribution and merge it as soon as possible. Thank you for helping to build this ecosystem!

---

## Citation

If you find this repository useful in your research, please cite these two papers:

```latex
@article{yue2025autonomous,
  title={Autonomous Scientific Discovery Through Hierarchical AI Scientist Systems},
  author={Yue, Ling and Di, Shimin and Pan, Shaowu},
  journal={Preprints, July},
  year={2025}
}

@article{ouyang2025code2mcp,
  title={Code2MCP: A Multi-Agent Framework for Automated Transformation of Code Repositories into Model Context Protocol Services},
  author={Ouyang, Chaoqian and Yue, Ling and Di, Shimin and Zheng, Libin and Pan, Shaowu and Zhang, Min-Ling},
  journal={arXiv preprint arXiv:2509.05941},
  year={2025}
}
```

