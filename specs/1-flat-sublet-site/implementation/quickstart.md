# Quickstart Guide

## Prerequisites
1. Node.js (for Tailwind CSS build process)
2. Basic text editor
3. Image optimization tools (e.g., ImageOptim, Squoosh)

## Setup Steps

1. **Initialize project**
   ```bash
   npm init -y
   npm install -D tailwindcss@latest
   ```

2. **Configure Tailwind CSS**
   ```bash
   npx tailwindcss init
   ```

3. **Create build structure**
   ```
   mkdir css img
   touch index.html
   ```

4. **Configure Tailwind CSS (tailwind.config.js)**
   ```javascript
   module.exports = {
     content: ['./*.html'],
     theme: {
       extend: {
         // Custom theme extensions will go here
       },
     },
     plugins: [],
   }
   ```

5. **Create CSS source file (css/styles.css)**
   ```css
   @tailwind base;
   @tailwind components;
   @tailwind utilities;
   ```

6. **Add build script to package.json**
   ```json
   {
     "scripts": {
       "build": "tailwindcss -i ./css/styles.css -o ./css/output.css --watch"
     }
   }
   ```

7. **Optimize images**
   - Resize images to appropriate dimensions
   - Convert to WebP format
   - Create responsive versions
   - Place in img/ directory

8. **Development**
   ```bash
   npm run build
   ```

9. **Testing**
   - Use Live Server VS Code extension or similar
   - Test across different devices and browsers
   - Validate HTML and CSS

## Deployment
1. Build production CSS:
   ```bash
   npx tailwindcss -i ./css/styles.css -o ./css/output.css --minify
   ```
2. Deploy static files to hosting service

## Project Structure
```
/
├── index.html          # Main HTML file
├── css/
│   ├── styles.css      # Tailwind source
│   └── output.css      # Compiled CSS
├── img/               # Optimized images
│   ├── 1.jpg
│   ├── ...
│   └── plan.png
├── package.json
└── tailwind.config.js
```