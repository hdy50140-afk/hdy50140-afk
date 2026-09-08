
<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">

<meta name="description" content="Open Theft Auto — a free, open-source GTA-style sandbox built in Godot.">
<meta property="og:title" content="Open Theft Auto">
<meta property="og:description" content="Free open-source GTA-style sandbox built in Godot.">

<title>Open Theft Auto — Official</title>

<style>
:root{
  --asphalt:#0b0d10;
  --ink:#14171b;
  --ink2:#1b1f24;
  --green:#3ecf6e;
  --amber:#ffb547;
  --gold:#ffd166;
  --paper:#eef1f4;
  --dim:#98a1ab;
  --line:#272d35;
  --body:system-ui,-apple-system,"Segoe UI",Arial,sans-serif;
  --mono:ui-monospace,"SFMono-Regular",Consolas,monospace;
}

*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}

html{
  scroll-behavior:smooth;
}

body{
  background:var(--asphalt);
  color:var(--paper);
  font-family:var(--body);
  line-height:1.6;
}

a{
  color:inherit;
  text-decoration:none;
}

.wrap{
  width:min(1120px,92%);
  margin:auto;
}

/* NAV */

nav{
  position:sticky;
  top:0;
  z-index:20;
  background:rgba(11,13,16,.94);
  border-bottom:1px solid var(--line);
  backdrop-filter:blur(12px);
}

.nav-inner{
  min-height:72px;
  display:flex;
  align-items:center;
  justify-content:space-between;
  gap:20px;
}

.logo{
  font-size:21px;
  font-weight:900;
  letter-spacing:-.7px;
}

.logo span{
  color:var(--green);
}

.nav-links{
  display:flex;
  gap:26px;
  align-items:center;
}

.nav-links a{
  color:var(--dim);
  font-weight:700;
  transition:.2s;
}

.nav-links a:hover{
  color:white;
}

.play{
  background:var(--green);
  color:#07110a;
  padding:11px 17px;
  border-radius:8px;
  font-weight:900;
}

/* HERO */

.hero{
  padding:95px 0 80px;
  border-bottom:1px solid var(--line);
  background:
    radial-gradient(circle at 80% 20%,rgba(62,207,110,.12),transparent 30%),
    radial-gradient(circle at 20% 80%,rgba(255,181,71,.08),transparent 30%);
}

.hero-grid{
  display:grid;
  grid-template-columns:1.15fr .85fr;
  gap:60px;
  align-items:center;
}

.eyebrow{
  color:var(--green);
  font-family:var(--mono);
  font-size:13px;
  font-weight:800;
  letter-spacing:1.5px;
  text-transform:uppercase;
  margin-bottom:18px;
}

h1{
  font-size:clamp(48px,8vw,92px);
  line-height:.92;
  letter-spacing:-5px;
  margin-bottom:25px;
}

h1 span{
  color:var(--green);
}

.hero-text{
  color:var(--dim);
  font-size:19px;
  max-width:650px;
  margin-bottom:30px;
}

.buttons{
  display:flex;
  gap:12px;
  flex-wrap:wrap;
}

.btn{
  display:inline-flex;
  justify-content:center;
  align-items:center;
  min-height:48px;
  padding:12px 20px;
  border-radius:8px;
  font-weight:900;
  border:1px solid var(--line);
  transition:.2s;
}

.btn:hover{
  transform:translateY(-2px);
}

.btn-green{
  background:var(--green);
  color:#07110a;
}

.btn-ghost{
  background:var(--ink2);
  color:white;
}

