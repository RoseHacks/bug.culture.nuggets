## Description
A collection of custom styles that I made and found to my liking. You will see them around my website. Feel free to use them as well.

## Items
- [Terminal-Like Text Box](#Terminal-Like-Text-Box)
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
