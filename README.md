# NOAA Free MCP Server - Community Hub

Welcome to the community repository for the **NOAA Free MCP Server**! This is your place to report issues, suggest features, ask questions, and connect with other users of this Model Context Protocol server.

## 📦 About the Package

A Model Context Protocol (MCP) server that provides access to NOAA precipitation data through an embedded Go binary. This server allows AI assistants to retrieve and analyze daily and monthly precipitation data from the NOAA Climate Prediction Center.

## ✨ Features

- 🌧️ **Daily precipitation data** with detailed statistics (mean, median, mode, quartiles, outliers)
- 📊 **Monthly precipitation totals** for any grid location
- 🗺️ **13,626 valid grids** across CONUS (Continental United States) at 0.25° resolution
- 📈 **Historical data** from 1947 to present
- ⚡ **High performance** with embedded Go binary for data processing
- 🔄 **Real-time and historical data** support
- 🖥️ **Cross-platform support** (Windows, macOS, Linux)

## 🏠 What This Repository Is For

This is a **community-only repository** for:

- 🐛 **Bug Reports** - Found an issue? Let us know!
- 💡 **Feature Requests** - Have ideas for improvements?
- ❓ **Questions** - Need help using the MCP server?
- 💬 **Discussions** - Connect with other users
- 📚 **Documentation** - Find usage examples and guides
- 😍 **Help me out** - If the right person comes along that wants to help I'm open to a collab

## ⚠️ Important Note

**This repository does NOT contain the source code.** The actual development happens in a private repository. This community hub is specifically designed to:

- Collect your feedback and suggestions
- Provide documentation and examples
- Foster discussion among users
- Track issues and feature requests

## 🚀 Installation & Setup

### Global Installation (Recommended)

```bash
npm install -g @bryance/noaa-free-mcp
```

### Local Installation

```bash
npm install @bryance/noaa-free-mcp
```

### Configuration

Add the server to your MCP client configuration:

#### Claude Desktop

Add to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "noaa-free": {
      "command": "noaa-free-mcp"
    }
  }
}
```

#### Other MCP Clients

Use the command `noaa-free-mcp` or the full path to the installed binary.

**Note:** After installing the package `@bryance/noaa-free-mcp`, the executable is available as `noaa-free-mcp` (npm automatically strips the scope from executable names).

## 🛠️ Usage

The server provides two main tools (More coming soon):

### 1. Get Daily Rain Data

Retrieves daily precipitation measurements for a specific grid, year, and month.

**Parameters:**

- `grid_id` (6196-34941): NOAA grid identifier for valid CONUS grids
- `year` (1947-present): Year for data request
- `month` (1-12): Month for data request

**Returns:**

- Daily measurements for each day in the month
- Statistical analysis

### 2. Get Monthly Rain Total

Retrieves total precipitation for a specific grid, year, and month.

**Parameters:**

- `grid_id` (6196-34941): NOAA grid identifier for valid CONUS grids
- `year` (1947-present): Year for data request
- `month` (1-12): Month for data request

**Returns:**

- Total precipitation for the month
- Grid location information

## 🤝 How to Contribute

We welcome your input! Here's how you can help make this MCP server better:

### Reporting Bugs

Found something broken? [Open an issue](../../issues/new) with:

- Clear description of the problem
- Steps to reproduce
- Your environment details (OS, Node version, etc.)
- Any error messages

### Requesting Features

Have an idea for improvement? [Start a discussion](https://github.com/BryanCE/noaa-free-community/discussions/new?category=ideas) describe:

- What you'd like to see added
- Why it would be useful
- How you envision it working

### Asking Questions

Not sure how something works? Post here for help [Discussions](https://github.com/BryanCE/noaa-free-community/discussions/2) section or [start a new discussion](https://github.com/BryanCE/noaa-free-community/discussions/new).

Not sure how something works? Check the [Discussions](../../discussions) section or open a new discussion thread.

## 📊 Package Stats

- **Weekly Downloads:** 161+ (and growing!)
- **Version:** 1.0.6
- **Grid Coverage:** 13,626 locations across CONUS
- **Historical Range:** 1947 to present
- **Resolution:** 0.25°

## 🙏 Thank You

Thanks to everyone who's downloaded and used this MCP server. Your usage and feedback help make it better for the entire community!

---

_This project provides access to NOAA Climate Prediction Center data. Please respect NOAA's data usage policies._
