## Description
A collection of custom styles that I made and found to my liking. You will see them around my website. Feel free to use them as well.

## Items
- [Terminal-Like Text Box](#Terminal-Like-Text-Box)
- [Expansion Boxes](#Expansion-on-code-blocks)
- [Dark Mode](#Dark-Mode)

<br>

### Terminal-Like Text Box:

<img src=../assets/terminal-like-box.PNG>

<b>HTML:</b>
```html
<div class="terminal-box">
    <div class="terminal-header">
        <span class="terminal-dot red"></span>
        <span class="terminal-dot yellow"></span>
        <span class="terminal-dot green"></span>
    </div>
    <div class="terminal-body">
        <pre><code><span class="terminal-user">turbul3nce</span><span class="terminal-host">@office</span>$ curl -k https://www.test.com
{"errors":[{"code":"UNAUTHORIZED","message":"authentication required","detail":null}]}</code></pre>
    </div>
</div>
```
<b>CSS:</b>
```/
/* Ubuntu Terminal Style */
.terminal-box {
    background-color:  #1e1e1e; /* Light Grey */
    border-radius: 5px;
    margin: 15px 0;
    font-family: 'Courier New', monospace;
    color: #eeeeec; /* Terminal Text Color */
    position: relative;
    overflow: hidden; /* Prevents extra border effect */
    border: 2px solid #2c001e; /* Matches header for consistency */
    border-width: 2px 1.4px 1.4px 1.4px; /* Top, Right, Bottom, Left */
}

/* Terminal Header */
.terminal-header {
    display: flex;
    gap: 5px;
    padding: 5px 10px;
    background: #2c001e; /* Slightly Darker Ubuntu Purple */
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
}

/* Terminal Buttons (MacOS-like Close, Minimize, Maximize) */
.terminal-dot {
    width: 10px;
    height: 10px;
    border-radius: 50%;
    display: inline-block;
}

.red { background: #ff5f56; }
.yellow { background: #ffbd2e; }
.green { background: #27c93f; }

/* Terminal Body */
.terminal-body {
    background-color: #2a2a2a !important; /* Force same grey */
    padding: 8px 11px;
    overflow-x: auto;
    white-space: nowrap;
    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
}
    
/* User & Host Colors */
.terminal-user {
    color: #00a3ff; /* Blue for 'turbul3nce' */
}

.terminal-host {
    color: #27c93f; /* Green for '@office' */
}
```

### Dark Mode

- Building an implementation of "dark mode" for the Mediumish Jekyll theme. Similar to Minima's themes.
- Will open a pull request on the official [GitHub](https://github.com/wowthemesnet/mediumish-theme-jekyll) and post steps here when complete.

### Expansion on Code Blocks

<b>HTML:</b>

```html
<div class="collapsible-code">
    <div class="terminal-box">
        <div class="terminal-header">
            <span class="terminal-dot red"></span>
            <span class="terminal-dot yellow"></span>
            <span class="terminal-dot green"></span>
        </div>
        <div class="terminal-body">
            <pre><span class="terminal-user">rosehacks</span><span class="terminal-host">@pwny</span>$ cat predictable.txt
This was a "hard" challenge from a HTB CTF...
</pre>
        </div>
    </div>
</div>
```

<b>Javascript:</b>

```javascript
document.addEventListener("DOMContentLoaded", function () {
    document.querySelectorAll(".collapsible-code").forEach(function (block) {
        // Check if content height exceeds max-height
        if (block.scrollHeight > block.clientHeight) {
            let button = document.createElement("button");
            button.className = "expand-button";
            button.innerText = "Expand";
            block.appendChild(button);

            button.addEventListener("click", function () {
                if (block.classList.contains("expanded")) {
                    block.classList.remove("expanded");
                    button.innerText = "Expand";
                } else {
                    block.classList.add("expanded");
                    button.innerText = "Collapse";
                }
            });
        }
    });
});
```

<b>CSS:</b>

```css
/* Base styles for code blocks */
.collapsible-code {
    position: relative;
    max-height: 300px; /* Set the max height before collapsing */
    overflow: hidden;
    transition: max-height 0.3s ease-in-out;
}

/* Expanded state (when user clicks 'Expand') */
.collapsible-code.expanded {
    max-height: none; /* Remove height restriction */
}

/* Expand/Collapse Button */
.expand-button {
    position: absolute;
    bottom: 5px;
    right: 5px;
    background: #00a3ff; /* Nice blue color */
    color: white;
    border: none;
    padding: 5px 10px;
    border-radius: 4px;
    font-size: 12px;
    cursor: pointer;
    transition: background 0.2s;
}

.expand-button:hover {
    background: #0086d1; /* Slightly darker on hover */
}

/* Add a gradient fade effect at the bottom when collapsed */
.collapsible-code:not(.expanded)::after {
    content: "";
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 40px;
    background: linear-gradient(to bottom, rgba(42, 42, 42, 0) 0%, #2a2a2a 100%);
}
```
