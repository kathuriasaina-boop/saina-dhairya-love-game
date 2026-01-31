<!DOCTYPE html><html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Saina & Dhairya – Our Love Adventure</title>
<style>
  body { margin:0; font-family: 'Segoe UI', system-ui, -apple-system; background:#0b0b12; color:#fff; }
  .screen { display:none; min-height:100vh; padding:24px; box-sizing:border-box; }
  .active { display:flex; flex-direction:column; align-items:center; justify-content:center; gap:16px; }
  h1,h2,h3 { margin:8px 0; text-align:center; }
  p { max-width:720px; text-align:center; line-height:1.5; }
  .btns { display:flex; gap:12px; flex-wrap:wrap; justify-content:center; }
  button { background:#ff4d6d; border:none; color:#fff; padding:12px 18px; border-radius:999px; font-size:16px; cursor:pointer; }
  button.secondary { background:#2a2a3a; }
  .card { background:#151524; border-radius:16px; padding:18px; max-width:820px; box-shadow:0 10px 30px rgba(0,0,0,.35); }
  .emoji { font-size:42px; }
  .fade { animation: fade .8s ease; }
  @keyframes fade { from{opacity:0; transform:translateY(8px)} to{opacity:1; transform:none} }
  .cert { border:2px dashed #ff8fa3; padding:22px; border-radius:16px; }
  footer { opacity:.6; font-size:12px; margin-top:12px }
</style>
</head>
<body>
<audio id="bgm" src="tum-ho-toh.mp3" loop autoplay></audio>
<script>
  document.addEventListener('click',()=>{
    const a=document.getElementById('bgm');
    if(a.paused) a.play();
  },{once:true});
</script><!-- START --><section id="start" class="screen active">
  <div class="card fade">
    <div class="emoji">💖</div>
    <h1>Saina & Dhairya</h1>
    <p>"A love story that started long before we knew it would…"</p>
    <p><strong>Background song:</strong> Tum Ho Toh (add your audio file below)</p>
    <div class="btns">
      <button onclick="go('l1')">Open now</button>
      <button class="secondary" onclick="tease()">Open later</button>
    </div>
  </div>
</section><!-- LEVEL 1 --><section id="l1" class="screen">
  <div class="card fade">
    <h2>Level 1: The Beginning 🏫 → 📱</h2>
    <p>We met in school, class 9th. Then came our first Instagram chat.</p>
    <p><strong>Quiz:</strong> Which month did we first talk?</p>
    <div class="btns">
      <button onclick="correct('l2')">December</button>
      <button class="secondary" onclick="wrong()">November</button>
      <button class="secondary" onclick="wrong()">January</button>
    </div>
  </div>
</section><!-- LEVEL 2 --><section id="l2" class="screen">
  <div class="card fade">
    <h2>Level 2: First Date 🍟</h2>
    <p>McDonald’s. Fries shared. Hearts racing.</p>
    <p>What do you do?</p>
    <div class="btns">
      <button onclick="go('l3')">Share the fries 🍟</button>
      <button class="secondary" onclick="go('l3')">Drop a fry 😅</button>
    </div>
    <p>Unlocked: Our first kiss at McDonald’s 💋</p>
  </div>
</section><!-- LEVEL 3 --><section id="l3" class="screen">
  <div class="card fade">
    <h2>Level 3: Photobooth 📸</h2>
    <p>Tap to reveal each photobooth memory.</p>
    <div class="btns">
      <button onclick="tap()">Tap ❤️</button>
      <button class="secondary" onclick="go('l4')">Next</button>
    </div>
  </div>
</section><!-- LEVEL 4 --><section id="l4" class="screen">
  <div class="card fade">
    <h2>Level 4: Love & Challenges 💞</h2>
    <p>We fought. We misunderstood. We never stopped choosing each other.</p>
    <div class="btns">
      <button onclick="go('final')">Apologize & Hug 🤍</button>
      <button class="secondary" onclick="go('final')">Tease & Laugh 😌</button>
    </div>
  </div>
</section><!-- FINAL --><section id="final" class="screen">
  <div class="card fade">
    <h2>Forever Promise 💍</h2>
    <p>"No matter the fights, misunderstandings, or distance…"</p>
    <p><strong>We will love each other forever and get married someday.</strong></p>
    <div class="cert">
      <h3>VIRTUAL MARRIAGE CERTIFICATE</h3>
      <p>This certifies that</p>
      <h3>Saina & Dhairya</h3>
      <p>chose each other through everything.</p>
      <p><strong>Date:</strong> 13 August</p>
      <div class="btns"><button onclick="seal()">Seal with Love ❤️</button></div>
    </div>
    <footer>
  <p>Add your photos/videos/audio by editing this file.</p>
  <video controls style="max-width:100%;border-radius:12px;" src="final-video.mp4"></video>
</footer>
  </div>
</section><script>
  function go(id){ document.querySelectorAll('.screen').forEach(s=>s.classList.remove('active')); document.getElementById(id).classList.add('active'); }
  function wrong(){ alert('Try again 😄'); }
  function correct(next){ alert('Correct! 💌'); go(next); }
  function tease(){ alert('You can’t resist me forever 😏'); }
  function tap(){ alert('Memory unlocked 📸'); }
  function seal(){ alert('Sealed with love ❤️'); }
</script></body>
</html>