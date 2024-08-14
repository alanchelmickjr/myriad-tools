# MyriaDAI Toolbox 🛠️

Welcome to the MyriaDAI Toolbox! This repository contains a collection of powerful tools that extend the functionality of AI models available at [MyriaDAI](https://myriadai.online). These tools allow you to interact with various APIs and perform internet searches to retrieve and manipulate data seamlessly. 

## Look Inside! 🕵️‍♀️

### Web Surfing Tool 🌐

#### Overview
The Web Surfing Tool enables you to surf the internet and extract specific information based on commands and URL parameters.

#### API Specification
This tool uses the OpenAPI Specification:

```json
{
  "openapi": "3.1.0",
  "info": {
    "title": "Web Surfing Tool",
    "description": "This tool allows you to surf the internet and retrieve data based on a specific command and URL.",
    "version": "v1.0.0"
  },
  "servers": [
    {
      "url": "https://myriadai.online/api/chat/tools/multion"
    }
  ],
  "paths": {
    "/": {
      "get": {
        "description": "Execute a command on a specific URL to retrieve information",
        "operationId": "SurfWeb",
        "parameters": [
          { "namecmd", "in": "query", "required": true, "description": "Command to execute.", "example": "summarize" },
          { "name": "url", "in": "query", "required": true, "description": "URL to query.", "example": "https://www.albanyumc.org" },
          { "name": "sshot", "in": "query", "required": false, "description": "Flag for taking a screenshot.", "example": false },
          { "name": "proxy", "in": "query", "required": false, "description": "Flag for using a proxy.", "example": false }
        ],
        "responses": {
          "200": {
            "description": "Successful response with the retrieved information",
            "content": { "application/json": { "schema": { "type": "object", "properties": { "result": { "type": "string", "description": "Retrieved information." }}}}}  
          },
          "400": { "description": "Bad request" },
          "500": { "description": "Internal server error" }
        }
      }
    }
  }
}
