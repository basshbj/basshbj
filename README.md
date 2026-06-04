<style>
    :root {
      --bg: #0d1117;
      --terminal: #05080c;
      --border: #30363d;
      --text: #e6edf3;
      --muted: #8b949e;
      --green: #3fb950;
      --blue: #58a6ff;
      --red: #ff5f56;
      --yellow: #ffbd2e;
      --window-green: #27c93f;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      display: grid;
      place-items: center;
      background:
        radial-gradient(circle at top left, rgba(88, 166, 255, 0.15), transparent 35%),
        radial-gradient(circle at bottom right, rgba(63, 185, 80, 0.12), transparent 35%),
        var(--bg);
      font-family: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, "Liberation Mono", "Courier New", monospace;
      color: var(--text);
      padding: 32px;
    }

    .terminal {
      width: min(920px, 100%);
      background: linear-gradient(145deg, rgba(5, 8, 12, 0.98), rgba(13, 17, 23, 0.96));
      border: 1px solid var(--border);
      border-radius: 18px;
      box-shadow:
        0 24px 80px rgba(0, 0, 0, 0.45),
        inset 0 1px 0 rgba(255, 255, 255, 0.04);
      overflow: hidden;
    }

    .terminal-header {
      height: 56px;
      display: flex;
      align-items: center;
      gap: 10px;
      padding: 0 22px;
      border-bottom: 1px solid rgba(48, 54, 61, 0.65);
      background: rgba(255, 255, 255, 0.02);
    }

    .dot {
      width: 14px;
      height: 14px;
      border-radius: 50%;
      display: inline-block;
    }

    .red { background: var(--red); }
    .yellow { background: var(--yellow); }
    .green-dot { background: var(--window-green); }

    .terminal-body {
      padding: 38px 42px 42px;
      font-size: clamp(17px, 2.2vw, 25px);
      line-height: 1.65;
      letter-spacing: -0.02em;
      white-space: pre-wrap;
    }

    .prompt-user { color: var(--green); }
    .prompt-host { color: var(--blue); }
    .command { color: var(--text); }
    .muted { color: var(--muted); }
    .cursor {
      display: inline-block;
      width: 0.62em;
      height: 0.12em;
      background: var(--text);
      margin-left: 0.18em;
      vertical-align: -0.1em;
      animation: blink 1s steps(2, start) infinite;
    }

    a {
      color: var(--text);
      text-decoration: none;
    }

    a:hover {
      color: var(--blue);
      text-decoration: underline;
    }

    @keyframes blink {
      50% { opacity: 0; }
    }

    @media (max-width: 640px) {
      body { padding: 16px; }
      .terminal-body { padding: 28px 24px 30px; }
      .terminal-header { height: 48px; padding: 0 18px; }
      .dot { width: 12px; height: 12px; }
    }
  </style>

  <main class="terminal" aria-label="CLI style GitHub profile card">
    <div class="terminal-header" aria-hidden="true">
      <span class="dot red"></span>
      <span class="dot yellow"></span>
      <span class="dot green-dot"></span>
    </div>

    <section class="terminal-body"><span class="prompt-user">basshbj</span>@<span class="prompt-host">github</span>:~$ <span class="command">whoami</span>

Bassam Al-Mahamid (basshbj)

Senior Digital Cloud Solution Architect @ Microsoft
Apps &amp; AI

📍 Japan
🇪🇸 Spain

🗣 Spanish | English | Japanese

🔗 <a href="https://www.linkedin.com/in/baalmahamid" target="_blank" rel="noreferrer">linkedin.com/in/baalmahamid</a>

<span class="prompt-user">basshbj</span>@<span class="prompt-host">github</span>:~$ <span class="cursor"></span></section>
  </main>
