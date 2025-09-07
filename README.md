<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Untuk Amiee, Dari Sahrul Dengan Cinta ❤️</title>
  <meta name="description" content="Kejutan kecil dari Sahrul untuk Amiee. Sebuah halaman cinta dengan musik, galeri, dan pesan dari hati." />
  <meta property="og:title" content="Untuk Amiee ❤️" />
  <meta property="og:description" content="Kejutan kecil dari Sahrul untuk Amiee. Buka ya!" />
  <meta property="og:type" content="website" />
  <!-- Ganti URL gambar di bawah agar preview link di chat makin cantik -->
  <meta property="og:image" content="https://images.unsplash.com/photo-1519741497674-611481863552?q=80&w=1200&auto=format&fit=crop" />
  <meta name="theme-color" content="#ff8fab" />

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">

  <style>
    :root {
      --rose1: #ff9aa2; /* pink */
      --rose2: #ffb7b2; /* light coral */
      --rose3: #ffdac1; /* peach */
      --ink: #2b2d42;
      --white: #fff;
    }
    * { box-sizing: border-box }
    html, body { height: 100%; }
    body {
      margin: 0;
      font-family: 'Poppins', system-ui, -apple-system, Segoe UI, Roboto, sans-serif;
      color: var(--ink);
      background: linear-gradient(120deg, var(--rose1), var(--rose2), var(--rose3));
      background-size: 200% 200%;
      animation: bgShift 12s ease-in-out infinite;
      overflow-x: hidden;
    }
    @keyframes bgShift {
      0%,100% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
    }

    /* Floating hearts */
    .hearts { position: fixed; inset: 0; overflow: hidden; pointer-events: none; z-index: 0; }
    .heart { position: absolute; bottom: -10vh; font-size: clamp(16px, 3vw, 32px); opacity: .7; animation: floatUp linear forwards; }
    @keyframes floatUp {
      0% { transform: translateY(0) translateX(0) rotate(0deg); opacity: .0; }
      10% { opacity: .7; }
      100% { transform: translateY(-120vh) translateX(var(--drift, 0)) rotate(360deg); opacity: 0; }
    }

    header {
      position: relative; z-index: 2; text-align: center; padding: 64px 20px 32px;
    }
    .badge { display: inline-block; padding: 8px 14px; border-radius: 999px; background: rgba(255,255,255,.6); backdrop-filter: blur(6px); font-size: 14px; }
    h1 { font-size: clamp(28px, 6vw, 56px); margin: 16px auto 8px; line-height: 1.1; }
    .subtitle { font-weight: 300; font-size: clamp(16px, 2.6vw, 22px); opacity: .9; }

    main { position: relative; z-index: 2; padding: 16px 20px 64px; max-width: 960px; margin: 0 auto; }

    /* Card */
    .card { background: rgba(255,255,255,.8); border-radius: 24px; padding: clamp(18px, 3vw, 28px); box-shadow: 0 10px 30px rgba(0,0,0,.12); backdrop-filter: blur(6px); }

    /* Typewriter */
    .type { display:inline-block; border-right: 2px solid var(--ink); white-space: nowrap; overflow: hidden; }

    /* Buttons */
    .btn { appearance: none; border: 0; border-radius: 999px; padding: 12px 18px; font-weight: 600; cursor: pointer; transition: transform .12s ease, box-shadow .2s ease; }
    .btn-primary { background: var(--ink); color: var(--white); box-shadow: 0 8px 16px rgba(43,45,66,.25); }
    .btn-primary:hover { transform: translateY(-1px); box-shadow: 0 12px 22px rgba(43,45,66,.28); }
    .btn-ghost { background: rgba(255,255,255,.65); backdrop-filter: blur(6px); color: var(--ink); }

    .stack { display: grid; gap: 16px; }

    /* Gallery */
    .grid { display: grid; grid-template-columns: repeat(12, 1fr); gap: 14px; margin-top: 18px; }
    .grid img { width: 100%; height: 100%; object-fit: cover; border-radius: 16px; box-shadow: 0 6px 18px rgba(0,0,0,.15); }
    .col-6 { grid-column: span 6; }
    .col-4 { grid-column: span 4; }
    @media (max-width: 700px) {
      .col-6, .col-4 { grid-column: span 12; }
    }

    /* Letter */
    .letter { position: relative; background: #fff; border-radius: 18px; padding: 20px; box-shadow: 0 10px 26px rgba(0,0,0,.12); }
    .letter h3 { margin: 0 0 8px 0; }
    .reveal { display: grid; place-items: center; border: 2px dashed rgba(43,45,66,.25); border-radius: 16px; padding: 18px; cursor: pointer; transition: background .2s; }
    .reveal:hover { background: rgba(0,0,0,.03); }

    footer { text-align: center; opacity: .8; padding: 28px 16px 56px; }
  </style>
</head>
<body>
  <!-- floating hearts layer -->
  <div class="hearts" id="hearts" aria-hidden="true"></div>

  <header>
    <span class="badge">Untuk Amiee dari Sahrul 💌</span>
    <h1>Hai, Amiee ❤️</h1>
    <p class="subtitle">Ada pesan kecil dari hatiku. Semoga membuat harimu hangat, seperti kamu menghangatkan aku.</p>

    <div class="stack" style="margin-top:18px; justify-content:center; align-items:center;">
      <button id="musicBtn" class="btn btn-primary">Putar Musik</button>
      <audio id="bgm" preload="auto">
        <!-- GANTI src DI BAWAH DENGAN LINK LAGU KALIAN (MP3) -->
        <source src="" type="audio/mpeg">
      </audio>
      <small style="opacity:.8">Tip: jika musik tidak otomatis, tekan tombol di atas ya 💿</small>
    </div>
  </header>

  <main>
    <section class="card" aria-label="pesan sayang">
      <h2 style="margin:0 0 6px 0">Pesan Untukmu</h2>
      <p style="margin:0">Aku punya satu kalimat yang selalu ingin aku ulang:</p>
      <p style="font-size:clamp(18px,3.6vw,28px);margin:10px 0 0 0;font-weight:700">
        <span id="type" class="type" aria-live="polite"></span>
      </p>
      <p style="margin-top:12px">Terima kasih sudah jadi rumah paling nyaman untuk hatiku. — Sahrul</p>
      <div class="grid" style="margin-top:10px">
        <!-- Ganti URL gambar di bawah dengan foto kalian -->
        <img class="col-6" src="https://images.unsplash.com/photo-1500648767791-00dcc994a43e?q=80&w=1200&auto=format&fit=crop" alt="Kenangan kita 1" />
        <img class="col-6" src="https://images.unsplash.com/photo-1516826957135-c9d5ffbaea1a?q=80&w=1200&auto=format&fit=crop" alt="Kenangan kita 2" />
        <img class="col-4" src="https://images.unsplash.com/photo-1544211412-2a9b65f7a66a?q=80&w=1200&auto=format&fit=crop" alt="Kenangan kita 3" />
        <img class="col-4" src="https://images.unsplash.com/photo-1519744346366-3f57b6d5f06a?q=80&w=1200&auto=format&fit=crop" alt="Kenangan kita 4" />
        <img class="col-4" src="https://images.unsplash.com/photo-1518199266791-5375a83190b7?q=80&w=1200&auto=format&fit=crop" alt="Kenangan kita 5" />
      </div>
    </section>

    <section style="height:18px"></section>

    <section class="letter" aria-label="surat cinta">
      <h3>Surat Kecil Untuk Amiee 💞</h3>
      <div id="secret" class="reveal" role="button" aria-pressed="false" tabindex="0">
        <strong>Klik di sini untuk membuka</strong>
      </div>
      <div id="content" style="display:none; margin-top:12px; line-height:1.7">
        Dear Amiee,<br/>
        Setiap hari aku bersyukur karena Tuhan menitipkan kamu dalam ceritaku. Caramu tertawa, caramu bercerita, bahkan caramu diam—semuanya menenangkan. Aku ingin kamu tahu, aku selalu ada; bukan hanya untuk hari ini, tapi esok dan seterusnya. Terima kasih sudah jadi ‘rumah’ yang selalu ingin aku pulang.<br/>
        — Sahrul
      </div>
    </section>

    <section style="height:8px"></section>

    <div style="display:flex; gap:10px; flex-wrap:wrap; justify-content:center; margin-top:8px">
      <button class="btn btn-ghost" id="shareBtn">Bagikan Link Ini</button>
      <a class="btn btn-ghost" href="#" id="saveImg">Simpan Pratinjau</a>
    </div>
  </main>

  <footer>
    <small>Made with ❤️ by Sahrul untuk Amiee • 2025</small>
  </footer>

  <script>
    // Floating hearts generator
    const heartsEl = document.getElementById('hearts');
    const HEARTS = 24;
    for (let i = 0; i < HEARTS; i++) {
      const span = document.createElement('span');
      span.className = 'heart';
      span.textContent = ['❤','💖','💗','💞'][Math.floor(Math.random()*4)];
      span.style.left = Math.random()*100 + 'vw';
      span.style.animationDuration = (6 + Math.random()*8) + 's';
      span.style.animationDelay = (Math.random()*6) + 's';
      span.style.setProperty('--drift', (Math.random()*80 - 40) + 'px');
      heartsEl.appendChild(span);
    }

    // Typewriter message
    const typeTarget = document.getElementById('type');
    const lines = [
      'Aku cinta kamu, hari ini dan seterusnya.',
      'Bersamamu, semua terasa pulang.',
      'Kamu dan aku — selamanya kita.'
    ];

    let li = 0, ci = 0, erasing = false;
    function typeLoop(){
      const txt = lines[li];
      if (!erasing){
        typeTarget.textContent = txt.slice(0, ++ci);
        if (ci === txt.length){ erasing = true; setTimeout(typeLoop, 1200); return; }
      } else {
        typeTarget.textContent = txt.slice(0, --ci);
        if (ci === 0){ erasing = false; li = (li+1)%lines.length; }
      }
      setTimeout(typeLoop, erasing ? 36 : 54);
    }
    typeLoop();

    // Music toggle
    const musicBtn = document.getElementById('musicBtn');
    const bgm = document.getElementById('bgm');
    let playing = false;
    musicBtn.addEventListener('click', async () => {
      try {
        if (!playing) { await bgm.play(); playing = true; musicBtn.textContent = 'Hentikan Musik'; }
        else { bgm.pause(); playing = false; musicBtn.textContent = 'Putar Musik'; }
      } catch(e){
        alert('Tidak bisa memutar musik. Coba tekan sekali lagi ya ❤');
      }
    });

    // Reveal letter
    const secret = document.getElementById('secret');
    const content = document.getElementById('content');
    function openLetter(){ secret.style.display = 'none'; content.style.display = 'block'; }
    secret.addEventListener('click', openLetter);
    secret.addEventListener('keydown', (e)=>{ if (e.key === 'Enter' || e.key === ' ') openLetter(); });

    // Share Link (Web Share API)
    const shareBtn = document.getElementById('shareBtn');
    shareBtn.addEventListener('click', async () => {
      const data = { title: 'Untuk Amiee ❤️', text: 'Kejutan kecil dari Sahrul untuk Amiee', url: window.location.href };
      if (navigator.share) { try { await navigator.share(data); } catch(_){} }
      else {
        navigator.clipboard.writeText(window.location.href);
        shareBtn.textContent = 'Link Disalin ✔';
        setTimeout(()=> shareBtn.textContent = 'Bagikan Link Ini', 1400);
      }
    });

    // Dummy save preview (just scroll to top image)
    document.getElementById('saveImg').addEventListener('click', (e)=>{
      e.preventDefault(); window.scrollTo({ top: 0, behavior: 'smooth' });
    });
  </script>
</body>
</html>
