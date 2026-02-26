<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>QR App</title>

<script src="https://unpkg.com/html5-qrcode"></script>

<style>
body{
  margin:0;
  font-family:system-ui;
  background:#f2f2f7;
}

/* ЭКРАНЫ */
.screen{
  display:none;
  padding:16px;
  padding-bottom:90px;
}
.screen.active{
  display:block;
}

/* HOME CARD */
.card{
  background:white;
  border-radius:16px;
  padding:16px;
  box-shadow:0 4px 10px rgba(0,0,0,0.08);
  margin-bottom:15px;
}

/* FULLSCREEN SCANNER */
#reader{
  position:fixed;
  inset:0;
  background:black;
  z-index:2000;
}

/* НИЖНЯЯ НАВИГАЦИЯ */
.bottom-nav{
  position:fixed;
  bottom:0;
  left:0;
  right:0;
  height:70px;
  background:white;
  border-top:1px solid #ddd;
  display:flex;
  z-index:1000;
}

.bottom-nav button{
  flex:1;
  border:none;
  background:none;
  font-size:14px;
  color:#666;
}

.bottom-nav button.active{
  color:#007aff;
  font-weight:600;
}
</style>
</head>
<body>

<!-- ================= SCREENS ================= -->

<div id="screen-home" class="screen active">
  <div class="card">
    <h2>🏠 Home</h2>
    <div>Adresse: <b id="address">—</b></div>
    <div>Telefon: <b id="phone">—</b></div>
    <div>Betrag: <b id="amount">—</b></div>
  </div>
</div>

<div id="screen-scanner" class="screen">
  <div id="reader"></div>
</div>

<div id="screen-report" class="screen">
  <div class="card">
    <h2>📊 Bericht</h2>
    <div id="reportText">Noch keine Daten</div>
  </div>
</div>

<!-- ================= NAVIGATION ================= -->

<div class="bottom-nav">
  <button data-screen="scanner">📷<br>Scanner</button>
  <button data-screen="home" class="active">🏠<br>Home</button>
  <button data-screen="report">📊<br>Bericht</button>
</div>

<script>

/* ================= VARIABLES ================= */

let qr = null;
let scannerRunning = false;

const screens = {
  home: document.getElementById("screen-home"),
  scanner: document.getElementById("screen-scanner"),
  report: document.getElementById("screen-report")
};

const navButtons = document.querySelectorAll(".bottom-nav button");

/* ================= NAVIGATION ================= */

function showScreen(name){

  // выключаем камеру если уходим со сканера
  if(name !== "scanner"){
    stopScanner();
  }

  Object.values(screens).forEach(s => s.classList.remove("active"));
  navButtons.forEach(b => b.classList.remove("active"));

  screens[name].classList.add("active");
  document.querySelector(`[data-screen="${name}"]`).classList.add("active");

  if(name === "scanner"){
    startScanner();
  }
}

navButtons.forEach(btn=>{
  btn.onclick = () => showScreen(btn.dataset.screen);
});

// ВСЕГДА стартуем с HOME
showScreen("home");

/* ================= SCANNER ================= */

function startScanner(){
  if(scannerRunning) return;

  qr = new Html5Qrcode("reader");
  scannerRunning = true;

  qr.start(
    { facingMode: "environment" },
    { fps: 10 },
    text => {
      stopScanner();
      parseQR(text);
      showScreen("home");
    }
  );
}

function stopScanner(){
  if(!scannerRunning) return;
  qr.stop().catch(()=>{});
  scannerRunning = false;
}

/* ================= QR PARSE ================= */

function parseQR(text){

  // 🔥 СЮДА ПОТОМ ВСТАВИШЬ СВОЙ СТАРЫЙ parseQR

  document.getElementById("address").textContent = text;
}

</script>

</body>
</html>
