<!-- 🌟 Typing Header -->
<div style="text-align:center;padding:40px;background:#0f172a;color:#fff;">
  <h1 id="typing" style="font-size:2em;"></h1>
  <script>
    const txt = "👋 Hi, I'm Aminul — CSE Final Year | Web & App Dev";
    let i=0; const speed=60;
    function type() {
      if(i<txt.length) {
        document.getElementById("typing").innerHTML += txt.charAt(i);
        i++; setTimeout(type,speed);
      }
    }
    type();
  </script>
</div>

<!-- 🎉 Confetti Effect -->
<div style="position:relative;height:140px;background:#031520;">
  <h2 style="text-align:center;color:#00ffcc;">🎉 Congratulations!</h2>
  <canvas id="confetti" style="position:absolute;top:0;left:0;width:100%;height:100%;pointer-events:none;"></canvas>
  <script>
    const c = document.getElementById("confetti"), ctx = c.getContext("2d");
    c.width = window.innerWidth; c.height = 140;
    const p = Array.from({length:80},()=>({
      x:Math.random()*c.width,y:Math.random()*-c.height,s:Math.random()*6+2,
      clr:`hsl(${Math.random()*360},70%,70%)`,spd:Math.random()*1.5+0.5
    }));
    function animate() {
      ctx.clearRect(0,0,c.width,c.height);
      p.forEach(e=>{
        ctx.beginPath(); ctx.arc(e.x,e.y,e.s,0,Math.PI*2);
        ctx.fillStyle=e.clr; ctx.fill(); e.y+=e.spd;
        if(e.y>c.height) e.y=0;
      }); requestAnimationFrame(animate);
    }
    animate();
  </script>
</div>

<!-- 👨‍💻 Profile Card -->
<div style="max-width:800px;margin:auto;padding:20px;background:#1a1a1a;border-radius:10px;color:#eee;box-shadow:0 0 10px #00ffc550;">
  <img src="YOUR_IMAGE_URL" alt="Aminul Islam" style="width:100px;border-radius:50%;display:block;margin:auto;">
  <h2 style="text-align:center;color:#00ffd5;">Aminul Islam</h2>
  <p style="text-align:center;">🚀 CSE Final Year | Firebase Auth | Flutter | Netlify | React.js</p>
</div>

<!-- 📁 Project Showcase -->
<div style="max-width:800px;margin:auto;padding:20px;">
  <h3 style="color:#00ffcc;">🌐 Featured Project</h3>
  <a href="https://chemicaladventure.netlify.app/" target="_blank" style="display:block;padding:10px;background:#222;border-radius:8px;color:#00ffd5;text-decoration:none;margin-top:10px;transition:0.3s;">
    🔬 Chemical Adventure → Visit Site
  </a>
</div>

<!-- 💡 Skills Section -->
<div style="max-width:800px;margin:auto;padding:20px;">
  <h3 style="color:#00ffcc;">💼 Skills</h3>
  <div style="display:flex;flex-wrap:wrap;gap:10px;">
    <span style="background:#00ffd5;padding:6px 12px;border-radius:6px;color:#000;">React.js</span>
    <span style="background:#00ffd5;padding:6px 12px;border-radius:6px;color:#000;">Flutter</span>
    <span style="background:#00ffd5;padding:6px 12px;border-radius:6px;color:#000;">Firebase Auth</span>
    <span style="background:#00ffd5;padding:6px 12px;border-radius:6px;color:#000;">Netlify Deploy</span>
    <span style="background:#00ffd5;padding:6px 12px;border-radius:6px;color:#000;">Portfolio Security</span>
  </div>
</div>

<!-- 📞 Contact Section -->
<div style="max-width:800px;margin:auto;padding:20px;">
  <h3 style="color:#00ffcc;">📬 Contact Me</h3>
  <p>Email: <a href="mailto:aminul@example.com" style="color:#00ffd5;">aminul@example.com</a></p>
  <p>LinkedIn: <a href="https://www.linkedin.com/in/aminul-islam-97282b25a" target="_blank" style="color:#00ffd5;">Visit Profile</a></p>
</div>
