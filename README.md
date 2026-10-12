<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Hacienda Raíces</title>
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,300;0,400;0,600;1,400&family=Montserrat:wght@300;400;500&display=swap" rel="stylesheet">
<style>
:root{--blanco:#FAF6F0;--arena:#D9C7A7;--terra:#B5623C;--cafe:#6B4A2F;--oliva:#6E7B4B;--texto:#5A5044}
*{margin:0;padding:0;box-sizing:border-box}
html{scroll-behavior:smooth}
body{font-family:'Montserrat',sans-serif;background:var(--blanco);color:var(--texto);line-height:1.7;font-weight:300}
img{max-width:100%;display:block}
a{text-decoration:none;color:inherit}
.nav{position:fixed;top:0;left:0;width:100%;z-index:1000;padding:1.2rem 3rem;display:flex;justify-content:space-between;align-items:center;transition:.4s}
.nav.scrolled{background:rgba(250,246,240,.97);box-shadow:0 2px 20px rgba(107,74,47,.08)}
.nav-logo{font-family:'Cormorant Garamond',serif;font-size:1.6rem;font-weight:600;color:var(--blanco)}
.nav.scrolled .nav-logo{color:var(--cafe)}
.nav-links{display:flex;gap:2.5rem;list-style:none}
.nav-links a{font-size:.8rem;font-weight:500;letter-spacing:.15em;text-transform:uppercase;color:var(--blanco)}
.nav.scrolled .nav-links a{color:var(--cafe)}
.hero{position:relative;height:100vh;min-height:600px;display:flex;align-items:center;justify-content:center;text-align:center}
.hero-bg{position:absolute;inset:0;background:linear-gradient(to bottom,rgba(44,36,24,.3),rgba(44,36,24,.5)),url('https://images.unsplash.com/photo-1582268611958-ebfd161ef9cf?w=1920&q=80') center/cover no-repeat}
.hero-content{position:relative;z-index:2;max-width:800px;padding:0 2rem}
.hero-badge{display:inline-block;font-size:.7rem;font-weight:500;letter-spacing:.3em;text-transform:uppercase;color:var(--arena);border:1px solid rgba(217,199,167,.5);padding:.5rem 1.5rem;margin-bottom:2rem}
.hero h1{font-family:'Cormorant Garamond',serif;font-size:clamp(2.8rem,6vw,5rem);font-weight:300;color:var(--blanco);line-height:1.15;margin-bottom:1.5rem}
.hero h1 em{font-style:italic}
.hero-subtitle{font-size:1rem;color:rgba(250,246,240,.85);letter-spacing:.05em;margin-bottom:2.5rem}
.hero-cta{display:inline-block;font-size:.75rem;font-weight:500;letter-spacing:.2em;text-transform:uppercase;color:var(--blanco);border:1px solid rgba(250,246,240,.6);padding:1rem 2.8rem;transition:.4s}
.hero-cta:hover{background:var(--terra);border-color:var(--terra)}
.section{padding:7rem 3rem}
.section-inner{max-width:1200px;margin:0 auto}
.section-label{font-size:.7rem;font-weight:500;letter-spacing:.3em;text-transform:uppercase;color:var(--terra);margin-bottom:1.5rem}
.section-title{font-family:'Cormorant Garamond',serif;font-size:clamp(2rem,4vw,3.2rem);font-weight:300;color:var(--cafe);line-height:1.2;margin-bottom:1.5rem}
.section-text{font-size:1rem;color:var(--texto);max-width:650px;line-height:1.9}
.concepto-grid{display:grid;grid-template-columns:1fr 1fr;gap:5rem;align-items:center}
.concepto-image img{width:100%;height:500px;object-fit:cover}
.concepto-quote{font-family:'Cormorant Garamond',serif;font-size:1.6rem;font-style:italic;color:var(--terra);line-height:1.5;margin-top:2rem;padding-left:1.5rem;border-left:2px solid var(--arena)}
.arquitectura{background:var(--cafe);color:var(--blanco)}
.arquitectura .section-label{color:var(--arena)}
.arquitectura .section-title{color:var(--blanco)}
.arquitectura .section-text{color:rgba(250,246,240,.75)}
.arco-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:2rem;margin-top:3rem}
.arco-card{background:rgba(250,246,240,.06);border:1px solid rgba(217,199,167,.15);padding:2.5rem}
.arco-card h3{font-family:'Cormorant Garamond',serif;font-size:1.5rem;font-weight:400;color:var(--blanco);margin-bottom:1rem}
.arco-card p{font-size:.9rem;color:rgba(250,246,240,.65);line-height:1.8}
.galeria-header{text-align:center;margin-bottom:3rem}
.galeria-header .section-text{margin:0 auto}
.galeria-grid{display:grid;grid-template-columns:repeat(3,1fr);gap:1.5rem}
.galeria-item{overflow:hidden}
.galeria-item img{width:100%;height:320px;object-fit:cover;transition:.6s}
.galeria-item:hover img{transform:scale(1.05)}
.galeria-item--wide{grid-column:span 2}
.materiales{background:var(--arena);padding:5rem 3rem;text-align:center}
.color-palette{display:flex;justify-content:center;gap:2.5rem;flex-wrap:wrap;margin-top:2rem}
.color-swatch{text-align:center}
.color-swatch-circle{width:80px;height:80px;border-radius:50%;margin:0 auto 1rem;border:3px solid rgba(255,255,255,.5)}
.color-swatch-name{font-size:.7rem;font-weight:500;letter-spacing:.15em;text-transform:uppercase;color:var(--cafe)}
.cierre{position:relative;padding:8rem 3rem;text-align:center;background:linear-gradient(to bottom,rgba(44,36,24,.6),rgba(44,36,24,.85)),url('https://images.unsplash.com/photo-1600585154340-be6161a56a0c?w=1920&q=80') center/cover no-repeat}
.cierre h2{font-family:'Cormorant Garamond',serif;font-size:clamp(2.2rem,5vw,3.5rem);font-weight:300;color:var(--blanco);line-height:1.25;margin-bottom:2rem}
.cierre h2 em{font-style:italic}
.cierre p{color:rgba(250,246,240,.8);margin-bottom:2.5rem;max-width:650px;margin-left:auto;margin-right:auto}
.cierre-cta{display:inline-block;font-size:.75rem;font-weight:500;letter-spacing:.2em;text-transform:uppercase;color:var(--cafe);background:var(--blanco);padding:1.1rem 3rem;transition:.4s}
.cierre-cta:hover{background:var(--terra);color:var(--blanco)}
.contacto-grid{display:grid;grid-template-columns:1fr 1fr;gap:5rem}
.contacto-info h3{font-family:'Cormorant Garamond',serif;font-size:1.3rem;font-weight:400;color:var(--cafe);margin:1.5rem 0 .3rem}
.contacto-info h3:first-child{margin-top:0}
.form-group{display:flex;flex-direction:column;gap:.5rem;margin-bottom:1.5rem}
.form-group label{font-size:.7rem;font-weight:500;letter-spacing:.15em;text-transform:uppercase;color:var(--cafe)}
.form-group input,.form-group textarea{font-family:'Montserrat',sans-serif;font-size:.95rem;color:var(--cafe);background:transparent;border:none;border-bottom:1px solid var(--arena);padding:.8rem 0;outline:none}
.form-group textarea{min-height:110px;resize:vertical}
.form-submit{font-family:'Montserrat',sans-serif;font-size:.75rem;font-weight:500;letter-spacing:.2em;text-transform:uppercase;color:var(--blanco);background:var(--terra);border:none;padding:1rem 3rem;cursor:pointer;transition:.4s}
.form-submit:hover{background:var(--cafe)}
.footer{background:#2C2418;padding:2.5rem;text-align:center}
.footer p{font-size:.75rem;color:rgba(250,246,240,.5);letter-spacing:.1em}
@media(max-width:900px){.concepto-grid,.contacto-grid,.arco-grid{grid-template-columns:1fr}.galeria-grid{grid-template-columns:1fr}.galeria-item--wide{grid-column:span 1}.nav-links{display:none}}
</style>
</head>
<body>
<nav class="nav" id="nav">
  <a href="#" class="nav-logo">Hacienda Raíces</a>
  <ul class="nav-links">
    <li><a href="#concepto">Concepto</a></li>
    <li><a href="#arquitectura">Arquitectura</a></li>
    <li><a href="#galeria">Galería</a></li>
    <li><a href="#contacto">Contacto</a></li>
  </ul>
</nav>

<section class="hero">
  <div class="hero-bg"></div>
  <div class="hero-content">
    <span class="hero-badge">Venta Exclusiva</span>
    <h1>Hacienda<br><em>Raíces</em></h1>
    <p class="hero-subtitle">Tradición, calidez y conexión con el hogar</p>
    <a href="#contacto" class="hero-cta">Agendar una visita</a>
  </div>
</section>

<section class="section" id="concepto">
  <div class="section-inner">
    <div class="concepto-grid">
      <div class="concepto-image">
        <img src="https://images.unsplash.com/photo-1600596542815-ffad4c1539a9?w=800&q=80" alt="Interior Hacienda Raíces">
      </div>
      <div>
        <span class="section-label">El Concepto</span>
        <h2 class="section-title">Tradición, calidez y<br>conexión con el hogar</h2>
        <p class="section-text">Hacienda Raíces busca transmitir tranquilidad y una sensación de hogar auténtico, mediante elementos tradicionales mexicanos combinados con un estilo de hacienda contemporánea.</p>
        <p class="concepto-quote">"Donde las raíces se convierten en hogar."</p>
      </div>
    </div>
  </div>
</section>

<section class="section arquitectura" id="arquitectura">
  <div class="section-inner">
    <span class="section-label">Arquitectura</span>
    <h2 class="section-title">Elementos que construyen<br>la identidad</h2>
    <p class="section-text">Un sello que evoca la arquitectura de haciendas mexicanas contemporáneas: arcos que conectan origen, hogar y naturaleza.</p>
    <div class="arco-grid">
      <div class="arco-card">
        <h3>Arcos de Teja</h3>
        <p>Arcos de barro tradicionales que marcan la entrada a cada espacio, creando transiciones fluidas entre interiores y exteriores.</p>
      </div>
      <div class="arco-card">
        <h3>Columnas de Madera</h3>
        <p>Vigas y carpintería de madera natural que aportan calidez, textura y un carácter rústico-elegante a cada ambiente.</p>
      </div>
      <div class="arco-card">
        <h3>Ventanas y Muros</h3>
        <p>Muros con acabado natural en yeso que reflejan la luz, combinados con amplios ventanales que conectan con el exterior.</p>
      </div>
    </div>
  </div>
</section>

<section class="section" id="galeria">
  <div class="section-inner">
    <div class="galeria-header">
      <span class="section-label">Galería</span>
      <h2 class="section-title">Espacios que inspiran</h2>
      <p class="section-text">Cada espacio fue diseñado para ofrecer una experiencia de vida excepcional, donde la arquitectura y la naturaleza coexisten.</p>
    </div>
    <div class="galeria-grid">
      <div class="galeria-item galeria-item--wide"><img src="https://images.unsplash.com/photo-1600585154340-be6161a56a0c?w=1200&q=80" alt="Fachada principal"></div>
      <div class="galeria-item"><img src="https://images.unsplash.com/photo-1600210492486-724fe5c67fb0?w=800&q=80" alt="Sala con arcos"></div>
      <div class="galeria-item"><img src="https://images.unsplash.com/photo-1600607687939-ce8a6c25118c?w=800&q=80" alt="Patio interior"></div>
      <div class="galeria-item"><img src="https://images.unsplash.com/photo-1600566753190-17f0baa2a6c3?w=800&q=80" alt="Cocina tradicional"></div>
      <div class="galeria-item galeria-item--wide"><img src="https://images.unsplash.com/photo-1600573472592-401b489a3cdc?w=1200&q=80" alt="Jardín y fuente"></div>
    </div>
  </div>
</section>
<section class="materiales">
  <div class="section-inner">
    <span class="section-label" style="color:var(--cafe)">Identidad Visual</span>
    <h2 class="section-title" style="color:var(--cafe)">Materiales que evocan origen</h2>
    <div class="color-palette">
      <div class="color-swatch"><div class="color-swatch-circle" style="background:#B5623C"></div><span class="color-swatch-name">Teja de barro</span></div>
      <div class="color-swatch"><div class="color-swatch-circle" style="background:#D9C7A7"></div><span class="color-swatch-name">Beige arena</span></div>
      <div class="color-swatch"><div class="color-swatch-circle" style="background:#FAF6F0"></div><span class="color-swatch-name">Blanco cálido</span></div>
      <div class="color-swatch"><div class="color-swatch-circle" style="background:#6B4A2F"></div><span class="color-swatch-name">Café madera</span></div>
      <div class="color-swatch"><div class="color-swatch-circle" style="background:#6E7B4B"></div><span class="color-swatch-name">Verde oliva</span></div>
    </div>
  </div>
</section>

<section class="cierre">
  <h2>Donde las raíces<br>se convierten en <em>hogar</em></h2>
  <p>Hacienda Raíces representa un hogar que conserva la esencia de la arquitectura mexicana, incorporando comodidad y una imagen contemporánea.</p>
  <a href="#contacto" class="cierre-cta">Contáctanos</a>
</section>

<section class="section" id="contacto">
  <div class="section-inner">
    <div class="contacto-grid">
      <div class="contacto-info">
        <span class="section-label">Contacto</span>
        <h2 class="section-title">¿Te interesa conocerla?</h2>
        <h3>Teléfono</h3>
        <p>+52 000 000 0000</p>
        <h3>Correo</h3>
        <p>tu@correo.com</p>
        <h3>Ubicación</h3>
        <p>Ciudad, México</p>
      </div>
      <form class="contacto-form" onsubmit="alert('¡Gracias! Te contactaremos pronto.');return false;">
        <div class="form-group"><label>Nombre</label><input type="text" required></div>
        <div class="form-group"><label>Correo</label><input type="email" required></div>
        <div class="form-group"><label>Mensaje</label><textarea required></textarea></div>
        <button type="submit" class="form-submit">Enviar mensaje</button>
      </form>
    </div>
  </div>
</section>

<footer class="footer"><p>Hacienda Raíces © 2026 — Todos los derechos reservados</p></footer>

<script>
window.addEventListener('scroll',function(){
  document.getElementById('nav').classList.toggle('scrolled',window.scrollY>60);
});
</script>
</body>
</html>
