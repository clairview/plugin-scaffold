## ClairView Plugin Scaffold

This project contains shared typescript types that ClairView plugin
authors can use.

```bash
# if using yarn
yarn add --dev @clairview/plugin-scaffold

# if using npm
npm install --save-dev @clairview/plugin-scaffold
``` 

Then in your plugins:

```typescript
import { PluginEvent, PluginInput, PluginMeta } from "@clairview/plugin-scaffold";

export function processEvent(event: PluginEvent, meta: PluginMeta<PluginInput>) {
    if (event.properties) {
        event.properties['hello'] = 'world'
    }
    return event
}
```