# fix autorefresh with custom port
```
# src/vite.config.js
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

// https://vite.dev/config/
export default defineConfig({
  plugins: [react()],
  server : {
    port: 3000,
    host: '0.0.0.0',
    watch: {
      usePolling: true,
    },
  }
})
```
