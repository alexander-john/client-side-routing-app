# Client-side routing
### How This Example Works:

Routes:

- A `routes` object defines which content to display for specific paths (`/`, `/about`, `/contact`).

Link Handling:

- Clicking a link calls the `route()` function via the `onclick` event:
    - Prevents the page reload with `event.preventDefault()`.
    - Updates the browser’s URL with `history.pushState()`.

Dynamic Content:

- The `render()` function updates the `#app` element with the corresponding content from the `routes` object.

Browser History:

- The `onpopstate` event handles browser back/forward navigation by re-rendering the correct content.

404 Handling:

- If the path doesn’t exist in the `routes` object, it displays a "404 - Page Not Found" message.

### Setting Up a Local Server
- Using Python (Built-In Web Server)
```bash
# Python 3.x
python -m http.server 8000
```
- Navigate to `http://localhost:8000` to view your app.

### Example Issue Without a Server

File System Behavior:

- You load `index.html` using `file:///path/to/index.html`.
- Your app works on the home route (`/`), but navigating to `/about` causes the browser to look for a file at `file:///about`, resulting in a "File not found" error.

Server Behavior:
- You run a local server and access the app at `http://localhost:8000`.
- Navigating to `/about` keeps you within the app, and your client-side router handles the route.
