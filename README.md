<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Azzaya — Portfolio V2 Pink Theme</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700&family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
<style>
:root{
  --bg:#FFE6ED; 
  --card:#FFDDE6; 
  --accent:#FF9AA2; 
  --accent2:#FFB3C6; 
  --muted:#7a5a6d; 
  --cream:#111; 
  --glass: rgba(255,255,255,0.3); 
}
*{box-sizing:border-box} 
body{margin:0;font-family:'Poppins',sans-serif;background:var(--bg);color:var(--cream);transition:0.3s;}
.wrapper{max-width:1150px;margin:32px auto;padding:20px;transition:0.3s;}

/* ---------- Hero ---------- */
.hero{
  display: grid;
  grid-template-columns: 1fr 420px;
  gap: 28px;
  align-items: center;
  min-height: 80vh;
  padding: 40px;
  background: linear-gradient(135deg, rgba(255,154,162,0.3), rgba(255,133,150,0.3));
  border-radius: 18px;
  transition: all 0.3s ease;
}
@media(max-width:920px){.hero{grid-template-columns:1fr;}}
.hero-left{padding:28px;background:var(--card);border-radius:18px;border:1px solid rgba(255,255,255,0.2);backdrop-filter:blur(4px);}
.eyebrow{font-weight:600;color:var(--accent2);letter-spacing:2px;font-size:13px}
.title{font-family:'Playfair Display',serif;font-size:clamp(44px,6vw,76px);line-height:0.9;margin:6px 0 10px;color:var(--cream)}
.subtitle{font-size:16px;color:var(--muted);max-width:70%}
.tags{display:flex;gap:8px;margin-top:18px} 
.tag{background:var(--glass);padding:8px 12px;border-radius:999px;font-weight:600;color:var(--accent2);transition:0.3s;}
.hero-right{display:flex;flex-direction:column;gap:12px;align-items:center;position:relative;}

/* --------- DESIGNER Text (Updated) --------- */
.decor-large {
  position: relative;
  margin-top: -60px; 
  font-family: 'Playfair Display', serif;
  font-size: 96px;
  line-height: 0.85;
  color: rgba(255,255,255,0.2);
  pointer-events: none;
  text-align: center;
}

/* Portrait */
.hero-img{width:380px;height:380px;border-radius:16px;background:rgba(255,255,255,0.5);display:flex;align-items:center;justify-content:center;color:var(--muted);transition:0.3s;animation:portraitFade 1s ease forwards;}
@keyframes portraitFade{from{opacity:0;transform:scale(0.95);}to{opacity:1;transform:scale(1);}}

/* ---------- Grid / Cards ---------- */
.grid{display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-top:28px}
@media(max-width:920px){.grid{grid-template-columns:1fr}}
.card{background:var(--card);border-radius:14px;padding:18px;border:1px solid rgba(255,255,255,0.2);box-shadow:0 10px 30px rgba(0,0,0,0.1);transition:0.3s;}
h3{margin:6px 0 12px;font-family:'Playfair Display'} p, li{color:var(--muted);margin:6px 0}

/* Work / Projects */
.work-grid{display:grid;grid-template-columns:1fr 1fr;gap:12px} @media(max-width:520px){.work-grid{grid-template-columns:1fr}}
.work-thumb{border-radius:10px;overflow:hidden;background:var(--card);height:160px;display:flex;align-items:center;justify-content:center;color:var(--muted);cursor:pointer;transition:0.3s;position:relative;}
.work-thumb:hover{transform:scale(1.05);box-shadow:0 10px 20px rgba(0,0,0,0.1);}
.work-thumb span{position:absolute;bottom:8px;left:8px;color:var(--cream);background:var(--accent);padding:4px 8px;border-radius:6px;font-size:13px;opacity:0;transition:0.3s;}
.work-thumb:hover span{opacity:1;}

/* Contact + Comments Grid */
.contact-comments{display:grid;grid-template-columns:1fr 1fr;gap:20px;margin-top:28px;}
@media(max-width:920px){.contact-comments{grid-template-columns:1fr;}}

/* Contact / QR */
.contact-qr{display:grid;grid-template-columns:1fr 120px;gap:16px;align-items:center} 
.qr{width:120px;height:120px;border-radius:10px;background:var(--glass);display:flex;align-items:center;justify-content:center;color:var(--cream)}

/* Comments */
.comments{margin-top:0} 
.comment-box{display:flex;gap:12px;align-items:flex-start}
.comment-avatar{width:44px;height:44px;border-radius:999px;background:var(--accent)}
.comment-text{background:var(--card);padding:10px;border-radius:8px;color:var(--muted);flex:1}

