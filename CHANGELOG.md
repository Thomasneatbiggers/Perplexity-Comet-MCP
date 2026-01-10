# Changelog

All notable changes to this project will be documented in this file.

## [2.4.0] - 2026-01-10

### Added

- **Tab Management System** - New `comet_tabs` tool for viewing, switching, and closing browser tabs
- **Tab Registry** - Internal tracking of all external browsing tabs with purpose and domain
- **Last Tab Protection** - Prevents closing the only external tab which would crash Comet
- **Internal Tab Filtering** - Automatically filters chrome://, devtools://, and Perplexity UI tabs
- **Windows/WSL Support** - Full compatibility with Windows and WSL environments
- **PowerShell Fetch Workarounds** - Bypasses Node.js fetch issues on Windows
- **Direct CDP WebSocket Connection** - More reliable connection on Windows
- **Smart Completion Detection** - Response stability tracking instead of fixed timeouts
- **Auto-Reconnect** - Exponential backoff recovery (300ms-2s) from connection drops
- **Health Check Caching** - 2-second cache for efficient connection validation
- **Pre-Operation Checks** - Validates connection before every operation
- **Agentic Prompt Transformation** - Automatically triggers browser actions for URLs and action verbs
- **DOM-Based Submit** - More reliable prompt submission using DOM events
- **Full Response Extraction** - Captures complete responses after "X steps completed" marker
- **Tab Change Handling** - Maintains Perplexity connection during agentic browsing
- **Idle Timeout Detection** - 6-second idle detection for completion

### Changed

- Increased max reconnect attempts to 10
- Reduced poll interval to 1.5 seconds for better responsiveness
- Improved error recovery with Perplexity tab switching

### Fixed

- Connection drops during long agentic tasks
- Response truncation on complex queries
- Submit not working (text in box but not sent)
- Browser crash when closing last tab
- Incorrect tab counting due to internal Chrome tabs

## [1.0.0] - Original Release

- Initial fork from [hanzili/comet-mcp](https://github.com/hanzili/comet-mcp)
- Basic 6 tools: connect, ask, poll, stop, screenshot, mode
- macOS support
