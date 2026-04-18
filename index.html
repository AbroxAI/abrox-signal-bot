<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>ABROX AI Trading Bot</title>
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<script src="https://cdn.tailwindcss.com"></script>
<style>
body { margin:0; background:#000; font-family:-apple-system,BlinkMacSystemFont,"SF Pro Text","SF Pro Display",system-ui,Helvetica,Arial,sans-serif; }
.space-bg { position:relative; background:radial-gradient(circle at top,#0d4f8b 0%,#062a4d 35%,#020b16 75%); overflow:hidden; }
#stars { position:absolute; top:0; left:0; width:100%; height:100%; z-index:0; }
.star { position:absolute; background:#fff; border-radius:50%; }

.icon-box { width:14vw; height:14vw; max-width:64px; max-height:64px; border-radius:14px; display:flex; align-items:center; justify-content:center; font-size:6vw; font-weight:700; box-shadow: inset 0 0 0 1px rgba(255,255,255,0.06), 0 4px 10px rgba(0,0,0,0.4); }
.icon-box.usd { background:linear-gradient(180deg,#134b7a,#0f365e); color:#7dd3fc; }
.icon-box.btc { background:linear-gradient(180deg,#0b233e,#091d33); color:#fff; }

.dropdown-btn { background:linear-gradient(180deg,#1bb6c9,#0ea5b7); color:#fff; font-weight:600; padding:3vw 4vw; border-radius:12px; display:flex; justify-content:space-between; align-items:center; box-shadow:inset 0 0 0 1px rgba(255,255,255,0.12); cursor:pointer; font-size:4vw; border:none; width:100%; }
.dropdown-list { position:absolute; top:calc(100% + 0.5vw); left:0; width:100%; background:#fff; border-radius:12px; overflow-y:auto; max-height:40vh; z-index:50; box-shadow:0 12px 35px rgba(0,0,0,0.45); font-size:4vw; -webkit-overflow-scrolling:touch; scroll-behavior:smooth; overscroll-behavior:contain; scroll-snap-type:y mandatory; }
.dropdown-list div { padding:3vw 4vw; color:#000; font-weight:500; cursor:pointer; scroll-snap-align:center; transition: transform 0.2s, font-size 0.2s, color 0.2s; }
.dropdown-list div.active { transform:scale(1.1); font-size:4.5vw; color:#1bb6c9; }

#startBtn { margin-top:4vw; width:100%; padding:4vw; border-radius:999px; font-weight:700; background:linear-gradient(90deg,#ec4899,#8b5cf6); color:#fff; cursor:pointer; font-size:4vw; border:none; }
.dotAnim { display:inline-block; width:12vw; text-align:left; }

@keyframes pulseScale { 0%,100%{ transform:scale(1); opacity:1; } 50%{ transform:scale(1.1); opacity:0.8; } }
.animate-pulse { animation:pulseScale 1s infinite; }

@keyframes logoGlowPulse { 0%{filter:drop-shadow(0 0 5px #ff5fd2) drop-shadow(0 0 10px #8b5cf6);} 50%{filter:drop-shadow(0 0 15px #ff5fd2) drop-shadow(0 0 25px #8b5cf6);} 100%{filter:drop-shadow(0 0 5px #ff5fd2) drop-shadow(0 0 10px #8b5cf6);} }

.header { display:flex; align-items:center; justify-content:space-between; min-height:100px; padding:0 1rem; position:relative; z-index:10; }
.logo-container { display:flex; align-items:center; justify-content:center; overflow:visible; }
.logo-container img { max-height:100%; max-width:50vw; height:auto; width:auto; display:block; animation:logoGlowPulse 2s infinite ease-in-out; transition: transform 0.3s ease; }
.logo-container:hover img { transform:scale(1.05); }

.lang-switch { transition: opacity 0.2s; }
.lang-switch.hidden { display: none; }

/* Page container: 占满剩余高度，可滚动 */
.page-container {
  position: relative;
  z-index: 10;
  height: calc(100% - 100px);
  overflow-y: auto;
  padding-bottom: 90px;
  box-sizing: border-box;
}

/* 所有页面默认占满高度 */
.page {
  display: none;
  height: 100%;
}
.page.active {
  display: block;
}

/* 信号页背景透明，由父级星空显示 */
#signalsPage {
  background: transparent;
}

/* 其他页面：完全深色背景 */
.dark-premium-bg {
  background: #0a0f1a;
  min-height: 100%;
  height: 100%;
  padding: 20px;
  box-sizing: border-box;
  display: flex;
  flex-direction: column;
}

.placeholder-page {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  flex: 1;
  color: #cbd5e1;
  font-size: 18px;
  font-weight: 500;
  text-align: center;
}

/* Bottom Navigation */
.bottom-nav {
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 80px;
  background: rgba(2, 11, 22, 0.9);
  backdrop-filter: blur(20px);
  border-top: 1px solid rgba(255,255,255,0.08);
  display: flex;
  justify-content: space-around;
  align-items: center;
  padding-bottom: env(safe-area-inset-bottom);
  z-index: 40;
}
.nav-item {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 4px;
  color: #8b9bb5;
  font-size: 11px;
  font-weight: 500;
  cursor: pointer;
  transition: color 0.15s;
}
.nav-item.active { color: #3b82f6; }
.nav-item i { font-size: 22px; }

@media(max-width:420px){ .w-[390px]{width:95vw;} .h-[844px]{height:95vh;} #startBtn{padding:3vw;font-size:4vw;} .dropdown-btn{padding:2.5vw 3vw;font-size:3.5vw;} }
</style>
</head>
<body class="flex justify-center items-center min-h-screen">
<div class="w-[390px] h-[844px] rounded-3xl overflow-hidden relative space-bg text-white">

  <div id="stars"></div>

  <!-- HEADER -->
  <div class="header">
    <div class="logo-container">
      <img id="abroxLogo" src="assets/logo.png" alt="ABROX Logo"/>
    </div>
    <div class="bg-cyan-600 px-3 py-1 rounded-lg text-sm font-medium lang-switch" id="langSwitch">🇺🇸 en</div>
  </div>

  <!-- PAGES CONTAINER -->
  <div class="page-container" id="pageContainer">
    <!-- SIGNALS PAGE -->
    <div id="signalsPage" class="page active">
      <div class="content-wrapper px-6 mt-6">
        <h1 class="text-2xl font-semibold tracking-tight">TRADING BOT</h1>
        <h2 class="text-lg mt-3 font-semibold tracking-tight">SETTINGS</h2>
        <p class="text-sm mt-3 opacity-80 leading-snug">(First select Currency Pair and Timeframe and then click on Start Signals.)</p>

        <div class="flex gap-4 mt-6">
          <div class="icon-box usd"><span>$</span></div>
          <div class="icon-box btc"><span>₿</span></div>
        </div>

        <div class="mt-6 space-y-4 relative">
          <div class="relative">
            <div class="dropdown-btn" onclick="toggleDropdown('currencyList')">Choose Currency <span class="text-sm">▾</span></div>
            <div id="currencyList" class="dropdown-list hidden">
              <div onclick="selectCurrency('USD/JPY')">USD/JPY</div>
              <div onclick="selectCurrency('USD/CHF')">USD/CHF</div>
              <div onclick="selectCurrency('USD/CAD')">USD/CAD</div>
              <div onclick="selectCurrency('GBP/USD')">GBP/USD</div>
              <div onclick="selectCurrency('EUR/USD')">EUR/USD</div>
              <div onclick="selectCurrency('AUD/USD')">AUD/USD</div>
            </div>
          </div>
          <div class="relative">
            <div class="dropdown-btn" onclick="toggleDropdown('timeList')">Timeframe <span class="text-sm">▾</span></div>
            <div id="timeList" class="dropdown-list hidden">
              <div onclick="selectTime('1 Minute')">1 Minute</div>
              <div onclick="selectTime('5 Minutes')">5 Minutes</div>
              <div onclick="selectTime('15 Minutes')">15 Minutes</div>
              <div onclick="selectTime('30 Minutes')">30 Minutes</div>
              <div onclick="selectTime('1 Hour')">1 Hour</div>
            </div>
          </div>
          <button id="startBtn" onclick="startSignals()">Start Signals</button>
          <p id="warn" class="text-red-400 text-xs text-center hidden mt-2">Please select currency and timeframe</p>
        </div>
      </div>
    </div>

    <!-- TRAINING PAGE -->
    <div id="trainingPage" class="page">
      <div class="dark-premium-bg">
        <div class="placeholder-page">
          <div class="text-5xl mb-4">📘</div>
          <h2 class="text-2xl font-bold mb-2 text-white">Training Center</h2>
          <p class="opacity-70">Beginner guides, strategy lessons, and video tutorials.</p>
        </div>
      </div>
    </div>

    <!-- CHAT PAGE -->
    <div id="chatPage" class="page">
      <div class="dark-premium-bg">
        <div class="placeholder-page">
          <div class="text-5xl mb-4">💬</div>
          <h2 class="text-2xl font-bold mb-2 text-white">Community Chat</h2>
          <p class="opacity-70">Connect with pro traders and AI personas.</p>
        </div>
      </div>
    </div>

    <!-- REFERRALS PAGE -->
    <div id="referralsPage" class="page">
      <div class="dark-premium-bg">
        <div class="placeholder-page">
          <div class="text-5xl mb-4">👥</div>
          <h2 class="text-2xl font-bold mb-2 text-white">Refer & Earn</h2>
          <p class="opacity-70">Invite friends and earn up to 20% commission.</p>
        </div>
      </div>
    </div>

    <!-- PROGRESS PAGE -->
    <div id="progressPage" class="page">
      <div class="dark-premium-bg">
        <div class="placeholder-page">
          <div class="text-5xl mb-4">📊</div>
          <h2 class="text-2xl font-bold mb-2 text-white">Your Progress</h2>
          <p class="opacity-70">Track your learning and trading milestones.</p>
        </div>
      </div>
    </div>
  </div>

  <!-- BOTTOM NAVIGATION -->
  <div class="bottom-nav">
    <div class="nav-item active" data-page="signals" onclick="switchPage('signals')">
      <i>📡</i>
      <span>Signals</span>
    </div>
    <div class="nav-item" data-page="training" onclick="switchPage('training')">
      <i>📚</i>
      <span>Training</span>
    </div>
    <div class="nav-item" data-page="chat" onclick="switchPage('chat')">
      <i>💬</i>
      <span>Chat</span>
    </div>
    <div class="nav-item" data-page="referrals" onclick="switchPage('referrals')">
      <i>👥</i>
      <span>Referrals</span>
    </div>
    <div class="nav-item" data-page="progress" onclick="switchPage('progress')">
      <i>📈</i>
      <span>Progress</span>
    </div>
  </div>

</div>

<script>
// Stars background
const starsContainer=document.getElementById("stars");
for(let i=0;i<40;i++){
  const s=document.createElement("div");
  s.className="star";
  s.style.top=(15+Math.random()*85)+"%";
  s.style.left=Math.random()*100+"%";
  s.style.width=s.style.height=(Math.random()*2+1)+"px";
  s.style.opacity=Math.random()*0.7+0.3;
  starsContainer.appendChild(s);
}

// Page switching with language toggle
const langSwitch = document.getElementById('langSwitch');
function switchPage(pageId) {
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.getElementById(pageId + 'Page').classList.add('active');
  document.querySelectorAll('.nav-item').forEach(item => {
    item.classList.toggle('active', item.dataset.page === pageId);
  });
  
  if (pageId === 'signals') {
    langSwitch.classList.remove('hidden');
  } else {
    langSwitch.classList.add('hidden');
  }
}

// Auto scroll to bottom on load
window.addEventListener('load', function() {
  const container = document.getElementById('pageContainer');
  if (container) {
    container.scrollTop = container.scrollHeight;
  }
});

// Original dropdown & signal logic
let currency=null, timeframe=null;

function toggleDropdown(id){ 
  document.getElementById(id).classList.toggle("hidden"); 
}

function selectCurrency(val){ 
  currency=val; 
  document.querySelectorAll('.dropdown-btn')[0].innerHTML = val+' <span class="text-sm">▾</span>'; 
  document.getElementById('currencyList').classList.add("hidden"); 
  highlightOption('currencyList',val); 
}

function selectTime(val){ 
  timeframe=val; 
  document.querySelectorAll('.dropdown-btn')[1].innerHTML = val+' <span class="text-sm">▾</span>'; 
  document.getElementById('timeList').classList.add("hidden"); 
  highlightOption('timeList',val); 
}

function startSignals(){ 
  if(!currency||!timeframe){ 
    document.getElementById("warn").classList.remove("hidden"); 
    return; 
  }
  document.getElementById("warn").classList.add("hidden");
  alert(`Signals started for ${currency} · ${timeframe}`);
}

document.addEventListener('click',e=>{
  if(!e.target.closest('.dropdown-btn')){
    document.getElementById('currencyList').classList.add('hidden');
    document.getElementById('timeList').classList.add('hidden');
  }
});

function highlightOption(listId,value){
  const list = document.getElementById(listId);
  const items = list.querySelectorAll('div');
  items.forEach(i => i.classList.remove('active'));
  const selected = Array.from(items).find(i => i.textContent===value);
  if(selected){
    selected.classList.add('active');
    selected.scrollIntoView({behavior:'smooth', block:'center'});
  }
}
</script>
</body>
</html>
