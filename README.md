<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Code Space - Online Code Editor</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <header class="header">
            <div class="logo"><h1>Code Space</h1></div>
            <nav class="nav">
                <button class="btn-save">Save</button>
                <button class="btn-run">Run Code</button>
                <button class="btn-share">Share</button>
            </nav>
        </header>

        <main class="main-content">
            <aside class="sidebar">
                <div class="file-explorer">
                    <h3>Files</h3>
                    <ul class="file-list">
                        <li class="file-item active"><span class="file-icon">📄</span><span>index.html</span></li>
                        <li class="file-item"><span class="file-icon">🎨</span><span>styles.css</span></li>
                        <li class="file-item"><span class="file-icon">⚙️</span><span>script.js</span></li>
                    </ul>
                </div>
                <div class="languages">
                    <h3>Languages</h3>
                    <select id="language-select" class="language-dropdown">
                        <option value="html">HTML</option>
                        <option value="css">CSS</option>
                        <option value="javascript">JavaScript</option>
                    </select>
                </div>
            </aside>

            <section class="editor-section">
                <div class="tab-bar">
                    <div class="tab active"><span>index.html</span><button class="tab-close">&times;</button></div>
                </div>
                <div class="editor-container">
                    <div class="line-numbers" id="line-numbers"></div>
                    <textarea id="code-editor" class="code-editor" placeholder="Write your code here..."></textarea>
                </div>
            </section>

            <section class="output-section">
                <div class="output-tabs">
                    <button class="output-tab active" data-tab="preview">Preview</button>
                    <button class="output-tab" data-tab="console">Console</button>
                </div>
                <div class="tab-content active" id="preview">
                    <iframe id="output-preview" class="output-preview"></iframe>
                </div>
                <div class="tab-content" id="console">
                    <div class="console-output" id="console-output"></div>
                </div>
            </section>
        </main>

        <footer class="status-bar">
            <span id="status">Ready</span>
            <span class="line-info">Line: <span id="line-count">1</span>, Column: <span id="column-count">1</span></span>
        </footer>
    </div>

    <script src="script.js"></script>
</body>
</html>