.hero-card{
  min-height:390px;
  border:1px solid var(--line);
  border-radius:18px;
  overflow:hidden;
  background:
    linear-gradient(145deg,#20262d,#0e1115);
  position:relative;
  display:flex;
  align-items:flex-end;
  padding:28px;
  box-shadow:0 25px 80px rgba(0,0,0,.4);
}

.hero-card:before{
  content:"";
  position:absolute;
  inset:0;
  background:
    linear-gradient(135deg,transparent 45%,rgba(62,207,110,.14)),
    repeating-linear-gradient(
      0deg,
      transparent 0 28px,
      rgba(255,255,255,.025) 29px
    );
}

.card-content{
  position:relative;
}

.card-title{
  font-size:32px;
  font-weight:900;
}

.card-sub{
  color:var(--dim);
}

/* SECTIONS */

section{
  padding:85px 0;
  border-bottom:1px solid var(--line);
}

h2{
  font-size:clamp(34px,5vw,58px);
  line-height:1;
  letter-spacing:-2px;
  margin-bottom:18px;
}

h2 span{
  color:var(--green);
}

.section-intro{
  color:var(--dim);
  max-width:700px;
  margin-bottom:42px;
}

/* LATEST */

.cards{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:18px;
}

.card{
  background:var(--ink);
  border:1px solid var(--line);
  border-radius:14px;
  padding:25px;
}

.card .tag{
  color:var(--amber);
  font-family:var(--mono);
  font-size:12px;
  font-weight:800;
}

.card h3{
  font-size:23px;
  margin:10px 0;
}

.card p{
  color:var(--dim);
}

/* WORLD */

.world{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:20px;
}

.world-card{
  min-height:270px;
  padding:30px;
  border-radius:16px;
  border:1px solid var(--line);
  background:linear-gradient(135deg,var(--ink),var(--ink2));
  display:flex;
  flex-direction:column;
  justify-content:flex-end;
}

.world-card h3{
  font-size:30px;
  margin-bottom:7px;
}

.world-card p{
  color:var(--dim);
}

/* EMPIRE */

.stats{
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:14px;
  margin-top:35px;
}

.stat{
  padding:25px;
  background:var(--ink);
  border:1px solid var(--line);
  border-radius:12px;
}

.stat-number{
  font-size:38px;
  font-weight:950;
  color:var(--gold);
  line-height:1;
}

.stat-label{
  color:var(--dim);
  margin-top:8px;
  font-family:var(--mono);
  font-size:12px;
}

/* CONTROLS */

.controls{
  display:grid;
  grid-template-columns:repeat(2,1fr);
  gap:18px;
}

.control-box{
  background:var(--ink);
  border:1px solid var(--line);
  border-radius:14px;
  padding:25px;
}

.control-box h3{
  margin-bottom:18px;
}

.bind{
  display:flex;
  justify-content:space-between;
  gap:15px;
  padding:12px 0;
  border-bottom:1px solid var(--line);
  color:var(--dim);
}

.bind:last-child{
  border-bottom:0;
}

.keys{
  display:flex;
  gap:5px;
  flex-wrap:wrap;
}

kbd{
  display:inline-block;
  padding:3px 8px;
  border:1px solid #454d56;
  border-radius:5px;
  background:#0b0e11;
  color:white;
  font-family:var(--mono);
  font-size:11px;
}

/* DOWNLOAD */

.steps{
  display:grid;
  grid-template-columns:repeat(3,1fr);
  gap:18px;
}

.step{
  background:var(--ink);
  border:1px solid var(--line);
  border-radius:14px;
  padding:28px;
}

.num{
  width:38px;
  height:38px;
  display:grid;
  place-items:center;
  background:var(--green);
  color:#07110a;
  border-radius:50%;
  font-weight:950;
  margin-bottom:18px;
}

.step h3{
  font-size:23px;
  margin-bottom:9px;
}

.step p{
  color:var(--dim);
  margin-bottom:20px;
}

.step .btn{
  width:100%;
  margin-top:8px;
}

.clone{
  border:1px dashed #454d56;
  border-radius:8px;
  padding:11px;
  color:var(--dim);
  font-family:var(--mono);
  font-size:12px;
}

.req{
  text-align:center;
  color:var(--dim);
  font-family:var(--mono);
  font-size:11px;
  margin-top:35px;
}

/* FOOTER */

footer{
  padding:50px 0;
  color:var(--dim);
  background:#080a0c;
}

footer p{
  margin:8px 0;
}

footer a{
  color:var(--green);
}

/* MOBILE */

@media(max-width:800px){

  .nav-inner{
    min-height:64px;
  }

  .nav-links{
    display:none;
  }

  .hero{
    padding:65px 0;
  }

  .hero-grid{
    grid-template-columns:1fr;
    gap:35px;
  }

  h1{
    letter-spacing:-3px;
  }

  .hero-card{
    min-height:280px;
  }

  section{
    padding:60px 0;
  }

  .cards,
  .world,
  .controls,
  .steps{
    grid-template-columns:1fr;
  }

  .stats{
    grid-template-columns:repeat(2,1fr);
  }

  .buttons .btn{
    width:100%;
  }
}

@media(max-width:420px){

  .stats{
    grid-template-columns:1fr;
  }

  h1{
    font-size:50px;
  }

  h2{
    font-size:38px;
  }
}
</style>
</head>

<body>

<!-- NAV -->
<nav>
  <div class="wrap nav-inner">

    <a class="logo" href="#">
      Open <span>Theft</span> Auto
    </a>

    <div class="nav-links">
      <a href="#latest">Latest</a>
      <a href="#world">World</a>
      <a href="#empire">Empire</a>
      <a href="#controls">Controls</a>
      <a class="play" href="#get">Play free →</a>
    </div>

  </div>
</nav>


<!-- HERO -->
<header class="hero">
  <div class="wrap hero-grid">

    <div>

      <p class="eyebrow">
        Free · Open Source · Godot
      </p>

      <h1>
        Open<br>
        <span>Theft Auto</span>
      </h1>

      <p class="hero-text">
        A free open-source GTA-style sandbox built in Godot.
        Build New Harbor Island, hunt Forbes rivals, mine
        helium-3 on the Moon, and build a $1T empire.
      </p>

      <div class="buttons">
        <a class="btn btn-green" href="#get">
          Download the game
        </a>

        <a class="btn btn-ghost" href="#world">
          Explore the world
        </a>
      </div>

    </div>

    <div class="hero-card">
      <div class="card-content">
        <p class="eyebrow">NEW HARBOR ISLAND</p>
        <div class="card-title">
          Build it.<br>
          Own it.
        </div>
        <p class="card-sub">
          Your city. Your empire. Your rules.
        </p>
      </div>
    </div>

  </div>
</header>


<!-- LATEST -->
<section id="latest">
  <div class="wrap">

    <p class="eyebrow">What's happening</p>

    <h2>
      Latest <span>updates.</span>
    </h2>

    <p class="section-intro">
      Explore the latest features and systems inside
      Open Theft Auto.
    </p>

    <div class="cards">

      <article class="card">
        <span class="tag">01 · CITY</span>
        <h3>New Harbor Island</h3>
        <p>
          Build businesses, expand your territory and
          turn a small island into a massive city.
        </p>
      </article>

      <article class="card">
        <span class="tag">02 · EMPIRE</span>
        <h3>Forbes Rivals</h3>
        <p>
          Compete against wealthy rivals and climb
          your way toward the top.
        </p>
      </article>

      <article class="card">
        <span class="tag">03 · MOON</span>
        <h3>Lunar Mining</h3>
        <p>
          Travel beyond Earth and mine helium-3
          to fuel your growing empire.
        </p>
      </article>

    </div>

  </div>
</section>


<!-- WORLD -->
<section id="world">
  <div class="wrap">

    <p class="eyebrow">Open world</p>

    <h2>
      One world.<br>
      <span>Infinite possibilities.</span>
    </h2>

    <p class="section-intro">
      Explore cities, industrial zones and the Moon.
      Build your fortune and decide how you want to play.
    </p>

    <div class="world">

      <div class="world-card">
        <p class="eyebrow">EARTH</p>
        <h3>New Harbor Island</h3>
        <p>
          Streets, businesses, vehicles and opportunities
          everywhere you look.
        </p>
      </div>

      <div class="world-card">
        <p class="eyebrow">SPACE</p>
        <h3>The Moon</h3>
        <p>
          Mine lunar helium-3 and turn space resources
          into an economic advantage.
        </p>
      </div>

    </div>

  </div>
</section>


<!-- EMPIRE -->
<section id="empire">
  <div class="wrap">

    <p class="eyebrow">Build your fortune</p>

    <h2>
      From zero to <span>$1T.</span>
    </h2>

    <p class="section-intro">
      Start small, grow your operations and build
      an empire that reaches far beyond the city.
    </p>

    <div class="stats">

      <div class="stat">
        <div class="stat-number">$1T</div>
        <div class="stat-label">TARGET EMPIRE VALUE</div>
      </div>

      <div class="stat">
        <div class="stat-number">3D</div>
        <div class="stat-label">GODOT WORLD</div>
      </div>

      <div class="stat">
        <div class="stat-number">∞</div>
        <div class="stat-label">POSSIBILITIES</div>
      </div>

      <div class="stat">
        <div class="stat-number">FREE</div>
        <div class="stat-label">OPEN SOURCE</div>
      </div>

    </div>

  </div>
</section>


<!-- CONTROLS -->
<section id="controls">
  <div class="wrap">

    <p class="eyebrow">Controls</p>

    <h2>
      Your game.<br>
      <span>Your controls.</span>
    </h2>

    <p class="section-intro">
      Keyboard and controller support with
      rebindable actions.
    </p>

    <div class="controls">

      <div class="control-box">

        <h3>Keyboard</h3>

        <div class="bind">
          <span class="keys">
            <kbd>W</kbd>
            <kbd>A</kbd>
            <kbd>S</kbd>
            <kbd>D</kbd>
          </span>
          <span>Move</span>
        </div>

        <div class="bind">
          <span class="keys">
            <kbd>SPACE</kbd>
          </span>
          <span>Jump</span>
        </div>

        <div class="bind">
          <span class="keys">
            <kbd>E</kbd>
          </span>
          <span>Interact · Vehicle · Suit</span>
        </div>

        <div class="bind">
          <span class="keys">
            <kbd>1</kbd>
            <kbd>2</kbd>
          </span>
          <span>Cycle weapons</span>
        </div>

        <div class="bind">
          <span class="keys">
            <kbd>ENTER</kbd>
          </span>
          <span>Confirm</span>
        </div>

        <div class="bind">
          <span class="keys">
            <kbd>ESC</kbd>
          </span>
          <span>Pause / Settings</span>
        </div>

      </div>


      <div class="control-box">

        <h3>Controller</h3>

        <div class="bind">
          <span class="keys">
            <kbd>LS</kbd>
          </span>
          <span>Move</span>
        </div>

        <div class="bind">
          <span class="keys">
            <kbd>A</kbd>
          </span>
          <span>Jump</span>
        </div>

        <div class="bind">
          <span class="keys">
            <kbd>X</kbd>
          </span>
          <span>Interact</span>
        </div>

        <div class="bind">
          <span class="keys">
            <kbd>LB</kbd>
            <kbd>RB</kbd>
          </span>
          <span>Cycle weapons</span>
        </div>

        <div class="bind">
          <span class="keys">
            <kbd>A</kbd>
          </span>
          <span>Confirm</span>
        </div>

        <div class="bind">
          <span class="keys">
            <kbd>MENU</kbd>
          </span>
          <span>Pause / Settings</span>
        </div>

      </div>

    </div>

    <p class="req">
      EVERY ACTION IS REBINDABLE IN-GAME
    </p>

  </div>
</section>


<!-- GET THE GAME -->
<section id="get">
  <div class="wrap">

    <p class="eyebrow">
      Standalone builds · No engine required
    </p>

    <h2>
      Playing tonight.<br>
      <span>Three quick steps.</span>
    </h2>

    <div class="steps">

      <div class="step">

        <span class="num">1</span>

        <h3>Download the game</h3>

        <p>
          Choose the available build for your device.
        </p>

        <a
          class="btn btn-green"
          href="https://github.com/mehulkapadia5/open-theft-auto/releases/download/v1.0.0/Open-Theft-Auto-macOS-v1.0.zip">
          Download for macOS
        </a>

        <a
          class="btn btn-ghost"
          href="https://github.com/mehulkapadia5/open-theft-auto/releases/download/v1.0.0/openTheftAuto.apk">
          Android · Download APK
        </a>

      </div>


      <div class="step">

        <span class="num">2</span>

        <h3>Install it</h3>

        <p>
          Open the downloaded file and follow
          the normal installation steps.
        </p>

        <div class="clone">
          Open Theft Auto
        </div>

      </div>


      <div class="step">

        <span class="num">3</span>

        <h3>Open and play</h3>

        <p>
          Launch the game and start building
          your own empire.
        </p>

        <a
          class="btn btn-ghost"
          href="https://github.com/mehulkapadia5/open-theft-auto/archive/refs/heads/main.zip">
          Download source →
        </a>

      </div>

    </div>

    <p class="req">
      MACOS 11+ OR ANDROID · KEYBOARD OR CONTROLLER
    </p>

  </div>
</section>


<!-- FOOTER -->
<footer>

  <div class="wrap">

    <p>
      <a href="https://github.com/mehulkapadia5/open-theft-auto">
        GitHub Repository
      </a>
    </p>

    <p>
      Built with the Godot Engine.
    </p>

    <p>
      A fan-made open-source sandbox.
      Not affiliated with Rockstar Games.
    </p>

  </div>

</footer>

</body>
</html>
