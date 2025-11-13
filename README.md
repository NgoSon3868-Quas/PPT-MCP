# Cấu hình MCP Server PowerPoint

Repository này chứa cấu hình MCP Server PowerPoint để sử dụng trên nhiều máy tính.

## Cấu hình

File `mcp.json` chứa cấu hình để thêm vào `.cursor/mcp.json` hoặc `~/.cursor/mcp.json`:

```json
{
  "mcpServers": {
    "ppt": {
      "command": "uvx",
      "args": [
        "--from",
        "office-powerpoint-mcp-server",
        "ppt_mcp_server"
      ],
      "env": {}
    }
  }
}
```

## Sử dụng

1. Clone repository này:
   ```bash
   git clone https://github.com/NgoSon3868-Quas/PPT-MCP.git
   cd PPT-MCP
   ```

2. Copy nội dung từ `mcp.json` vào file cấu hình MCP của bạn:
   - Windows: `C:\Users\<username>\.cursor\mcp.json`
   - Mac/Linux: `~/.cursor/mcp.json`
   
   Hoặc merge vào file `mcpServers` hiện có của bạn.

3. Khởi động lại Cursor IDE

## Yêu cầu

- Python với `uv` hoặc `uvx` đã được cài đặt
- Package `office-powerpoint-mcp-server` có sẵn trên PyPI

## Cài đặt uv (nếu chưa có)

```bash
# Windows
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"

# Mac/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh
```

## Tính năng

MCP Server PowerPoint cung cấp các công cụ để:
- Tạo và chỉnh sửa PowerPoint presentations
- Quản lý slides
- Xử lý nội dung presentation

## Kiểm tra cấu hình

Sau khi thêm cấu hình và khởi động lại Cursor:
1. Vào Settings > Tools & MCP
2. Kiểm tra trong danh sách "Installed MCP Servers" có `ppt` với trạng thái "Ready"
