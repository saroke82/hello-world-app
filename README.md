// Project: hello-world-app (React 18 using Vite)

// ------------------- // File: index.html // -------------------

<!DOCTYPE html><html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Hello World App</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>// ------------------- // File: src/main.jsx // ------------------- import React from 'react' import ReactDOM from 'react-dom/client' import App from './App'

ReactDOM.createRoot(document.getElementById('root')).render( <React.StrictMode> <App /> </React.StrictMode> )

// ------------------- // File: src/App.jsx // ------------------- import React from 'react';

function App() { return ( <div> <h1>Hello World</h1> </div> ); }

export default App;

// ------------------- // File: package.json (partial) // ------------------- { "name": "hello-world-app", "version": "0.0.0", "private": true, "scripts": { "dev": "vite", "build": "vite build", "preview": "vite preview" }, "dependencies": { "react": "^18.0.0", "react-dom": "^18.0.0" }, "devDependencies": { "vite": "^5.0.0", "@vitejs/plugin-react": "^4.0.0" } }

// ------------------- // File: vite.config.js // ------------------- import { defineConfig } from 'vite' import react from '@vitejs/plugin-react'

export default defineConfig({ plugins: [react()], })
