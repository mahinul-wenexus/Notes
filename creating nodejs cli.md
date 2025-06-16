# Create Node.js CLI which will be able to run by Node.js
The line
```javascript
#!/usr/bin/env node
```
is called a `shebang` (or `hashbang`) line.

### ✅ What It Means in Node.js
This line tells the operating system:

> "Use the `node` interpreter found in the current environment (`/usr/bin/env`) to run this script."
So when you run the file directly (like `./my-script.js`), the OS uses Node.js to execute it.

### 🧠 Breakdown
* `#!` — Special marker that tells Unix-like systems to use the given interpreter
* `/usr/bin/env` — Finds the correct path to the `node` binary in your `$PATH`
* `node` — The interpreter (Node.js) to run the script

It ensures the script runs with whichever Node.js version is active in your current environment (e.g., via nvm, asdf, or system-installed).

## 🛠️ How to Use It
1. Add the line to the top of your .js file:
```javascript
#!/usr/bin/env node

console.log('Hello from Node.js script!');
```

2. Make the file executable:
```bash
chmod +x my-script.js
```

3. Run it like a normal shell command:
```bash
./my-script.js
```


<br>
<br>

### ✅ What Does `chmod` Do?
chmod stands for `change mode`, and it’s a Unix/Linux command used to change file or directory permissions.


#### 🧠 In Simple Terms:
chmod controls who can read, write, or execute a file.

For example:
```bash
chmod +x my-script.js
```

> This makes my-script.js executable, so you can run it like this:

```bash
./my-script.js
```

##### Without chmod you have to do like this
```bash
node ./my-script.js
```
Without +x, you'd get a "Permission denied" error when trying to execute it.

#### 🔐 Permission Basics
Every file has three levels of permissions:
| Entity         | Symbol |
| -------------- | ------ |
| Owner          | `u`    |
| Group          | `g`    |
| Others (world) | `o`    |


Each can have three types of permissions:
| Permission | Symbol | Meaning                                       |
| ---------- | ------ | --------------------------------------------- |
| Read       | `r`    | Can view the file                             |
| Write      | `w`    | Can modify the file                           |
| Execute    | `x`    | Can run the file (if it's a script or binary) |



