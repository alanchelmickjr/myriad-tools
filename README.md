# Myriad AI Toolbox 🛠️
#### powered by the Ethical Responsible Ai Consortium (E.R.A.C.) 

Welcome to the MyriadAi Toolbox! This repository contains a collection of powerful tools that extend the functionality of AI models available at [MyriaDAI](https://myriadai.online). These tools allow you to interact with various APIs and perform internet searches to retrieve and manipulate data seamlessly. 

As always, use ethically and responsibly please, it keeps the government from making us track everything you do.  In the Builder/Pro version you can drag and drop these tools with no code. 

## During this BETA testing phase while we build the tools be free to test.  This tool is functioning and an API Key will be required in 3 days, best to grab your key now at https://www.multion.ai/ and put in the the headers section, more examples coming soon.  Without this key you will need a subscription to access the Internet directly with your models.
<img width="170" alt="multion.ai" src="https://github.com/user-attachments/assets/7b263c91-7ce9-4737-a1f7-3dd5b37341ad">

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
          {
            "name": "cmd",
            "in": "query",
            "required": true,
            "description": "Items to search the Internet for",
            "example": "summarize",
            "schema": {
              "type": "string"
            }
          },
          {
            "name": "url",
            "in": "query",
            "required": true,
            "description": "URL to query.",
            "example": "https://myriadai.online",
            "schema": {
              "type": "string"
            }
          },
          {
            "name": "sshot",
            "in": "query",
            "required": false,
            "description": "Flag for taking a screenshot.",
            "example": false,
            "schema": {
              "type": "boolean"
            }
          },
          {
            "name": "proxy",
            "in": "query",
            "required": false,
            "description": "Flag for using a proxy.",
            "example": false,
            "schema": {
              "type": "boolean"
            }
          },
          {
            "name": "sessionId",
            "in": "query",
            "required": false,
            "description": "Session ID to maintain state across multiple requests.",
            "example": "abc123",
            "schema": {
              "type": "string"
            }
          }
        ],
        "responses": {
          "200": {
            "description": "Successful response with the retrieved information",
            "content": {
              "application/json": {
                "schema": {
                  "type": "object",
                  "properties": {
                    "result": {
                      "type": "string",
                      "description": "Retrieved information."
                    }
                  }
                }
              }
            }
          },
          "400": {
            "description": "Bad request"
          },
          "500": {
            "description": "Internal server error"
          }
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


#### Getting Started 🚀

0. this beta version does not require access codes, abuse prevention will require implementing access codes so come back here if you get a permission error and update your code


1. copy and paste the JSON file you wish to use into a new Tool you just created by Clicking on "New Tool" in your left side drawer (under the lightning bolt) after you signup for Free at https://myriadai.online
3. press ! while using gpt-4o and select your tool from the list that opens when you type ! in the input
4. wait patiently as your ai assistant searches the internet and returns the response


5. also while creating an assistant you may select this tool for that assistant, please use gpt-4o during beta, that will tie internet searches to that agents tool pipeline


#### Contributing 🤝
We welcome contributions! Feel free to fork the repo, create a branch, and submit a pull request with your improvements!
License 📝
This project is licensed under the MIT License - see the LICENSE file for details.
Contact Me! 📫
For questions or support, reach out via GitHub Issues or check out my profile on MyriaDAI.



#### Feel free to copy and paste! If you need anything else, just let me know! 😊✨
