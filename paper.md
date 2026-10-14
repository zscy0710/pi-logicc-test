# A Note on Tool-Calling Through MCP

## Abstract

This note records how an OpenAI-compatible adapter can expose client-supplied
tools to a chat platform that only accepts tools through MCP connections.

## Method

The adapter registers the caller's tool definitions as an MCP server, then
translates the platform's tool-input events into OpenAI tool_calls.

## Result

The model calls the client's tools and the client executes them.
