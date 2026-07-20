<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Deepak Kararwal — THz Research Desktop</title>
<style>
:root{
  --win-gray:#c0c0c0;
  --win-dark:#808080;
  --win-light:#ffffff;
  --win-blue:#000080;
  --win-teal:#008080;
  --text:#000000;
}
*{box-sizing:border-box}
body{
  margin:0;
  background:var(--win-teal);
  color:var(--text);
  font-family:"MS Sans Serif",Tahoma,Geneva,sans-serif;
  font-size:15px;
}
.desktop{
  width:min(1180px,calc(100% - 24px));
  margin:20px auto 76px;
}
.window{
  background:var(--win-gray);
  border-top:2px solid var(--win-light);
  border-left:2px solid var(--win-light);
  border-right:2px solid #404040;
  border-bottom:2px solid #404040;
  box-shadow:2px 2px 0 #000;
  margin-bottom:18px;
}
.titlebar{
  background:var(--win-blue);
  color:#fff;
  display:flex;
  justify-content:space-between;
  align-items:center;
  min-height:30px;
  padding:3px 4px 3px 8px;
  font-weight:bold;
  letter-spacing:.2px;
}
.titlebar .controls{
  display:flex;
  gap:3px;
}
.win-btn{
  width:25px;
  height:23px;
  display:grid;
  place-items:center;
  background:var(--win-gray);
  color:#000;
  border-top:2px solid var(--win-light);
  border-left:2px solid var(--win-light);
  border-right:2px solid #404040;
  border-bottom:2px solid #404040;
  font-weight:bold;
  line-height:1;
}
.window-body{
  padding:16px;
}
.hero{
  text-align:center;
  padding:28px 18px 24px;
}
.hero h1{
  margin:0 0 12px;
  font-size:clamp(2rem,5vw,4rem);
  line-height:1.05;
}
.hero h2{
  margin:0 0 10px;
  font-size:1.45rem;
}
.hero p{
  margin:6px 0;
}
.menu-bar{
  display:flex;
  flex-wrap:wrap;
  gap:3px;
  padding:4px 6px;
  border-bottom:1px solid var(--win-dark);
}
.menu-item{
  padding:4px 9px;
}
.menu-item:hover{
  background:var(--win-blue);
  color:#fff;
}
.toolbar{
  display:flex;
  flex-wrap:wrap;
  gap:8px;
  padding:10px 6px 2px;
  justify-content:center;
}
.retro-button{
  display:inline-block;
  text-decoration:none;
  color:#000;
  background:var(--win-gray);
  padding:7px 12px;
  border-top:2px solid var(--win-light);
  border-left:2px solid var(--win-light);
  border-right:2px solid #404040;
  border-bottom:2px solid #404040;
  font-weight:bold;
}
.retro-button:active{
  border-top:2px solid #404040;
  border-left:2px solid #404040;
  border-right:2px solid var(--win-light);
  border-bottom:2px solid var(--win-light);
}
.grid{
  display:grid;
  grid-template-columns:repeat(2,minmax(0,1fr));
  gap:16px;
}
.project-body{
  min-height:340px;
  display:flex;
  flex-direction:column;
}
.project-body ul{
  margin:8px 0 16px;
  padding-left:22px;
}
.project-body .actions{
  margin-top:auto;
  display:flex;
  gap:8px;
  flex-wrap:wrap;
}
.fieldset{
  border-top:2px solid #808080;
  border-left:2px solid #808080;
  border-right:2px solid #fff;
  border-bottom:2px solid #fff;
  padding:14px;
  background:#d4d0c8;
}
.fieldset legend{
  padding:0 6px;
  font-weight:bold;
}
.two-col{
  display:grid;
  grid-template-columns:repeat(2,minmax(0,1fr));
  gap:14px;
}
.icon-row{
  display:flex;
  flex-wrap:wrap;
  justify-content:center;
  gap:10px;
}
.icon{
  min-width:130px;
  padding:10px;
  text-align:center;
  border:1px dotted #606060;
  background:#d4d0c8;
}
.math{
  font-family:"Courier New",monospace;
  background:#000;
  color:#00ff00;
  border-top:2px solid #404040;
  border-left:2px solid #404040;
  border-right:2px solid #fff;
  border-bottom:2px solid #fff;
  padding:16px;
  line-height:1.8;
  overflow:auto;
}
.statusbar{
  display:grid;
  grid-template-columns:1fr auto;
  gap:4px;
  padding:4px;
}
.status-pane{
  padding:4px 7px;
  border-top:2px solid #808080;
  border-left:2px solid #808080;
  border-right:2px solid #fff;
  border-bottom:2px solid #fff;
}
.taskbar{
  position:fixed;
  bottom:0;
  left:0;
  right:0;
  height:48px;
  background:var(--win-gray);
  border-top:2px solid #fff;
  display:flex;
  align-items:center;
  gap:8px;
  padding:5px 8px;
  z-index:10;
}
.start{
  display:flex;
  align-items:center;
  gap:6px;
  font-weight:bold;
  background:var(--win-gray);
  padding:7px 12px;
  border-top:2px solid #fff;
  border-left:2px solid #fff;
  border-right:2px solid #404040;
  border-bottom:2px solid #404040;
}
.task{
  flex:1;
  max-width:300px;
  padding:7px 12px;
  border-top:2px solid #808080;
  border-left:2px solid #808080;
  border-right:2px solid #fff;
  border-bottom:2px solid #fff;
  white-space:nowrap;
  overflow:hidden;
  text-overflow:ellipsis;
}
.clock{
  margin-left:auto;
  padding:7px 12px;
  border-top:2px solid #808080;
  border-left:2px solid #808080;
  border-right:2px solid #fff;
  border-bottom:2px solid #fff;
}
@media(max-width:800px){
  .grid,.two-col{grid-template-columns:1fr}
  .desktop{width:min(100% - 12px,1180px);margin-top:8px}
  .project-body{min-height:auto}
}
</style>
</head>
<body>
<main class="desktop">

