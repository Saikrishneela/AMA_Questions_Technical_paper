# AMA Questions and Answers

### What does the `chmod` command do in Linux?

`chmod` is used to change file permissions in Linux.

* Permissions: `r` (read), `w` (write), `x` (execute)

**Example:**

```bash
chmod 755 script.sh
```

Owner: read, write, execute; Group: read, execute; Others: read, execute.

### How do you list hidden files in a directory?

Use the `ls -a` command.

**Example:**

```bash
ls -a
```

Shows hidden files like `.gitignore`, `.env`.

### What’s the difference between `git merge` and `git rebase`?

* `git merge`: Combines branches, keeps history, creates a merge commit.
* `git rebase`: Moves commits on top of another branch, rewrites history (linear).

**Example:**

```bash
git checkout feature
git merge main
# or
 git rebase main
```

### How do you undo the last commit but keep the changes locally?

Use `git reset`.

**Example:**

```bash
git reset --soft HEAD~1   
git reset --mixed HEAD~1  
```

### What’s the difference between `<link>` and `<script>` tags?

* `<link>`: Links external resources (CSS, icons, etc.)
* `<script>`: Loads and executes JavaScript

**Example:**

```html
<link rel="stylesheet" href="styles.css">
<script src="app.js"></script>
```

### What are the differences between block-level and inline elements in HTML?

* Block-level: Full width, starts on a new line (`<div>`, `<p>`)
* Inline: Only as much width as needed, does not start on a new line (`<span>`, `<a>`)

**Example:**

```html
<div>This is block</div>
<span>This is inline</span>
```

### What is the difference between `em`, `rem`, and `px` units in CSS?

* `px`: Fixed size (absolute unit)
* `em`: Relative to parent’s font size
* `rem`: Relative to root (`html`) font size

**Example:**

```css
html { font-size: 16px; }
p { font-size: 2em; }   
h1 { font-size: 2rem; } 
```

### How does the CSS `z-index` property work?

`z-index` sets the stacking order of positioned elements (`relative`, `absolute`, `fixed`, `sticky`). Higher value appears on top.

**Example:**

```css
.box1 { position: absolute; z-index: 1; }
.box2 { position: absolute; z-index: 10; } 
```

### What is the difference between `null` and `undefined` in JavaScript?

* `undefined`: Variable declared but not assigned
* `null`: Explicitly set to "no value"

**Example:**

```javascript
let a;
console.log(a); 
let b = null;
console.log(b); 
```
