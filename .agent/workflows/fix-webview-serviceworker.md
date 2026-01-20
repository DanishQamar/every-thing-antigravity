---
description: Fix "Error loading webview: Error: Could not register service worker" in VS Code
---

# Fix Webview Service Worker Error

This error (`InvalidStateError: Failed to register a ServiceWorker`) typically occurs in VS Code when the webview's service worker process gets into a bad state or the cache becomes corrupted.

## Workflow Steps

1. **Close VS Code Completely**
   Ensure all VS Code windows are closed.

2. **Kill Lingering Processes**
   Run the following command to ensure all VS Code processes are terminated:
   ```bash
   pkill -f code || echo "No running processes found"
   ```
   // turbo

3. **Clear VS Code Cache (Linux)**
   Clear the GPU and Service Worker caches.
   > [!WARNING]
   > This will clear your editor's cached data, but settings and extensions will be preserved.
   ```bash
   rm -rf ~/.config/Code/Cache
   rm -rf ~/.config/Code/CachedData
   rm -rf ~/.config/Code/GPUCache
   rm -rf ~/.config/Code/Service\ Worker
   ```
   // turbo

4. **Restart VS Code**
   Launch VS Code again:
   ```bash
   code .
   ```

## Troubleshooting

If the issue persists:
- **Disable Extensions**: Try running with `code --disable-extensions` to see if an extension is causing the conflict.
- **Update VS Code**: Ensure you are on the latest version.