<section class="window">
  <div class="titlebar">
    <span>Terahertz_Research_Profile.exe</span>
    <div class="controls">
      <span class="win-btn">_</span>
      <span class="win-btn">□</span>
      <span class="win-btn">×</span>
    </div>
  </div>
  <div class="menu-bar">
    <span class="menu-item"><u>F</u>ile</span>
    <span class="menu-item"><u>R</u>esearch</span>
    <span class="menu-item"><u>P</u>rojects</span>
    <span class="menu-item"><u>T</u>ools</span>
    <span class="menu-item"><u>H</u>elp</span>
  </div>
  <div class="window-body hero">
    <div style="font-size:3rem">🌌</div>
    <h1>Welcome to the World of Terahertz Science</h1>
    <h2>KARARWAL Deepak</h2>
    <p><strong>PhD Student in Terahertz Optics and Photonics</strong></p>
    <p>Department of Electrical Engineering · École de technologie supérieure · ÉTS Montréal</p>
    <div class="toolbar">
      <span class="retro-button">THz Sources</span>
      <span class="retro-button">Vector Beams</span>
      <span class="retro-button">Polarization Imaging</span>
      <span class="retro-button">THz Waveguides</span>
      <span class="retro-button">Scientific Computing</span>
    </div>
  </div>
  <div class="statusbar">
    <div class="status-pane">Ready — exploring THz science through experiments and simulations.</div>
    <div class="status-pane">Profile v1.0</div>
  </div>
</section>

<section class="window">
  <div class="titlebar">
    <span>Research_Profile.txt</span>
    <div class="controls"><span class="win-btn">_</span><span class="win-btn">□</span><span class="win-btn">×</span></div>
  </div>
  <div class="window-body">
    <fieldset class="fieldset">
      <legend>Research Background</legend>
      <p>
        My research focuses on broadband THz generation, structured THz vector beams,
        spatio-spectral polarization analysis, hollow-core circular metallic waveguides,
        spintronic THz emitters, and terahertz time-domain spectroscopy.
      </p>
      <p>
        I combine experimental optics, electromagnetic simulations, signal processing,
        and scientific visualization to investigate THz emission, propagation,
        polarization, dispersion, and light–matter interactions.
      </p>
    </fieldset>
  </div>
</section>

