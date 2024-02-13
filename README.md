![Hello Godot](/hello-godot.png)

# hello-godot
[Godot](https://godotengine.org/) is a cross-platform, free and open-source game engine released under the permissive MIT license.

## Setting Up GitHub Pages
Note: This only needs to be done once.
1. Go to the "Settings" tab of the repo
1. Select "Pages" from left-nav
1. Select `main` branch and `/docs` directory, then select "Save"
    - A GitHub Action will deploy your website
1. On the main page of the GitHub repo, click the gear icon next to "About"
1. Select "Use your GitHub Pages website", then select "Save changes"

## Building for Web Using Godot GUI
1. Select "Project" > "Export..."
    - If you see errors, click the link for "Manage Export Templates" and then click "Download and Install"
1. Select the preset "Web (Runnable)"
1. (One Time Setup) Download [coi.js](https://github.com/gzuidhof/coi-serviceworker/raw/master/coi-serviceworker.js) and add it to the `/docs` directory
1. (One Time Setup) Enter "Head Include" `<script src="coi-serviceworker.js"></script>`
1. Select "Export Project..."
1. Select the "docs" folder
    - The GitHub Pages config points to the `main` branch and `/docs` directory
1. Enter `index.html`
1. Select "Save"
1. Commit the code to trigger a GitHub Pages deployment (above), or run the code locally (below)

## Running the web server locally
1. Open the root folder using [VS Code](https://code.visualstudio.com/)
    - If you use GitHub Desktop, select the "Open in Visual Studio" button
1. Open the [integrated terminal](https://code.visualstudio.com/docs/editor/integrated-terminal)
1. Enter `npx local-web-server --https --cors.embedder-policy "require-corp" --cors.opener-policy "same-origin" --directory "./docs"`
    1. Enter `y` if prompted
1. In your browser navigate to [https://127.0.0.1:8000/](https://127.0.0.1:8000/)
1. In terminal press [Ctrl]+[C] to stop the web process
    1. Enter `y` if prompted
