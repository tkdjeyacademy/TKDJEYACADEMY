// app/page.tsx
export default function Home() {
  const heroUrl = ""; // <- pega aquí la URL pública de tu foto para el fondo del Hero (opcional)

  return (
    <main style={{ fontFamily: "system-ui, -apple-system, Segoe UI, Roboto, Ubuntu, Helvetica, Arial, 'Noto Sans', sans-serif", background:"#0b1220", color:"#eaf0fc" }}>
      {/* Header */}
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

      {/* HERO */}
      <section
        id="inicio"
        style={{
          position:"relative",
          minHeight:"72vh",
          display:"grid",
          placeItems:"center",
          padding:24,
          backgroundImage:
            `radial-gradient(1200px 600px at 80% -10%, rgba(82,224,210,.15), transparent),
             radial-gradient(1000px 500px at 10% -10%, rgba(82,224,210,.15), transparent),
             ${heroUrl ? `url('${heroUrl}')` : "none"}`,
          backgroundSize: heroUrl ? "cover" : "auto",
          backgroundPosition:"center",
          backgroundRepeat:"no-repeat",
          filter: heroUrl ? "saturate(1.05) contrast(1.05) brightness(.92)" : undefined
        }}
      >
        <div style={{ maxWidth:820, width:"100%", background:"rgba(15,29,56,.82)", border:"1px solid #1b2d52", borderRadius:20, padding:24 }}>
          <span style={tag}>Única academia internacional con sede en EEUU</span>
          <h1 style={{ margin:"10px 0 8px 0", fontSize:40, lineHeight:1.1 }}>Taekwondo para niños, jóvenes y adultos</h1>
          <p>Especialistas en clases para niños desde los 3 años. Programas After School y <strong>Winter &amp; Summer Camps</strong> en USA.</p>
          <div style={{ display:"flex", gap:10, flexWrap:"wrap", marginTop:12 }}>
            <span style={tag}>Clases en Inglés y Español</span>
            <span style={tag}>Antibullying</span>
            <span style={tag}>Masters certificados USA &amp; Korea</span>
          </div>
          <div style={{ display:"flex", gap:12, marginTop:14 }}>
            <a href="#programas" style={btn}>Ver Programas</a>
            <a href="#contacto" style={btnOutline}>Inscripciones</a>
          </div>
        </div>
      </section>

      <div style={{ maxWidth:1150, margin:"0 auto", padding:"0 24px" }}>
        {/* NOSOTROS */}
        <section id="nosotros" style={{ padding:"34px 0" }}>
          <h2>Sobre Nosotros</h2>
          <div style={box}>
            Somos la <strong>Academia Internacional de Taekwondo TKD JEY</strong>, con maestros certificados en USA y Corea.
            Aplicamos <em>Psicotraining</em> y biomecánica al Taekwondo, con enfoque en Taekwondo Olímpico y Tradicional.
          </div>
          <div style={{ marginTop:16, ...box }}>
            <h3 style={{ marginTop:0 }}>Certificaciones &amp; Afiliaciones</h3>
            <div>
              <span style={pill}>Kukkiwon</span>
              <span style={pill}>WTA</span>
              <span style={pill}>TKD JEY</span>
            </div>
          </div>
        </section>

        {/* PROGRAMAS */}
        <section id="programas" style={{ padding:"34px 0" }}>
          <h2>Programas</h2>
          <div style={box}>
            <ul>
              <li>After School</li>
              <li>Somos especialistas en clases para niños desde los 3 años</li>
              <li>Clases en inglés y español</li>
              <li>Winters y Summer Camps en USA</li>
              <li>Masters certificados en USA y Korea</li>
              <li>Programas antibullying</li>
            </ul>
          </div>
          <div style={{ display:"grid", gap:18, gridTemplateColumns:"repeat(auto-fit, minmax(230px, 1fr))", marginTop:18 }}>
            {[
              ["Pequeños Guerreros (3–6 años)", "Juego, disciplina y coordinación."],
              ["Kids & Teens (7–15 años)", "Técnica, valores y crecimiento competitivo."],
              ["Adultos & Familia", "Defensa personal y entrenamiento en familia."],
              ["Alto Rendimiento", "Biomecánica y Psicotraining para atletas."],
              ["After School", "Hábitos, tareas y Taekwondo."],
              ["Camps en USA", "Entrenamiento intensivo y experiencias internacionales."]
            ].map(([t, d]) => (
              <div key={t} style={program}>
                <h3 style={{ marginTop:0 }}>{t}</h3>
                <p style={{ marginBottom:0 }}>{d}</p>
              </div>
            ))}
          </div>
        </section>

        {/* SEDES */}
        <section id="sedes" style={{ padding:"34px 0" }}>
          <h2>Sedes</h2>
          <div style={{ display:"grid", gap:18, gridTemplateColumns:"repeat(auto-fit, minmax(260px, 1fr))" }}>
            <div style={box}>
              <h3 style={{ marginTop:0 }}>Santa Cruz, Bolivia</h3>
              <p>Av. San Martín, Shopping Fidalga de Equipetrol, Piso 3.</p>
              <p><a target="_blank" rel="noopener" href="https://maps.google.com/?q=Shopping%20Fidalga%20Equipetrol%20Santa%20Cruz%20Bolivia">Ver en Google Maps</a></p>
            </div>
            <div style={box}>
              <h3 style={{ marginTop:0 }}>Florida, USA</h3>
              <p>8408 NW 17th St, Doral, FL.</p>
              <p><a target="_blank" rel="noopener" href="https://maps.google.com/?q=8408%20NW%2017th%20St%2C%20Doral%2C%20FL">Ver en Google Maps</a></p>
            </div>
          </div>
        </section>

        {/* EQUIPO */}
        <section id="equipo" style={{ padding:"34px 0" }}>
          <h2>Nuestro Equipo</h2>
          <div style={{ display:"grid", gap:18, gridTemplateColumns:"repeat(auto-fit, minmax(260px, 1fr))" }}>
            <div style={box}>
              <h3 style={{ marginTop:0 }}>Master Jey Marcano</h3>
              <p>Black belt 7º Dan Taekwondo WT · Black belt 5º Dan Taekwondo ITF.</p>
              <p>Master en Biomecánica y ciencias aplicadas a los deportes de combate.</p>
            </div>
            <div style={box}>
              <h3 style={{ marginTop:0 }}>Master Raquel Tueti</h3>
              <p>Black belt 5º Dan Taekwondo WT · Master en Psicopedagogía.</p>
              <p>Creadora del programa Manejo de Emociones y Psicotraining (alto rendimiento). Asesora y coaching psicopedagógico de la FBT.</p>
            </div>
          </div>
        </section>

        {/* CONTACTO */}
        <section id="contacto" style={{ padding:"34px 0" }}>
          <h2>Inscripciones y Contacto</h2>
          <div style={{ display:"grid", gap:18, gridTemplateColumns:"repeat(auto-fit, minmax(260px, 1fr))" }}>
            <div style={box}>
              <h3 style={{ marginTop:0 }}>Escríbenos</h3>
              <p><strong>Correo:</strong> <a href="mailto:tkdjey@gmail.com">tkdjey@gmail.com</a></p>
              <p><strong>Instagram:</strong> <a target="_blank" rel="noopener" href="https://instagram.com/tkdjey">@tkdjey</a></p>
              <p><strong>TikTok:</strong> <a target="_blank" rel="noopener" href="https://www.tiktok.com/@tkdjey_usa">@tkdjey_usa</a></p>
            </div>
            <div style={box}>
              <h3 style={{ marginTop:0 }}>Visítanos</h3>
              <p><strong>Santa Cruz, Bolivia:</strong> Av. San Martín, Shopping Fidalga de Equipetrol, Piso 3.</p>
              <p><strong>Florida, USA:</strong> 8408 NW 17th St, Doral, FL.</p>
            </div>
          </div>
          <div style={{ borderTop:"1px solid #1b2d52", marginTop:18, paddingTop:14, color:"#a7b3c7", fontSize:14 }}>
            © {new Date().getFullYear()} TKD JEY Taekwondo Academy · Todos los derechos reservados.
          </div>
        </section>
      </div>
    </main>
  );
}

const tag: React.CSSProperties = {
  display:"inline-block",
  fontSize:12,
  letterSpacing:.4,
  textTransform:"uppercase",
  background:"#0c1a33",
  border:"1px solid #18305c",
  color:"#9ee6dc",
  padding:"6px 10px",
  borderRadius:999
};

const btn: React.CSSProperties = {
  display:"inline-block",
  padding:"10px 16px",
  borderRadius:12,
  background:"#52e0d2",
  color:"#03131a",
  fontWeight:800,
  textDecoration:"none"
};

const btnOutline: React.CSSProperties = {
  ...btn,
  background:"transparent",
  color:"#52e0d2",
  border:"1px solid #52e0d2"
};

const box: React.CSSProperties = {
  background:"#0f1d38",
  border:"1px solid #1b2d52",
  borderRadius:18,
  padding:18
};

const program: React.CSSProperties = {
  padding:16,
  borderRadius:16,
  background:"linear-gradient(180deg,#102142,#0b1a33)",
  border:"1px solid #1b2d52"
};
