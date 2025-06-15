
To keep your Node.js system fully asynchronous, the goal is to never block the event loop — that means:
> Avoid anything that waits, blocks, or freezes execution, and instead use async I/O, worker threads, or queues.

### ✅ 1. Use Async I/O for Everything
#### 🔧 File System

* ❌ Avoid: fs.readFileSync, `fs.writeFileSync`
* ✅ Use: fs.promises.readFile, await fs.promises.writeFile


#### 🔧 HTTP/Network Requests
* Use libraries that return `Promises` (e.g., `axios`, `node-fetch`)
