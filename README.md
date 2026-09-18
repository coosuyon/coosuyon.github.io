# @xmoonvii — Profile Website

A single-file, static HTML profile website. No frameworks, no build step — just open the file in a browser or drop it on any static host.

## How to use

1. Copy the HTML below into a file named `index.html`.
2. Open it in any browser, or upload it to any static host (GitHub Pages, Netlify, Carrd, etc.).

## Full source (`index.html`)

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>@xmoonvii — archive</title>
  <style>
    :root {
      --bg: #1a1a1a;
      --text: #cccccc;
      --border: #4d4d4d;
      --white: #ffffff;
      --muted: rgba(204, 204, 204, 0.8);
    }
    * { box-sizing: border-box; margin: 0; padding: 0; }
    body {
      background: var(--bg);
      color: var(--text);
      font-family: ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, sans-serif;
      line-height: 1.6;
      -webkit-font-smoothing: antialiased;
    }
    .wrap { max-width: 1000px; margin: 0 auto; padding: 24px 16px; }
    @media (min-width: 640px) { .wrap { padding: 40px 16px; } }

    .archive-tag {
      display: flex; align-items: center; gap: 8px;
      font-size: 11px; letter-spacing: 0.18em; text-transform: uppercase;
      color: var(--muted); margin-bottom: 16px;
    }
    .archive-tag svg { width: 14px; height: 14px; }

    header.bar {
      display: flex; flex-direction: column; gap: 12px;
      border: 1px solid var(--border); border-radius: 999px;
      padding: 12px 20px; margin-bottom: 24px;
    }
    @media (min-width: 640px) {
      header.bar { flex-direction: row; align-items: center; justify-content: space-between; }
    }
    header.bar .handle { color: var(--white); font-weight: 500; letter-spacing: 0.02em; }
    header.bar a.url {
      display: inline-flex; align-items: center; gap: 8px;
      border: 1px solid var(--border); border-radius: 999px;
      padding: 6px 16px; font-size: 12px; color: var(--text);
      text-decoration: none; transition: border-color 0.2s, color 0.2s;
    }
    header.bar a.url:hover { border-color: var(--white); color: var(--white); }
    header.bar a.url svg { width: 13px; height: 13px; }

    .grid { display: grid; grid-template-columns: 1fr; gap: 24px; }
    @media (min-width: 768px) { .grid { grid-template-columns: 240px 1fr; gap: 24px; } }

    aside { display: flex; flex-direction: column; align-items: center; text-align: center; }
    .avatar {
      width: 100%; max-width: 220px; aspect-ratio: 1 / 1;
      overflow: hidden; border: 1px solid var(--border); border-radius: 2px;
    }
    .avatar img { width: 100%; height: 100%; object-fit: cover; filter: grayscale(1); display: block; }
    .info { margin-top: 20px; font-size: 14px; }
    .info p { margin-bottom: 2px; }
    .info .name { color: var(--white); }
    .info .dim { color: var(--muted); }
    hr.sep { width: 100%; border: none; border-top: 1px solid var(--border); margin: 20px 0; }
    .links h2, .box h3 {
      color: var(--white); font-size: 13px; letter-spacing: 0.18em;
      text-transform: uppercase; margin-bottom: 12px; text-align: left;
    }
    .links ul { list-style: none; text-align: left; }
    .links li { margin-bottom: 8px; }
    .links a {
      display: flex; align-items: center; gap: 8px;
      font-size: 14px; color: var(--text); text-decoration: none;
      transition: color 0.2s;
    }
    .links a:hover { color: var(--white); }
    .links a svg { width: 15px; height: 15px; color: var(--muted); }
    .anime-list {
      margin-top: 16px; display: flex; align-items: center; gap: 8px;
      border: 1px solid var(--border); border-radius: 2px;
      padding: 8px 12px; font-size: 14px; color: var(--text);
      text-decoration: none; transition: border-color 0.2s, color 0.2s;
    }
    .anime-list:hover { border-color: var(--white); color: var(--white); }
    .anime-list svg { width: 15px; height: 15px; color: var(--muted); }

    main { display: flex; flex-direction: column; gap: 16px; }
    .box { border: 1px solid var(--border); border-radius: 2px; padding: 16px; }
    .box p { font-size: 14px; }
    .band { width: 100%; overflow: hidden; border: 1px solid var(--border); border-radius: 2px; }
    .band img { width: 100%; height: 160px; object-fit: cover; display: block; }
    .closing { font-size: 14px; text-align: center; padding: 0 8px; }
  </style>
