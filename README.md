# TCP File Server 🌐

## Overview 🎯
A robust TCP server implementation that handles file requests via HTTP/1.1 protocol. This server enables clients to retrieve files from a specified directory with support for persistent connections and comprehensive error handling.

## Key Features ⭐
- **HTTP/1.1 File Retrieval** 📂
  - GET request support
  - Binary & text file handling
  - Path flexibility (relative/absolute)
  
- **Smart Connection Management** 🔌
  - Keep-alive support
  - Auto-timeout (1 second) ⏱️
  - Connection state tracking

- **Error Handling** 🚨
  - 404 Not Found responses
  - 301 Redirects
  - Timeout management

## Quick Start 🚀

### Server Setup 💻
```bash
python3 tcp_server.py [PORT]
```

### Client Usage 🖥️
```bash
python3 tcp_client.py [SERVER_IP] [PORT]
```

## Example Interactions 🔄

### Successful Request 📧
```http
# Request
GET / HTTP/1.1
Connection: close

# Response
HTTP/1.1 200 OK
Connection: close
Content-Length: 11

hello world
```

### Error Cases ❌
- File Not Found: Returns 404 error
- Redirect Needed: Returns 301 with location header

## Technical Features 🛠️

### Connection Handling 🔌
- **Persistent Connections**
  - Keep-alive support
  - Configurable timeouts
  - Auto-cleanup

### File Operations 📁
- Text file serving
- Binary file support (.jpg, .ico)
- Directory traversal protection

### Network Analysis 🔍
- Wireshark compatibility
- Connection tracking
- Packet inspection

## Requirements 📋
- Python 3.x
- Basic networking tools
- Wireshark (for debugging)

## Testing 🧪
1. Start server
2. Run client requests
3. Monitor Wireshark output
4. Verify file transfers

## Best Practices 💡
- Keep connections short
- Handle binary files properly
- Monitor timeouts
- Validate paths

## Contributors 👥
- Development Team
- Network Specialists
- QA Engineers

Need help? Open an issue! 🤝

---
Made with ❤️ by the TCP Server Team
