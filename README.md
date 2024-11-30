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