/* Buttons / Mode */
.mode-toggle{display:flex;gap:8px;align-items:center;margin-top:12px}
.btn{background:var(--accent2);padding:8px 12px;border-radius:10px;border:1px solid var(--accent);cursor:pointer;color:var(--cream);transition:0.3s;}
.btn.active{background:var(--accent);border-color:var(--accent);}
.fade{opacity:0;transform:translateY(12px);animation:fadeIn .7s ease forwards}
.fade.delay{animation-delay:0.12s}
@keyframes fadeIn{to{opacity:1;transform:none}}
footer{color:var(--muted);text-align:center;margin:36px 0 12px}
.skill-icon{width:24px;height:24px;margin-right:6px;vertical-align:middle;fill:var(--accent2);transition:0.3s;}
.skill-item:hover .skill-icon{transform:scale(1.2);}
</style>
</head>
<body>
<div class="wrapper">
  <!-- Hero -->
  <header class="hero fade">
    <div class="hero-left">
      <div class="eyebrow">PORTFOLIO • IT</div>
      <div class="title">Azzaya</div>
      <div class="subtitle">I study at Amjilt Cyber School. I explore anything interesting. I always complete what I start and stay committed.</div>
      <div class="tags"><div class="tag">IT</div><div class="tag">Student</div></div>
      <div class="mode-toggle" style="margin-top:20px">
        <button class="btn active" id="inspiredBtn">Inspired</button>
        <button class="btn" id="minimalBtn">Minimal</button>
      </div>
    </div>
    <div class="hero-right">
      <div class="decor-large">DESIGNER</div>
      <div class="hero-img">Portrait</div>
    </div>
  </header>

  <!-- Grid Sections -->
  <section class="grid">
    <!-- About Me -->
    <div class="card fade">
      <h3>About Me</h3>
      <p>I’m an IT student enjoying learning across fields. I follow anything that sparks curiosity. I value discipline and commitment.</p>
      <p><strong>Hobbies:</strong> Air tennis, dancing, drawing, billiards, CS, Valorant, Dota</p>
      <p><strong>Goal:</strong> To build the perfect life and become the best version of myself.</p>
    </div>

    <!-- Skills -->
    <div class="card fade delay">
      <h3>Skills</h3>
      <p><strong>Technical Skills:</strong></p>
      <ul>
        <li class="skill-item">C++</li>
        <li class="skill-item">HTML / CSS</li>
        <li class="skill-item">Python</li>
        <li class="skill-item">Java</li>
      </ul>
      <p><strong>Soft Skills:</strong></p>
      <ul>
        <li class="skill-item">Communication</li>
        <li class="skill-item">Teamwork</li>
        <li class="skill-item">Problem-solving</li>
        <li class="skill-item">Creativity</li>
      </ul>
    </div>

    <!-- Projects -->
    <div class="card fade" style="grid-column:span 2">
      <h3>Projects / Works</h3>
      <div class="work-grid">
        <div class="work-thumb">Project 1 <span>Web Design</span></div>
        <div class="work-thumb">Project 2 <span>UI/UX</span></div>
        <div class="work-thumb">Project 3 <span>Mini App</span></div>
        <div class="work-thumb">Project 4 <span>Poster</span></div>
      </div>
    </div>
  </section>

  <!-- Contact + Comments Side by Side -->
  <section class="contact-comments">
    <!-- Contact Card -->
    <div class="card fade">
      <h3>Contact</h3>
      <p>I’m open to collaboration. Reach out and I’ll create a customized solution for you.</p>
      <div class="contact-qr">
        <div style="display:flex;flex-direction:column;gap:8px;">
          <div style="padding:8px 12px;background:var(--glass);border-radius:10px">Email: alinaal478@gmail.com</div>
          <div style="padding:8px 12px;background:var(--glass);border-radius:10px">Phone: 94246064</div>
          <div style="padding:8px 12px;background:var(--glass);border-radius:10px">GitHub: (Add link)</div>
        </div>
        <div class="qr">QR</div>
      </div>
    </div>

    <!-- Comments Card -->
    <div class="card fade">
      <h3>Comments</h3>
      <div id="comment-list">
        <div class="comment-box"><div class="comment-avatar"></div><div class="comment-text">Welcome! Leave a note or feedback.</div></div>
      </div>
      <div style="margin-top:12px;display:flex;gap:10px;align-items:center">
        <input id="name" placeholder="Your name" style="flex:0 0 180px;padding:10px;border-radius:8px;border:1px solid var(--glass);background:transparent;color:var(--cream)"/>
        <input id="comment" placeholder="Write a comment..." style="flex:1;padding:10px;border-radius:8px;border:1px solid var(--glass);background:transparent;color:var(--cream)"/>
        <button onclick="postComment()" class="btn">Post</button>
      </div>
    </div>
  </section>

  <footer>Designed & coded by Azzaya • V2 Pink Theme</footer>
</div>

<script>
function postComment(){
  const name=document.getElementById('name').value||'Anonymous';
  const text=document.getElementById('comment').value.trim();
  if(!text) return;
  const list=document.getElementById('comment-list');
  const box=document.createElement('div');box.className='comment-box';
  box.innerHTML=`<div class='comment-avatar'></div><div class='comment-text'><strong>${escapeHtml(name)}:</strong> ${escapeHtml(text)}</div>`;
  list.appendChild(box);
  document.getElementById('comment').value='';document.getElementById('name').value='';
  box.scrollIntoView({behavior:'smooth',block:'end'});
}
function escapeHtml(s){return s.replace(/[&<>"']/g, c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":"&#39;"}[c]))}

const inspiredBtn=document.getElementById('inspiredBtn');
const minimalBtn=document.getElementById('minimalBtn');
inspiredBtn.addEventListener('click',()=>{inspiredBtn.classList.add('active'); minimalBtn.classList.remove('active'); document.body.removeAttribute('data-theme');});
minimalBtn.addEventListener('click',()=>{minimalBtn.classList.add('active'); inspiredBtn.classList.remove('active'); document.body.setAttribute('data-theme','minimal');});

document.addEventListener('DOMContentLoaded',()=>{document.querySelectorAll('.fade').forEach((el,i)=>{el.style.animationDelay=(i*0.08)+'s';el.style.animationPlayState='running'})});
</script>
</body>
</html>
