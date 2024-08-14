# MyriaD AI Toolbox powered by the Ethical Responsible Ai Consortium (E.R.A.C.) 🛠️

Welcome to the MyriaDAI Toolbox! This repository contains a collection of powerful tools that extend the functionality of AI models available at [MyriaDAI](https://myriadai.online). These tools allow you to interact with various APIs and perform internet searches to retrieve and manipulate data seamlessly. 

As always, use ethically and responsibly please, it keeps the government from making us track everything you do.

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
          { "name": "url", "in": "query", "required": false, "description": "URL to query.", "example": "https://myriadai.online" },
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
```
#### Features ⭐
Command Execution: Run specific commands to retrieve data from web pages.
Flexible URL Input: Specify the URL for targeted information extraction.
Screenshot Option: Take a screenshot of the page as needed.
Proxy Support: Easily use a proxy when accessing content.
Getting Started 🚀
Clone the repository:


git clone https://github.com/yourusername/myriadai-toolbox.git
Follow the API specifications to integrate and use the tools.
Contributing 🤝
We welcome contributions! Feel free to fork the repo, create a branch, and submit a pull request with your improvements!
License 📝
This project is licensed under the MIT License - see the LICENSE file for details.
Contact Me! 📫
For questions or support, reach out via GitHub Issues or check out my profile on MyriaDAI.



Feel free to copy and paste! If you need anything else, just let me know! 😊✨
