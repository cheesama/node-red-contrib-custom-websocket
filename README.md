# node-red-contrib-custom-websocket
Custom websocket node implementation for node-red

## Feature
- Accept additional query parameters in websocket url
    - Query parameters are contianed in "_session.params" object when message arrived(it can be set in handleUpgrade time)
---
- Add custom headers when creating websocket client
    - User can add headers in custom-websocket-client editing UI
    