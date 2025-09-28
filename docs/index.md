<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Cyber Security Notes</title>
  <meta name="description" content="Landing page for Red Team and Blue Team notes" />
  <style>
    :root {
      --bg: #0fb9b1; /* teal/cyan */
      --bg-accent: #00c2c7; /* slightly brighter cyan */
      --text: #ffffff;
      --card-bg: rgba(255, 255, 255, 0.14); /* glass base */
      --card-border: rgba(255, 255, 255, 0.35);
      --card-shadow: rgba(0, 0, 0, 0.25);
      --gloss-start: rgba(255, 255, 255, 0.65);
      --gloss-end: rgba(255, 255, 255, 0.05);
    }

    /* Page baseline */
    html, body {
      height: 100%;
    }
    body {
      margin: 0;
      color: var(--text);
      font-family: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial, "Apple Color Emoji", "Segoe UI Emoji";
      background: linear-gradient(135deg, var(--bg), var(--bg-accent));
      display: grid;
      place-items: center;
    }

    /* Wrapper to center content */
    .container {
      width: min(1100px, 92vw);
      display: grid;
      place-items: center;
      gap: clamp(16px, 3vw, 32px);
      padding: clamp(16px, 4vw, 48px);
    }

    /* Button grid */
    .grid {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: clamp(16px, 5vw, 40px);
      align-items: center;
      justify-items: center;
    }

    /* Glassy square buttons */
    .tile {
      --size: clamp(140px, 36vw, 220px);
      position: relative;
      width: var(--size);
      height: var(--size);
      border-radius: 22px; /* rounded corners on a square */
      background: linear-gradient(145deg, rgba(255,255,255,0.18), rgba(255,255,255,0.10));
      border: 1px solid var(--card-border);
      box-shadow:
        0 12px 30px var(--card-shadow),
        inset 0 0 0 0.5px rgba(255,255,255,0.25);
      backdrop-filter: blur(8px) saturate(135%);
      -webkit-backdrop-filter: blur(8px) saturate(135%);
      display: grid;
      place-items: center;
      text-decoration: none;
      color: var(--text);
      font-weight: 700;
      letter-spacing: 0.4px;
      text-transform: uppercase;
      transition: transform 160ms ease, box-shadow 160ms ease, background 160ms ease;
      outline: none;
      isolation: isolate; /* ensure pseudo-element sits on top */
    }

    /* iOS-style gloss highlight */
    .tile::before {
      content: "";
      position: absolute;
      inset: 0;
      border-radius: inherit;
      background: linear-gradient( to bottom, var(--gloss-start) 0%, var(--gloss-end) 44% );
      mix-blend-mode: screen;
      opacity: 0.55;
      pointer-events: none;
    }

    /* subtle inner highlight ring */
    .tile::after {
      content: "";
      position: absolute;
      inset: 0;
      border-radius: inherit;
      box-shadow: inset 0 2px 12px rgba(255,255,255,0.18), inset 0 -6px 18px rgba(0,0,0,0.18);
      pointer-events: none;
    }

    /* Hover / focus interactions */
    .tile:hover, .tile:focus-visible {
      transform: translateY(-4px);
      box-shadow:
        0 18px 40px rgba(0,0,0,0.35),
        inset 0 0 0 0.5px rgba(255,255,255,0.35);
      background: linear-gradient(145deg, rgba(255,255,255,0.22), rgba(255,255,255,0.12));
    }

    .label {
      font-size: clamp(18px, 3.6vw, 26px);
      text-shadow: 0 1px 2px rgba(0,0,0,0.35);
    }

    /* Optional team hues for subtle edge glow */
    .blue {
      box-shadow:
        0 12px 30px var(--card-shadow),
        0 0 0 1px rgba(77, 184, 255, 0.35) inset,
        0 12px 50px rgba(60,130,255,0.20);
    }
    .red {
      box-shadow:
        0 12px 30px var(--card-shadow),
        0 0 0 1px rgba(255, 120, 120, 0.35) inset,
        0 12px 50px rgba(255,60,60,0.20);
    }

    /* Accessibility: focus ring */
    .tile:focus-visible {
      outline: 3px solid rgba(255,255,255,0.7);
      outline-offset: 2px;
    }

    /* Small screens: stack vertically */
    @media (max-width: 560px) {
      .grid { grid-template-columns: 1fr; }
    }
  </style>
</head>
<body>
  <main class="container" role="main">
    <nav class="grid" aria-label="Team Selection">
      <!-- Blue Team (left) -->
      <a class="tile blue" href="./blue/" aria-label="Blue Team notes">
        <span class="label">Blue Team</span>
      </a>

      <!-- Red Team (right) -->
      <a class="tile red" href="./red/" aria-label="Red Team notes">
        <span class="label">Red Team</span>
      </a>
    </nav>
  </main>
</body>
</html>