</head>
<body>
  <div class="wrap">
    <div class="archive-tag">
      <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M4 4h4l2 2h8a2 2 0 0 1 2 2v9a2 2 0 0 1-2 2H4a2 2 0 0 1-2-2V6a2 2 0 0 1 2-2z"/></svg>
      <span>archive</span>
    </div>

    <header class="bar">
      <span class="handle">@xmoonvii</span>
      <a class="url" href="https://www.intrludemoon.carrd.co/" target="_blank" rel="noreferrer">
        <svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"/><path d="M2 12h20M12 2a15.3 15.3 0 0 1 4 10 15.3 15.3 0 0 1-4 10 15.3 15.3 0 0 1-4-10 15.3 15.3 0 0 1 4-10z"/></svg>
        https://www.intrludemoon.carrd.co/
      </a>
    </header>

    <div class="grid">
      <aside>
        <div class="avatar">
          <img src="https://media.base44.com/images/public/6aad875a3d5efbfb2d370d4c/e6c30ef16_generated_9dba7e8f.jpg" alt="profile" />
        </div>
        <div class="info">
          <p class="name">ang <span class="dim">she/her</span></p>
          <p>sixteen <span class="dim">040110</span></p>
          <p>viet-american</p>
          <p>intj-t capricorn</p>
          <p class="dim">pacific standard time</p>
        </div>
        <hr class="sep" />
        <div class="links">
          <h2>links!</h2>
          <ul>
            <li><a href="#"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17.5 19a4.5 4.5 0 1 0 0-9h-1.8A7 7 0 1 0 4 14.9"/></svg> backup twitter</a></li>
            <li><a href="#"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17.5 19a4.5 4.5 0 1 0 0-9h-1.8A7 7 0 1 0 4 14.9"/></svg> youtube channel</a></li>
            <li><a href="#"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17.5 19a4.5 4.5 0 1 0 0-9h-1.8A7 7 0 1 0 4 14.9"/></svg> spotify account</a></li>
          </ul>
          <a class="anime-list" href="#"><svg viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2"><circle cx="12" cy="12" r="9"/></svg> anime list</a>
        </div>
      </aside>

      <main>
        <section class="box">
          <h3>:D</h3>
          <p>bts, anime/manga, mario cart, among us, animal crossing, driving, music, vietnamese food, sleeping, rollercoasters, sunrise and sunset, stuffed animals, and reading</p>
        </section>
        <section class="box">
          <h3>:C</h3>
          <p>antis, no jammers, serious shippers, babies and children, slow walkers, milk, weddings, running, math, malls, judgemental people, airplanes, people who lack common sense</p>
        </section>
        <section class="box">
          <h3>BYF!</h3>
          <p>this is a fan account for bts, but my tweets are not limited to bts...if that makes sense? i might tweet or retweet things unrelated at times. i have social anxiety. i try my best to interact, but that can be difficult. if i do not reply/interact with your tweets, please do not take it personally. i tend to overthink and may delete my tweets sometimes, too. if i ever tweet something questionable, please dm me about it, so i can learn from my mistake.</p>
        </section>
        <section class="box">
          <h3>DFI!</h3>
          <p>honestly... follow me if you want to. i follow back; but i will unfollow you if i deem that you are a bad person.</p>
        </section>
        <section class="box">
          <h3>music</h3>
          <p>bts ~ i love all music from other k-pop &amp; western groups/soloists; however, i just casually listen to their music (ex. txt, heize, stray kids, loona, chung ha, etc.)</p>
        </section>
        <div class="band">
          <img src="https://media.base44.com/images/public/6aad875a3d5efbfb2d370d4c/8a57d00aa_generated_36438992.jpg" alt="band" />
        </div>
        <p class="closing">feel free to message me anytime to talk or if you want to be friends! gotta warn you tho... i'm awkward as fuck</p>
      </main>
    </div>
  </div>
</body>
</html>
```

## Customizing

- **Colors:** edit the CSS variables at the top (`--bg`, `--text`, `--border`, `--white`).
- **Images:** replace the two `<img src="...">` URLs with your own image links.
- **Links:** update the `href="#"` placeholders in the links list and anime list.
- **Text:** edit any of the text inside the `<p>`, `<h2>`, `<h3>`, and `<span>` tags.
