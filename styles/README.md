## Description
A collection of custom styles that I made and found to my liking. You will see them around my website. Feel free to use them as well.

## Items
- [Terminal-Like Text Box](#Terminal-Like-Text-Box)

<br>

Terminal-Like Text Box:

<b>HTML:</b>
```html
<div class="terminal-box">
    <div class="terminal-header">
        <span class="terminal-dot red"></span>
        <span class="terminal-dot yellow"></span>
        <span class="terminal-dot green"></span>
    </div>
    <div class="terminal-body">
        <pre><code><span class="terminal-user">turbul3nce</span><span class="terminal-host">@office</span>$ curl -k https://magicgardens.htb:5000/v2/
{"errors":[{"code":"UNAUTHORIZED","message":"authentication required","detail":null}]}</code></pre>
    </div>
</div>
```
<b>CSS:</b>
```/
* Terminal-Like Style */
.terminal-box {
    background-color: #300a24; /* Ubuntu Terminal Light Purple */
    border-radius: 5px;
    margin: 15px 0;
    font-family: 'Courier New', monospace;
    color: #eeeeec; /* Ubuntu Terminal Text Color */
    position: relative;
    overflow: hidden; /* Prevents extra border effect */
    border: 2px solid #2c001e; /* Matches header for consistency */
}

/* Terminal Header (Fake MacOS-style buttons) */
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
    background-color: #1e1e1e; /* Dark Grey Terminal Background */
    padding: 10px 15px;
    overflow-x: auto; /* Enables horizontal scrolling */
    white-space: nowrap; /* Prevents line wrapping */
    border-bottom-left-radius: 5px;
    border-bottom-right-radius: 5px;
}

/* Code Styling */
pre, code {
    background: none;
    color: #eeeeec; /* Ubuntu Terminal Text Color */
    padding: 0;
    margin: 0;
    border: none;
    font-size: 0.95rem;
    display: block;
}```
