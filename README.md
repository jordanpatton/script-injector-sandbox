# Script Injection Sandbox

### Installation (requires [node](https://nodejs.org))

```bash
git clone https://github.com/jordanpatton/script-injection-sandbox.git
cd script-injection-sandbox
npm install
node app.js
```

### Usage

1. Go to [localhost:3000](http://localhost:3000).
2. Open your browser console and inspect your network traffic.
3. Click the `Inject` button.

### Expected Results

The following things will happen _very_ quickly when you click `Inject`:

1. Browser adds a `script` node to the DOM.
2. Browser requests a file matching the script node's `src`.
3. Server generates the script dynamically.
4. Browser loads the generated script.
5. Browser parses the generated script and adds the results to memory.
6. Browser inserts the result in the lower `textarea`.
7. Browser removes the `script` node from the DOM.

It's likely this will happen so quickly that you won't even see the DOM transform.

### Questions

**Q:** Why would I ever use this?

**A:** Script injection provides a viable alternative to cross-origin resource sharing.