<section class="window">
  <div class="titlebar">
    <span>Research_Areas — Control Panel</span>
    <div class="controls"><span class="win-btn">_</span><span class="win-btn">□</span><span class="win-btn">×</span></div>
  </div>
  <div class="window-body">
    <div class="two-col">
      <fieldset class="fieldset">
        <legend>⚡ THz Sources and Detection</legend>
        <ul>
          <li>Broadband terahertz generation</li>
          <li>Spintronic THz emitters</li>
          <li>Electro-optic detection</li>
          <li>THz time-domain spectroscopy</li>
        </ul>
      </fieldset>
      <fieldset class="fieldset">
        <legend>🌊 Structured THz Fields</legend>
        <ul>
          <li>Radial and azimuthal vector beams</li>
          <li>Spatiotemporal THz fields</li>
          <li>Polarization singularities</li>
          <li>Topological shaping of THz light</li>
        </ul>
      </fieldset>
      <fieldset class="fieldset">
        <legend>🧭 Polarization Imaging</legend>
        <ul>
          <li>Stokes polarimetry</li>
          <li>Spatial polarization maps</li>
          <li>Spectral polarization analysis</li>
          <li>Polarization ellipse reconstruction</li>
        </ul>
      </fieldset>
      <fieldset class="fieldset">
        <legend>📡 THz Waveguides</legend>
        <ul>
          <li>Hollow-core metallic waveguides</li>
          <li>Mode excitation and propagation</li>
          <li>Coupling, loss, and dispersion</li>
          <li>Multimode interference</li>
        </ul>
      </fieldset>
    </div>
  </div>
</section>

<section class="window">
  <div class="titlebar">
    <span>My Computer — Research Tools</span>
    <div class="controls"><span class="win-btn">_</span><span class="win-btn">□</span><span class="win-btn">×</span></div>
  </div>
  <div class="window-body">
    <div class="icon-row">
      <div class="icon">🐍<br><strong>Python</strong></div>
      <div class="icon">🔢<br><strong>NumPy</strong></div>
      <div class="icon">📊<br><strong>Matplotlib</strong></div>
      <div class="icon">🧲<br><strong>Magpylib</strong></div>
      <div class="icon">📝<br><strong>LaTeX</strong></div>
      <div class="icon">⚡<br><strong>THz-TDS</strong></div>
    </div>
  </div>
</section>

