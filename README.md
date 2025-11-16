# Hermionoon
Test
<!doctype html>
<html lang="th">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Cute Witch — แม่มดน่ารัก</title>
  <style>
    :root{
      --bg:#FFF7FF;
      --card:#fff;
      --accent:#6B21A8;
      --accent-2:#F97316;
      --muted:#6b7280;
      --glass: rgba(255,255,255,0.6);
      font-family: 'Segoe UI', Roboto, 'Noto Sans', system-ui, sans-serif;
    }
    *{box-sizing:border-box}
    body{
      margin:0; min-height:100vh; display:flex; align-items:center; justify-content:center;
      background: linear-gradient(180deg,#FFF7FF 0%, #F0F7FF 100%);
      color:#111;
    }
    .card{
      width:min(820px,94vw); background:var(--card); border-radius:18px; padding:28px;
      box-shadow: 0 10px 30px rgba(107,33,168,0.12); display:grid; grid-template-columns: 310px 1fr; gap:22px; align-items:center;
    }
    .left{
      display:flex; flex-direction:column; gap:14px; align-items:center;
    }
    .portrait{
      width:260px; height:260px; background:linear-gradient(180deg,#FFFAFF,#FFF0FF); border-radius:16px; display:flex; align-items:center; justify-content:center; box-shadow:0 6px 18px rgba(0,0,0,0.06);
    }
    .speech{
      padding:12px 14px; border-radius:12px; background:var(--glass); backdrop-filter: blur(6px); text-align:center; font-size:1rem;
    }
    .controls{display:flex; gap:8px; align-items:center;}
    button{border:0; padding:8px 12px; border-radius:10px; cursor:pointer; font-weight:600}
    .btn-lang{background:transparent; border:1px solid rgba(0,0,0,0.06);} 
    .btn-primary{background:var(--accent); color:white}

    .right{padding:6px 6px 6px 0}
    h1{margin:0 0 6px 0; font-size:1.6rem}
    p.desc{margin:0 0 8px 0; color:var(--muted)}

    .bubble{background:linear-gradient(90deg,#fff,#FFF6FF); border-radius:12px; padding:18px; box-shadow:0 6px 18px rgba(107,33,168,0.06)}
    .traits{display:flex; gap:10px; flex-wrap:wrap; margin-top:12px}
    .tag{display:inline-flex; gap:8px; align-items:center; padding:8px 10px; border-radius:999px; font-weight:600; box-shadow:0 4px 10px rgba(0,0,0,0.04)}

    /* Simple cute SVG styling */
    .svg-witch{width:220px; height:220px}
    .hat-wiggle{transform-origin:center bottom; animation:hat 3s ease-in-out infinite}
    @keyframes hat{0%{transform:rotate(-6deg)}50%{transform:rotate(6deg)}100%{transform:rotate(-6deg)}}
    .wave{animation:wave 1.6s ease-in-out infinite}
    @keyframes wave{0%{transform:translateY(0)}50%{transform:translateY(-6px)}100%{transform:translateY(0)}}

    footer{margin-top:14px; font-size:0.86rem; color:var(--muted)}

    /* responsive */
    @media (max-width:720px){
      .card{grid-template-columns:1fr; padding:18px}
      .portrait{width:200px;height:200px}
    }
  </style>
</head>
<body>
  <main class="card" role="main">
    <section class="left">
      <div class="portrait" aria-hidden="false">
        <!-- Cute witch SVG -->
        <svg class="svg-witch" viewBox="0 0 200 200" xmlns="http://www.w3.org/2000/svg" role="img" aria-label="cute witch illustration">
          <defs>
            <linearGradient id="g1" x1="0" x2="0" y1="0" y2="1">
              <stop offset="0" stop-color="#FFE6FF"/>
              <stop offset="1" stop-color="#FFF0FF"/>
            </linearGradient>
          </defs>
          <!-- hat -->
          <g class="hat-wiggle">
            <path d="M45 55 C55 20,145 20,155 55 C130 45,70 45,45 55 Z" fill="#2D0B4A" stroke="#1b0528"/>
            <rect x="60" y="60" width="80" height="10" rx="5" fill="#4C0E83"/>
          </g>
          <!-- face -->
          <g transform="translate(0,18)">
            <circle cx="100" cy="100" r="46" fill="#FFF0E6" stroke="#FFD9C9"/>
            <!-- eyes -->
            <g transform="translate(0,6)">
              <ellipse cx="85" cy="98" rx="6" ry="8" fill="#2B2B2B"/>
              <ellipse cx="115" cy="98" rx="6" ry="8" fill="#2B2B2B"/>
              <circle cx="85" cy="94" r="2" fill="#fff"/>
              <circle cx="115" cy="94" r="2" fill="#fff"/>
            </g>
            <!-- smile -->
            <path d="M84 122 Q100 134 116 122" stroke="#8B3E2F" stroke-width="3" fill="none" stroke-linecap="round"/>
            <!-- body -->
            <path d="M60 136 C70 160,130 160,140 136 Q100 150 60 136 Z" fill="#7733CC"/>
            <!-- hand with butterbeer -->
            <g class="wave" transform="translate(130,120)">
              <rect x="-6" y="-6" width="38" height="28" rx="6" fill="#FFF4E6" stroke="#E6B267"/>
              <path d="M0 0 q10 -6 20 0" fill="#F3D19A"/>
              <circle cx="24" cy="-8" r="5" fill="#fff" opacity="0.9"/>
            </g>
            <!-- little pet (cute owl) -->
            <g transform="translate(28,133)">
              <ellipse cx="0" cy="0" rx="18" ry="16" fill="#FFE" stroke="#DDBB99"/>
              <circle cx="-6" cy="-2" r="3" fill="#2B2B2B"/>
              <circle cx="6" cy="-2" r="3" fill="#2B2B2B"/>
              <path d="M-4 6 q4 6 8 0" stroke="#A56" stroke-width="2" fill="none"/>
            </g>
          </g>
        </svg>
      </div>

      <div class="speech" id="speech">เป็นแม่มด อยู่ฮอกวอตส์ ชอบกินบัตเตอร์เบียร์ ชอบคริสต์มาส</div>

      <div class="controls">
        <button class="btn-lang" id="btn-th">ภาษาไทย</button>
        <button class="btn-lang" id="btn-en">English</button>
        <button class="btn-primary" id="btn-copy">คัดลอกข้อความ</button>
      </div>
    </section>

    <section class="right">
      <h1 id="title">แม่มดน่ารัก / Cute Witch</h1>
      <p class="desc">หน้าตัวอย่างสำหรับอธิบายตัวละครสั้น ๆ — เหมาะสำหรับใส่ใน GitHub README หรือโปรไฟล์</p>

      <div class="bubble">
        <strong>Traits / ลักษณะเด่น</strong>
        <div class="traits" id="traits">
          <span class="tag">🏰 Hogwarts</span>
          <span class="tag">🍺 Butterbeer</span>
          <span class="tag">🎄 Christmas lover</span>
          <span class="tag">🦉 Cute pet</span>
        </div>

        <div style="margin-top:12px">
          <em>Short bio (English) —</em>
          <p id="bio-en">A happy witch who lives at Hogwarts, loves drinking Butterbeer and celebrating Christmas. Has a cute little pet owl.</p>
          <em>ประวัติสั้น (ภาษาไทย) —</em>
          <p id="bio-th" style="display:none">เป็นแม่มดที่แฮปปี้ อาศัยอยู่ที่ฮอกวอตส์ ชอบดื่มบัตเตอร์เบียร์และชอบฉลองวันคริสต์มาส มีนกฮูกน่ารักเป็นเพื่อน</p>
        </div>

        <footer>ไฟล์นี้เป็น HTML เดียว (single-file). คุณสามารถกด "คัดลอกข้อความ" เพื่อใช้ประโยคไปวางใน README ของ GitHub ได้</footer>
      </div>
    </section>
  </main>

  <script>
    const speech = document.getElementById('speech');
    const bioEn = document.getElementById('bio-en');
    const bioTh = document.getElementById('bio-th');
    const title = document.getElementById('title');
    const traits = document.getElementById('traits');

    const thText = 'เป็นแม่มด อยู่ฮอกวอตส์ ชอบกินบัตเตอร์เบียร์ ชอบคริสต์มาส';
    const enText = "I'm a witch at Hogwarts. I love Butterbeer and Christmas.";
    const enShort = "A happy witch who lives at Hogwarts, loves drinking Butterbeer and celebrating Christmas. Has a cute little pet owl.";
    const thShort = 'เป็นแม่มดที่แฮปปี้ อาศัยอยู่ที่ฮอกวอตส์ ชอบดื่มบัตเตอร์เบียร์และชอบฉลองวันคริสต์มาส มีนกฮูกน่ารักเป็นเพื่อน';

    document.getElementById('btn-th').addEventListener('click', ()=>{
      speech.textContent = thText;
      bioEn.style.display = 'none'; bioTh.style.display = 'block';
      title.textContent = 'แม่มดน่ารัก / Cute Witch';
    });
    document.getElementById('btn-en').addEventListener('click', ()=>{
      speech.textContent = enText;
      bioEn.style.display = 'block'; bioTh.style.display = 'none';
      title.textContent = 'Cute Witch / แม่มดน่ารัก';
    });

    document.getElementById('btn-copy').addEventListener('click', async ()=>{
      try{
        await navigator.clipboard.writeText(speech.textContent);
        const old = document.getElementById('btn-copy').textContent;
        document.getElementById('btn-copy').textContent = 'คัดลอกแล้ว ✓';
        setTimeout(()=> document.getElementById('btn-copy').textContent = old,1200);
      }catch(e){
        alert('ไม่สามารถคัดลอกอัตโนมัติได้ — โปรดคัดลอกด้วยตนเอง');
      }
    });
  </script>
</body>
</html>
