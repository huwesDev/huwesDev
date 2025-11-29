<!doctype html>
<html lang="tr">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>ShakeDev — GitHub Profil (Anime Temalı)</title>
  <meta name="description" content="Anime estetiğiyle hazırlanmış GitHub profil sayfası — tek dosya HTML." />
  <!--
    Kullanım:
    1) `USERNAME` yazan yerleri kendi GitHub kullanıcı adınızla değiştirin.
    2) README veya profil sayfanızda stat görüntüleri kullanmak isterseniz ilgili <img> URL'lerini güncelleyin.
    3) Bu dosyayı GitHub Pages ile veya doğrudan local olarak açabilirsiniz.
  -->
  <style>
    :root{
      --bg:#0b1020; /* koyu gece */
      --card:#0f1724;
      --accent:#ff6b6b; /* pembe-kırmızı accent */
      --glass: rgba(255,255,255,0.04);
      --glass-2: rgba(255,255,255,0.02);
      --mono: 'Inter', ui-sans-serif, system-ui, -apple-system, 'Segoe UI', Roboto;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      font-family:var(--mono);
      background: radial-gradient(1200px 600px at 10% 10%, rgba(80,60,150,0.12), transparent),
                  radial-gradient(800px 400px at 90% 90%, rgba(255,120,120,0.06), transparent),
                  var(--bg);
      color:#e6eef8;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:40px;
    }

    .stage{
      width:100%;
      max-width:1100px;
      display:grid;
      grid-template-columns: 380px 1fr;
      gap:28px;
      align-items:start;
    }

    /* Sol kart */
    .card{
      background: linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));
      border-radius:18px;
      padding:22px;
      box-shadow: 0 10px 30px rgba(2,6,23,0.6), inset 0 1px 0 rgba(255,255,255,0.02);
      border: 1px solid rgba(255,255,255,0.03);
      backdrop-filter: blur(6px) saturate(120%);
      position:relative;
      transform-style:preserve-3d;
      transition: transform .35s cubic-bezier(.2,.9,.3,1);
    }
    .card:hover{ transform: translateY(-6px) rotateX(3deg) }

    .avatar{
      width:120px;height:120px;border-radius:14px;overflow:hidden;border:2px solid rgba(255,255,255,0.06);
      box-shadow: 0 8px 20px rgba(0,0,0,0.6);
    }
    .avatar img{width:100%;height:100%;object-fit:cover;display:block}

    h1{margin:10px 0 6px;font-size:22px}
    p.lead{margin:0;color:#bcd3ff;opacity:0.95}

    .tags{margin-top:12px;display:flex;gap:8px;flex-wrap:wrap}
    .tag{padding:6px 10px;border-radius:999px;background:var(--glass);font-size:13px;color:#dbe8ff;border:1px solid rgba(255,255,255,0.03)}

    /* Sağ panel */
    .panel{
      background: linear-gradient(180deg, rgba(255,255,255,0.01), transparent);
      border-radius:18px;padding:20px;border:1px solid rgba(255,255,255,0.03);
      box-shadow: 0 8px 24px rgba(2,6,23,0.5);
    }
    .hero{
      display:flex;gap:16px;align-items:center;justify-content:space-between;margin-bottom:14px;
    }
    .hero h2{margin:0;font-size:20px}
    .hero .sub{color:#b2c7ff;font-size:13px}

    .grid-two{display:grid;grid-template-columns:1fr 1fr;gap:12px}

    /* 3D-ish anime card */
    .anime-card{height:160px;border-radius:12px;overflow:hidden;position:relative;background:linear-gradient(135deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.04)}
    .anime-card .bg{
      position:absolute;inset:0;background-image: url('https://images.unsplash.com/photo-1519389950473-47ba0277781c?q=80&w=1600&auto=format&fit=crop&ixlib=rb-4.0.3&s=placeholder');
      background-size:cover;background-position:center;filter:grayscale(.05) contrast(.9) saturate(.9) blur(.6px);opacity:.9;
      transform:translateZ(-10px) scale(1.06);
    }
    .anime-card .vignette{position:absolute;inset:0;background:linear-gradient(180deg, rgba(10,6,20,0.25), rgba(10,6,20,0.45));}
    .anime-card .content{position:relative;padding:16px;display:flex;flex-direction:column;gap:8px;height:100%;}
    .anime-card h3{margin:0;font-size:18px}
    .anime-card p{margin:0;font-size:13px;color:#cbdcff}

    /* stat images */
    .stats img{width:100%;border-radius:10px;border:1px solid rgba(255,255,255,0.03);background:var(--glass-2)}

    footer{margin-top:16px;color:#9fb0ff;font-size:13px}

    /* responsive */
    @media (max-width:880px){
      .stage{grid-template-columns:1fr;}
      .hero{flex-direction:column;align-items:flex-start;gap:8px}
    }
  </style>
</head>
<body>
  <main class="stage">
    <section class="card" aria-labelledby="profile">
      <div style="display:flex;gap:12px;align-items:center">
        <div class="avatar">
          <!-- Örnek anime avatar, istersen değiştirebilirsin -->
          <img src="https://i.pinimg.com/originals/7f/6f/0f/7f6f0f0d3d6f9d0f8b6a1f0c8a4c0c1b.jpg" alt="anime avatar" />
        </div>
        <div>
          <h1 id="profile">ShakeDev — <small style="opacity:.8">Anime Temalı</small></h1>
          <p class="lead">Kod + tasarım + anime estetiği. Full-stack geliştirici.</p>
          <div class="tags">
            <span class="tag">TypeScript</span>
            <span class="tag">React</span>
            <span class="tag">Node.js</span>
            <span class="tag">Discord Bot</span>
          </div>
        </div>
      </div>

      <div style="margin-top:16px">
        <div style="display:flex;gap:8px;align-items:center;">
          <div style="flex:1">
            <strong>Hakkımda</strong>
            <p style="margin:6px 0 0;color:#bcd3ff;font-size:14px">Projelerimi anime hissiyle tasarlar, temiz kod yazarım. Otomasyon ve e-ticaret projeleri yapıyorum.</p>
          </div>
        </div>

        <div style="display:flex;gap:8px;margin-top:12px;flex-wrap:wrap">
          <a href="#projects" style="text-decoration:none;padding:8px 12px;border-radius:8px;background:linear-gradient(90deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.03);">Projeler</a>
          <a href="#contact" style="text-decoration:none;padding:8px 12px;border-radius:8px;">İletişim</a>
        </div>
      </div>

      <footer>
        <div style="display:flex;gap:12px;margin-top:14px;align-items:center">
          <img src="https://img.icons8.com/ios-filled/24/ffffff/github.png" alt="github" style="opacity:.9"/>
          <div>
            <div style="font-size:13px">GitHub: <strong>USERNAME</strong></div>
            <div style="font-size:12px;color:#93b1ff">README'ye ekleyebileceğin stat görselleri aşağıda.</div>
          </div>
        </div>
      </footer>
    </section>

    <section class="panel">
      <div class="hero">
        <div>
          <h2>Öne Çıkan Projeler</h2>
          <div class="sub">Minimal, ölçeklenebilir ve anime etkili</div>
        </div>
        <div style="text-align:right">
          <small style="color:#9fb0ff">Güncel: Otomatik olarak güncelle</small>
        </div>
      </div>

      <div class="grid-two">
        <div class="anime-card">
          <div class="bg" aria-hidden></div>
          <div class="vignette"></div>
          <div class="content">
            <h3>ShakeShop</h3>
            <p>E‑ticaret altyapısı — Stripe, admin paneli, hızlı deploy.</p>
            <div style="margin-top:auto;display:flex;gap:8px;align-items:center">
              <span style="font-size:12px;color:#bcd3ff">Tech: Next.js • Node • PostgreSQL</span>
            </div>
          </div>
        </div>

        <div style="display:flex;flex-direction:column;gap:12px">
          <div class="anime-card" style="height:72px;display:flex;align-items:center;padding:12px">
            <div style="flex:1">
              <strong>ShakeBot</strong>
              <div style="font-size:13px;color:#cbdcff">Discord bot — moderasyon, oyun, ekonomi</div>
            </div>
            <div style="width:64px;height:64px;border-radius:8px;background:var(--glass);display:flex;align-items:center;justify-content:center">🤖</div>
          </div>

          <div class="anime-card" style="height:72px;display:flex;align-items:center;padding:12px">
            <div style="flex:1">
              <strong>DevSnippets</strong>
              <div style="font-size:13px;color:#cbdcff">Hızlı kod snippet kütüphanesi</div>
            </div>
            <div style="width:64px;height:64px;border-radius:8px;background:var(--glass);display:flex;align-items:center;justify-content:center">🗃️</div>
          </div>
        </div>
      </div>

      <hr style="border:none;border-top:1px solid rgba(255,255,255,0.03);margin:16px 0">

      <div class="stats">
        <!-- README'ye eklemek için örnek linkler: YOUR_USERNAME ile değiştir -->
        <img src="https://github-readme-stats.vercel.app/api?username=YOUR_USERNAME&show_icons=true&theme=radical" alt="github stats" />
        <div style="height:12px"></div>
        <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=YOUR_USERNAME&layout=compact&theme=radical" alt="top langs" />
      </div>

      <div style="margin-top:12px;display:flex;gap:12px;flex-wrap:wrap">
        <a href="https://github.com/YOUR_USERNAME" target="_blank" rel="noreferrer" style="padding:8px 12px;border-radius:8px;background:var(--accent);color:#081126;text-decoration:none;font-weight:600">GitHub'a Git</a>
        <a href="#contact" style="padding:8px 12px;border-radius:8px;background:transparent;border:1px solid rgba(255,255,255,0.04);text-decoration:none">Daha Fazla</a>
      </div>

      <div id="contact" style="margin-top:18px">
        <strong>İletişim</strong>
        <div style="font-size:13px;color:#b2c7ff;margin-top:6px">Discord: <code>ShakeDev#0001</code> • E‑posta: <code>hello@shakedev.dev</code></div>
      </div>
    </section>
  </main>

  <!-- Opsiyonel küçük JS: username placeholder'ı sayfada gösterir ve README linklerini günceller. -->
  <script>
    (function(){
      const USER = 'YOUR_USERNAME'; // burayı değiştirin
      document.body.querySelectorAll('img').forEach(img=>{
        if(img.src && img.src.includes('YOUR_USERNAME')){
          img.src = img.src.replace(/YOUR_USERNAME/g, USER);
        }
      });
      document.body.innerHTML = document.body.innerHTML.replace(/USERNAME/g, USER);
    })();
  </script>
</body>
</html>
