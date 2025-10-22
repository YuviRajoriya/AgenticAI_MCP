Agentic AI with Model Context Protocol (MCP)

This project implements an Agentic AI system that connects a Groq-hosted LLM (qwen-qwq-32b model) with various tools through a custom Model Context Protocol (MCP) server. The system enhances the LLM's capabilities by providing contextual information from Wikipedia, internet search (via Tavily API), and financial data (via Yahoo Finance API).

About MCP

The Model Context Protocol (MCP) is an open standard developed by Anthropic to standardize how applications provide context to large language models (LLMs). It facilitates seamless integration between LLM applications and external data sources and tools, allowing AI systems to interact dynamically with various services through a standardized interface.

Key Features of MCP:

Standardization: Provides a universal protocol for interfacing AI assistants with structured tools and data layers.
Modular Architecture: Follows a client–server pattern over a persistent stream, typically mediated by a host AI system.
Dynamic Introspection: Supports dynamic discovery of tools and resources through methods like tools/list and resources/list.
Security: Incorporates host-mediated authentication and supports secure transport protocols.​ By adopting MCP, developers can build AI applications that are more interoperable, secure, and capable of complex workflows.​

To add new tools to the MCP server:​

Define the Tool: Create a new function that handles the specific task or data retrieval.​
Register the Tool: Update the server's tool registry to include the new function, specifying the tool's name and description.​
Handle Requests: Ensure the server can route incoming requests to the appropriate tool based on the query.​ This modular approach allows for easy expansion of the server's capabilities, enabling the language model to access a broader range of contextual information.

Features

MCP Server: Central hub that provides access to various tools
Three Integrated Tools:
Wikipedia Search - for factual information retrieval
Internet Search - powered by Tavily API for comprehensive web results
Yahoo Finance API - for real-time stock and financial data
Groq API Integration: Ultra-fast LLM processing using qwen-qwq-32b model
Client-Server Architecture: Clean separation between tool management and LLM interaction


