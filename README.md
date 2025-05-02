# Random Cat MCP

A Model Context Protocol (MCP) tool for generating random cat images using the [cataas.com](https://cataas.com) API as a data source.

## Features

This tool provides a simple MCP tool to generate cat images with capabilities to:
- Add custom text overlay on images
- Filter cat images by specific tags
- Return image URLs

## Sample configuration
```bash
{
    "servers": {
        "random-cat-mcp": {
            "command": "uv",
            "args": [
                "--directory",
                "D:/random-cat-mcp",
                "run",
                "src/random_cat_mcp.py"
            ],
            "env": {},
            //"transportType":"stdio"
        }
    }
}
```

### Using the MCP Tool

This project defines the `random_cat_image` tool which accepts two parameters:
- `addition_message`: Text to display on the cat image (maximum 10 characters)
- `tag`: A list of tags for filtering cat image types

## Available Tags

The tool supports numerous tags for filtering cat image types, such as "cute", "happy", "sleepy", "orange", etc. For a detailed list of tags, please refer to the source code documentation.

## Technical Implementation

- Uses FastMCP to create an MCP service
- Uses the requests library for HTTP requests
- Built on the cataas.com API for fetching cat images

## Dependencies

- mcp[cli] >= 1.7.0
- requests >= 2.32.3
- httpx >= 0.28.1

