
# Chrome Extension CLI

Your go-to tool for creating Chrome Extensions. 🚀

## Quick Start
Get up and running quickly with the Chrome Extension CLI:




## Installation

Install my-project with npm

```bash
npm install -g chrome-extension-cli
chrome-extension-cli my-extension
cd my-extension
npm run watch
```



    
## Load Your Extension in Chrome

- Navigate to **chrome://extensions** in your browser.
- Enable **Developer mode**.
- Click **Load unpacked extension**.
- Choose the **my-extension/build** folder.

When ready for the Chrome Web Store, run ```npm run build``` to create a minified bundle, and ```npm run pack``` to zip it for publishing.



## Usage

```bash
chrome-extension-cli <project-name>
```

This creates a new directory with the following structure:

```
my-extension
├── README.md
├── node_modules
├── package.json
├── .gitignore
├── config/                   // Webpack config files
├── public/
│   ├── icons/                // Extension icons
│   ├── *.html                // HTML files for the extension
│   └── manifest.json
└── src/
    ├── *.css                 // CSS files
    └── *.js                  // JavaScript files

```



    
## Commands

- ```npm run watch```: Start development mode, auto-rebuilding on changes.
- ```npm run build```: Create a production-ready build.
- ```npm run pack```: Zip the build for easy distribution.
- ```npm run repack```: Rebuild and zip in one step.
- ```npm run format```: Format all code files.

## Supported Extension Types

- **Popup:** Add features to the active tab.
![template-popup](https://github.com/user-attachments/assets/511825b2-27c2-41c3-81cf-aa5067525e71)
- **Override Page:** Customize pages like New Tab, Bookmarks, or History.
  ![template-page](https://github.com/user-attachments/assets/681523a9-9ad6-4125-a49c-831dd90d8b8b)
- **DevTools:** Enhance Chrome Developer Tools.
  ![template-panel](https://github.com/user-attachments/assets/0cbf8bf9-3154-4af2-99c9-f5e7ad92e49e)
- **Side Panel:** Add a panel to the browser’s side area.
  ![template-side-panel](https://github.com/user-attachments/assets/8e16e8ca-e5cc-4e20-9080-ae42934e0938)


## CLI Options

Customize your project with options:

- **Override Pages:**
    ```
    chrome-extension-cli my-extension --override-page
    chrome-extension-cli my-extension --override-page=bookmarks
    chrome-extension-cli my-extension --override-page=history
    ```

- **DevTools Panel:**
    ```
    chrome-extension-cli my-extension --devtools
    ```

- **Side Panel:**
    ```
    chrome-extension-cli my-extension --side-panel
    ```

- **Language Support:**
    ```
    chrome-extension-cli my-extension --language=javascript
    chrome-extension-cli my-extension --language=typescript
    ```

