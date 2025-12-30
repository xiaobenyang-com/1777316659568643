# 图标数据服务 Iconify Icon

提供访问Iconify超过20万开源矢量图标的MCP服务器，支持图标集浏览、搜索及多框架使用示例获取。
Provide access to Iconify's MCP server with over 200,000 open-source vector ICONS, supporting icon set browsing, searching, and obtaining multi-framework usage examples.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| get_all_icon_sets | Browse all available icon collections from Iconify (200+ icon sets with 200,000+ icons). Returns a list of all icon sets with their metadata including name, total icons, author, license, and sample icons. |
| get_icon_set | Retrieve detailed information about a specific icon set including all available icons in that set. Provide the icon set prefix (e.g., 'mdi', 'fa', 'bi'). |
| search_icons | Search through Iconify's icon collection with flexible query parameters. Returns matching icons from all icon sets or a specific set. |
| get_icon_data | Retrieve specific icon data with usage examples for popular frameworks (React, Vue, Svelte, etc.). Provide the full icon name in format 'prefix:icon-name' (e.g., 'mdi:home', 'fa:user'). |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659568643](https://mcp.xiaobenyang.com/inspector/1777316659568643)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659568643](https://mcp.xiaobenyang.com/inspector/1777316659568643)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "图标数据服务": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659568643/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "图标数据服务": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659568643/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "图标数据服务": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659568643",
          },
          "transport": "stdio"
        }
      }
}

```
