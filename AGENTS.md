# AGENTS.md

A space to work with Blender to create a DIY Home Assistant kiosk.

## Blender MCP: WSL + Windows connection notes

This project uses Blender on Windows while agents run in WSL.  
That setup can look broken even when it is working.

### Connection issue resolution

- Blender UI said MCP was "Running on port 9876".
- Direct socket checks from WSL to `127.0.0.1:9876` failed (`Connection refused`).
- Windows showed Blender listening on `127.0.0.1:9876`.
- Despite that, `user-blender` MCP calls eventually worked.
