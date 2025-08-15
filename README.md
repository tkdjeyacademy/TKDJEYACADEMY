// app/page.tsx
export default function Home() {
  const heroUrl = ""; // opcional: pega aquí una URL pública de una foto para el fondo

  return (
    <main style={{ fontFamily:"system-ui,-apple-system,Segoe UI,Roboto,Ubuntu,Helvetica,Arial,'Noto Sans',sans-serif", background:"#0b1220", color:"#eaf0fc" }}>
      <header style={{ position:"sticky", top:0, zIndex:10, background:"rgba(11,18,32,.85)", borderBottom:"1px solid #1b2d52", backdropFilter:"blur(8px)" }}>
        <div style={{ maxWidth:1150, margin:"0 auto", padding:"18px 24px", display:"flex", justifyContent:"space-between", alignItems:"center", gap:16 }}>
          <div style={{ display:"flex", alignItems:"center", gap:10 }}>
            <div style={{ width:44, height:44, borderRadius:10, border:"1px solid #1b2d52", background:"#091226", display:"grid", placeItems:"center", fontWeight:900, color:"#52e0d2" }}>TJ</div>
            <strong>TKD JEY · Taekwondo Academy</strong>
          </div>
          <nav style={{ display:"flex", gap:16, flexWrap:"wrap" }}>
            <a href="#nosotros" style={{ color:"#52e0d2", textDecoration:"none" }}>Nosotros</a>
            <a href="#programas" style={{ color:"#52e0d2", textDecoration:"none" }}>Programas</a>
            <a href="#sedes" style={{ color:"#52e0d2", textDecoration:"none" }}>Sedes</a>
            <a href="#equipo" style={{ color:"#52e0d2", textDecoration:"none" }}>Equipo</a>
            <a href="#contacto" style={{ color:"#52e0d2", textDecoration:"none", border:"1px solid #52e0d2", borderRadius:12, padding:"8px 12px" }}>Contacto</a>
          </nav>
        </div>
      </header>

      <section id="inicio" style={{
        position:"relative", minHeight:"72vh", display:"grid", placeItems:"center", padding:24,
        backgroundImage:`radial-gradient(1200px 600px at 80% -10%, rgba(82,224,210,.15), transparent),
                         radial-gradient(1000px 500px at 10% -10%, rgba(82,224,210,.15), transparent),
                         ${heroUrl ? `url('${heroUrl}')` : "none"}`,
        backgroundSize: heroUrl ? "cover" : "auto", backgroundPosition:"center", backgroundRepeat:"no-repeat"
      }}>
        <div style={{ maxWidth:820, width:"100%", background:"rgba(15,29,56,.82)", border:"1px solid #1b2d52", borderRadius:20, padding:24 }}>
          <span style={tag}>Única academia internacional con sede en EEUU</span>
          <h1 style={{ margin:"10px 0 8px 0", fontSize:40, lineHeight:1.1 }}>Taekwondo para niños, jóvenes y adultos</h1>
          <p>Especialistas en clases para niños desde los 3 años. After School y <strong>Winter &amp; Summer Camps</strong> en USA.</p>
          <div style={{ display:"flex", gap:10, flexWrap:"wrap", marginTop:12 }}>
            <span style={tag}>Inglés y Español</span>
            <span style={tag}>Antibullying</span>
            <span style={tag}>Masters USA &amp; Korea</span>
          </div>
        </div>
      </section>

      <div style={{ maxWidth:1150, margin:"0 auto", padding:"0 24px" }}>
        <section id="nosotros" style={{ padding:"34px 0" }}>
          <h2>Sobre Nosotros</h2>
          <div style={box}>
            Somos la <strong>Academia Internacional de Taekwondo TKD JEY</strong>, con maestros certificados en USA y Corea. Aplicamos
            <em> Psicotraining</em> y biomecánica, con enfoque en Taekwondo Olímpico y Tradicional.
          </div>
        </section>

        <section id="programas" style={{ padding:"34px 0" }}>
          <h2>Programas</h2>
          <div style={box}>
            <ul>
              <li>After School</li><li>Niños desde 3 años</li><li>Inglés y Español</li>
              <li>Winter &amp; Summer Camps (USA)</li><li>Masters certificados USA &amp; Korea</li><li>Antibullying</li>
            </ul>
          </div>
        </section>

        <section id="sedes" style={{ padding:"34px 0" }}>
          <h2>Sedes</h2>
          <div style={{ display:"grid", gap:18, gridTemplateColumns:"repeat(auto-fit, minmax(260px, 1fr))" }}>
            <div style={box}><h3>Santa Cruz, Bolivia</h3><p>Av. San Martín, Shopping Fidalga de Equipetrol, Piso 3.</p></div>
            <div style={box}><h3>Florida, USA</h3><p>8408 NW 17th St, Doral, FL.</p></div>
          </div>
        </section>

        <section id="equipo" style={{ padding:"34px 0" }}>
          <h2>Nuestro Equipo</h2>
          <div style={{ display:"grid", gap:18, gridTemplateColumns:"repeat(auto-fit, minmax(260px, 1fr))" }}>
            <div style={box}><h3>Master Jey Marcano</h3><p>7º Dan WT · 5º Dan ITF · Master en Biomecánica.</p></div>
            <div style={box}><h3>Master Raquel Tueti</h3><p>5º Dan WT · Master en Psicopedagogía · Psicotraining.</p></div>
          </div>
        </section>

        <section id="contacto" style={{ padding:"34px 0" }}>
          <h2>Inscripciones y Contacto</h2>
          <div style={{ display:"grid", gap:18, gridTemplateColumns:"repeat(auto-fit, minmax(260px, 1fr))" }}>
            <div style={box}>
              <p><b>Correo:</b> <a href="mailto:tkdjey@gmail.com">tkdjey@gmail.com</a></p>
              <p><b>Instagram:</b> <a target="_blank" rel="noopener" href="https://instagram.com/tkdjey">@tkdjey</a></p>
              <p><b>TikTok:</b> <a target="_blank" rel="noopener" href="https://www.tiktok.com/@tkdjey_usa">@tkdjey_usa</a></p>
            </div>
            <div style={box}>
              <p><b>Santa Cruz:</b> Av. San Martín, Shopping Fidalga de Equipetrol, Piso 3.</p>
              <p><b>Doral, Florida:</b> 8408 NW 17th St, Doral, FL.</p>
            </div>
          </div>
          <div style={{ borderTop:"1px solid #1b2d52", marginTop:18, paddingTop:14, color:"#a7b3c7", fontSize:14 }}>
            © {new Date().getFullYear()} TKD JEY Taekwondo Academy
          </div>
        </section>
      </div>
    </main>
  );
}

const tag: React.CSSProperties = {
  display:"inline-block", fontSize:12, letterSpacing:.4,
  textTransform:"uppercase", background:"#0c1a33", border:"1px solid #18305c",
  color:"#9ee6dc", padding:"6px 10px", borderRadius:999
};
const box: React.CSSProperties = {
  background:"#0f1d38", border:"1px solid #1b2d52", borderRadius:18, padding:18
};