<section class="grid">
  <article class="window">
    <div class="titlebar">
      <span>Project_I — Polarization_of_Light.exe</span>
      <div class="controls"><span class="win-btn">_</span><span class="win-btn">□</span><span class="win-btn">×</span></div>
    </div>
    <div class="window-body project-body">
      <h3>🌀 Polarization of Light</h3>
      <p>Interactive simulation of linear, circular, and elliptical polarization.</p>
      <ul>
        <li>Polarization ellipse</li>
        <li>Animated electric-field trajectory</li>
        <li>Stokes parameters</li>
        <li>Orientation and ellipticity angles</li>
      </ul>
      <div class="actions">
        <a class="retro-button" href="https://github.com/kararwaldeepak/light-polarization-simulator">Repository</a>
        <a class="retro-button" href="https://kararwaldeepak.github.io/light-polarization-simulator/">Run</a>
      </div>
    </div>
  </article>

  <article class="window">
    <div class="titlebar">
      <span>Project_II — THz_Time_Domain_Pulse.exe</span>
      <div class="controls"><span class="win-btn">_</span><span class="win-btn">□</span><span class="win-btn">×</span></div>
    </div>
    <div class="window-body project-body">
      <h3>⚡ Time-Domain THz Pulse</h3>
      <p>Interactive exploration of the temporal and spectral properties of a broadband THz pulse.</p>
      <ul>
        <li>Time-domain electric field</li>
        <li>Fourier-amplitude spectrum</li>
        <li>Spectral phase and chirp</li>
        <li>Reflections and noise</li>
      </ul>
      <div class="actions">
        <a class="retro-button" href="https://github.com/kararwaldeepak/thz-time-domain-pulse">Repository</a>
        <a class="retro-button" href="https://kararwaldeepak.github.io/thz-time-domain-pulse/">Run</a>
      </div>
    </div>
  </article>

  <article class="window">
    <div class="titlebar">
      <span>Project_III — Broadband_THz_Vector_Beams.exe</span>
      <div class="controls"><span class="win-btn">_</span><span class="win-btn">□</span><span class="win-btn">×</span></div>
    </div>
    <div class="window-body project-body">
      <h3>🌊 Broadband THz Vector Beams</h3>
      <p>Interactive visualization of radial and azimuthal THz vector fields.</p>
      <ul>
        <li>Beam intensity</li>
        <li>Polarization vectors</li>
        <li>Normalized Stokes maps</li>
        <li>Local polarization ellipse</li>
      </ul>
      <div class="actions">
        <a class="retro-button" href="https://github.com/kararwaldeepak/Kararwaldeepak-broadband-thz-vector-beams">Repository</a>
        <a class="retro-button" href="https://kararwaldeepak.github.io/Kararwaldeepak-broadband-thz-vector-beams/">Run</a>
      </div>
    </div>
  </article>

  <article class="window">
    <div class="titlebar">
      <span>Project_IV — Spatiotemporal_THz_Field.exe</span>
      <div class="controls"><span class="win-btn">_</span><span class="win-btn">□</span><span class="win-btn">×</span></div>
    </div>
    <div class="window-body project-body">
      <h3>🔭 Spatiotemporal THz Electric Field</h3>
      <p>Interactive visualization of delay scans, time frames, FFT frames, and field evolution.</p>
      <ul>
        <li>Scan length and time window</li>
        <li>Frequency resolution</li>
        <li>Nyquist frequency</li>
        <li>Animated x–t field evolution</li>
      </ul>
      <div class="actions">
        <a class="retro-button" href="https://github.com/kararwaldeepak/thz-spatiotemporal-field-explorer">Repository</a>
        <a class="retro-button" href="https://kararwaldeepak.github.io/thz-spatiotemporal-field-explorer/">Run</a>
      </div>
    </div>
  </article>
</section>

<section class="window">
  <div class="titlebar">
    <span>COMMAND.COM — THz Delay-Scan Relations</span>
    <div class="controls"><span class="win-btn">_</span><span class="win-btn">□</span><span class="win-btn">×</span></div>
  </div>
  <div class="window-body">
    <div class="math">
C:\THz&gt; Δt = mΔL / c<br>
C:\THz&gt; L_scan = (N − 1)ΔL<br>
C:\THz&gt; T_span = (N − 1)Δt<br>
C:\THz&gt; Δf = 1 / (NΔt)<br>
C:\THz&gt; f_Nyquist = 1 / (2Δt)<br>
C:\THz&gt; N_f = floor(N/2) + 1<br>
C:\THz&gt; τ_FWHM = t₂ − t₁<br>
C:\THz&gt; B = f_high − f_low
    </div>
  </div>
</section>

<section class="window">
  <div class="titlebar">
    <span>Contact_Information.txt</span>
    <div class="controls"><span class="win-btn">_</span><span class="win-btn">□</span><span class="win-btn">×</span></div>
  </div>
  <div class="window-body">
    <p><strong>GitHub:</strong> <a href="https://github.com/kararwaldeepak">kararwaldeepak</a></p>
    <p><strong>Department:</strong> Electrical Engineering, ÉTS Montréal</p>
    <p><strong>Research:</strong> Terahertz optics, photonics, structured electromagnetic fields, and spatiotemporal shaping of THz light.</p>
  </div>
  <div class="statusbar">
    <div class="status-pane">Open science through interactive simulation and reproducible research.</div>
    <div class="status-pane">© KARARWAL Deepak</div>
  </div>
</section>

</main>

<div class="taskbar">
  <div class="start">🪟 Start</div>
  <div class="task">Terahertz_Research_Profile.exe</div>
  <div class="clock" id="clock">12:00 PM</div>
</div>

<script>
function updateClock(){
  const now=new Date();
  document.getElementById("clock").textContent=now.toLocaleTimeString([],{
    hour:"2-digit",minute:"2-digit"
  });
}
updateClock();
setInterval(updateClock,1000);
</script>
</body>
</html>
