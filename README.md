# crypto.github.io
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>CryptoMarket Pro 2026 — Portal Financiero Cripto y Bolsa</title>
<meta name="description" content="Portal financiero completo: criptomonedas, bolsa, análisis técnico, noticias, calculadoras, portfolio tracker, alertas y herramientas gratuitas.">
<style>
/* ============================================================
   RESET Y VARIABLES
============================================================ */
* { margin:0; padding:0; box-sizing:border-box; }
:root{
  --bg:#0d1117; --bg2:#161b22; --card:#1c2128; --card-hover:#22272e;
  --border:#30363d; --text:#e6edf3; --muted:#8b949e;
  --accent:#2962ff; --accent-light:#58a6ff;
  --green:#26a69a; --green-dark:#1b7a6e; --red:#ef5350; --red-dark:#b71c1c;
  --gold:#f0b90b; --purple:#a371f7; --orange:#ff9800; --pink:#f778ba;
  --shadow:0 4px 24px rgba(0,0,0,.4); --radius:10px;
  --font:'Segoe UI',system-ui,-apple-system,sans-serif;
  --mono:'SF Mono','Fira Code','Consolas',monospace;
  --transition:.2s ease;
}
[data-theme="light"]{
  --bg:#f6f8fa; --bg2:#ffffff; --card:#ffffff; --card-hover:#f0f3f6;
  --border:#d0d7de; --text:#1f2328; --muted:#656d76;
  --shadow:0 4px 24px rgba(0,0,0,.08);
}
html{ scroll-behavior:smooth; }
body{ background:var(--bg); color:var(--text); font-family:var(--font); line-height:1.6; min-height:100vh; transition:background var(--transition),color var(--transition); overflow-x:hidden; padding-bottom:110px; }
a{ color:var(--accent); text-decoration:none; }
a:hover{ color:var(--accent-light); }
img{ max-width:100%; }
button{ font-family:inherit; }
::-webkit-scrollbar{ width:8px; height:8px; }
::-webkit-scrollbar-track{ background:var(--bg2); }
::-webkit-scrollbar-thumb{ background:var(--border); border-radius:4px; }
::-webkit-scrollbar-thumb:hover{ background:var(--muted); }
::selection{ background:var(--accent); color:#fff; }

/* ============================================================
   HEADER
============================================================ */
header{
  background:linear-gradient(135deg,var(--bg2),var(--bg));
  border-bottom:1px solid var(--border);
  padding:12px 20px;
  position:sticky; top:0; z-index:100;
  display:flex; align-items:center; justify-content:space-between; flex-wrap:wrap; gap:10px;
  backdrop-filter:blur(12px);
}
.logo{
  font-size:1.4rem; font-weight:800; cursor:pointer;
  background:linear-gradient(90deg,var(--gold),var(--accent));
  -webkit-background-clip:text; background-clip:text; -webkit-text-fill-color:transparent;
  display:flex; align-items:center; gap:8px;
}
.logo span{ -webkit-text-fill-color:var(--text); font-size:.8rem; font-weight:400; opacity:.7; }
.header-actions{ display:flex; align-items:center; gap:10px; }
.theme-toggle{
  background:var(--card); border:1px solid var(--border); color:var(--text);
  width:38px; height:38px; border-radius:50%; cursor:pointer; font-size:1.1rem;
  display:flex; align-items:center; justify-content:center; transition:var(--transition);
}
.theme-toggle:hover{ background:var(--card-hover); transform:rotate(20deg); }
.ticker-bar{ display:flex; gap:18px; overflow-x:auto; font-size:.82rem; scrollbar-width:none; flex:1; max-width:600px; }
.ticker-bar::-webkit-scrollbar{ display:none; }
.ticker-item{ display:flex; gap:6px; white-space:nowrap; font-family:var(--mono); align-items:center; }
.ticker-item b{ color:var(--muted); font-weight:600; }
.up{ color:var(--green) !important; } .down{ color:var(--red) !important; }

/* ============================================================
   NAV
============================================================ */
nav{ background:var(--bg2); border-bottom:1px solid var(--border); padding:0 8px; overflow-x:auto; scrollbar-width:none; position:sticky; top:63px; z-index:99; }
nav::-webkit-scrollbar{ display:none; }
.nav-inner{ display:flex; gap:2px; max-width:1500px; margin:0 auto; }
.nav-btn{
  background:none; border:none; color:var(--muted); padding:12px 14px; cursor:pointer;
  font-size:.85rem; border-bottom:2px solid transparent; white-space:nowrap; font-weight:500;
  transition:var(--transition);
}
.nav-btn:hover{ color:var(--text); background:rgba(255,255,255,.03); }
.nav-btn.active{ color:var(--accent); border-bottom-color:var(--accent); }

/* ============================================================
   MAIN Y PÁGINAS
============================================================ */
main{ max-width:1500px; margin:0 auto; padding:24px 20px 60px; }
.page{ display:none; animation:fadeIn .35s ease; }
.page.active{ display:block; }
@keyframes fadeIn{ from{opacity:0;transform:translateY(10px);} to{opacity:1;transform:none;} }
h1{ font-size:1.7rem; margin-bottom:4px; font-weight:800; letter-spacing:-.5px; }
h2{ font-size:1.25rem; margin:28px 0 14px; font-weight:700; }
h3{ font-size:1.05rem; margin-bottom:10px; font-weight:600; }
.subtitle{ color:var(--muted); margin-bottom:22px; font-size:.92rem; }

/* ============================================================
   GRIDS Y CARDS
============================================================ */
.grid{ display:grid; gap:16px; }
.grid-4{ grid-template-columns:repeat(auto-fit,minmax(220px,1fr)); }
.grid-3{ grid-template-columns:repeat(auto-fit,minmax(280px,1fr)); }
.grid-2{ grid-template-columns:repeat(auto-fit,minmax(340px,1fr)); }
.card{
  background:var(--card); border:1px solid var(--border); border-radius:var(--radius);
  padding:18px; transition:var(--transition);
}
.card:hover{ border-color:var(--muted); box-shadow:var(--shadow); }
.card-title{ font-size:.78rem; color:var(--muted); text-transform:uppercase; letter-spacing:.8px; margin-bottom:8px; font-weight:600; }
.price{ font-size:1.6rem; font-weight:800; font-family:var(--mono); letter-spacing:-1px; }
.change{ font-size:.9rem; font-weight:600; }
.mono{ font-family:var(--mono); }

/* ============================================================
   TABLAS
============================================================ */
.table-wrap{ overflow-x:auto; border-radius:var(--radius); }
table{ width:100%; border-collapse:collapse; font-size:.88rem; }
th{
  text-align:left; padding:11px 10px; color:var(--muted); font-size:.74rem;
  text-transform:uppercase; border-bottom:1px solid var(--border); font-weight:700;
  letter-spacing:.5px; position:sticky; top:0; background:var(--card); z-index:2;
}
td{ padding:11px 10px; border-bottom:1px solid var(--border); vertical-align:middle; }
tr:hover td{ background:rgba(255,255,255,.02); }
.coin-cell{ display:flex; align-items:center; gap:10px; }
.coin-cell img{ width:26px; height:26px; border-radius:50%; }
.coin-cell .sym{ color:var(--muted); font-size:.78rem; text-transform:uppercase; }

/* ============================================================
   WIDGETS TRADINGVIEW
============================================================ */
.tv-container{ background:var(--card); border-radius:var(--radius); overflow:hidden; border:1px solid var(--border); min-height:420px; }
.tv-container .tradingview-widget-container,
.tv-container .tradingview-widget-container__widget{ width:100% !important; }
.tv-container iframe{ width:100% !important; }

/* ============================================================
   FORMULARIOS
============================================================ */
input, select, textarea{
  background:var(--bg2); border:1px solid var(--border); color:var(--text);
  padding:10px 12px; border-radius:8px; font-size:.92rem; outline:none;
  width:100%; margin-bottom:12px; transition:var(--transition);
}
input:focus, select:focus, textarea:focus{ border-color:var(--accent); box-shadow:0 0 0 3px rgba(41,98,255,.15); }
input::placeholder{ color:var(--muted); }
button.action{
  background:var(--accent); border:none; color:#fff; cursor:pointer;
  padding:11px 18px; border-radius:8px; font-size:.92rem; font-weight:600;
  width:100%; margin-bottom:10px; transition:var(--transition);
}
button.action:hover{ background:var(--accent-light); transform:translateY(-1px); }
button.action:active{ transform:none; }
button.secondary{ background:var(--bg2); border:1px solid var(--border); color:var(--text); }
button.secondary:hover{ background:var(--card-hover); }
button.danger{ background:var(--red); }
button.danger:hover{ background:var(--red-dark); }
button.success{ background:var(--green); }
button.small{ width:auto; padding:6px 12px; font-size:.8rem; margin:0; }
label{ display:block; font-size:.8rem; color:var(--muted); margin-bottom:5px; margin-top:10px; font-weight:600; }
.form-row{ display:grid; grid-template-columns:1fr 1fr; gap:12px; }
@media(max-width:500px){ .form-row{ grid-template-columns:1fr; } }

/* ============================================================
   BADGES
============================================================ */
.badge{
  display:inline-block; padding:3px 9px; border-radius:20px;
  font-size:.7rem; font-weight:700; text-transform:uppercase; letter-spacing:.3px;
}
.badge-green{ background:rgba(38,166,154,.18); color:var(--green); }
.badge-red{ background:rgba(239,83,80,.18); color:var(--red); }
.badge-blue{ background:rgba(41,98,255,.18); color:var(--accent-light); }
.badge-gold{ background:rgba(240,185,11,.18); color:var(--gold); }
.badge-purple{ background:rgba(163,113,247,.18); color:var(--purple); }

/* ============================================================
   NOTICIAS
============================================================ */
.news-item{ padding:16px 0; border-bottom:1px solid var(--border); }
.news-item:last-child{ border:none; }
.news-item h4{ font-size:1rem; margin-bottom:5px; line-height:1.4; }
.news-item p{ color:var(--muted); font-size:.86rem; }
.news-item .meta{ font-size:.75rem; color:var(--muted); margin-top:6px; display:flex; gap:12px; }

/* ============================================================
   UTILIDADES
============================================================ */
.loading{ color:var(--muted); padding:24px; text-align:center; font-size:.9rem; }
.profit{ color:var(--green) !important; font-weight:700; }
.loss{ color:var(--red) !important; font-weight:700; }
.info-box{ background:rgba(41,98,255,.08); border-left:3px solid var(--accent); padding:13px 16px; border-radius:8px; margin:16px 0; font-size:.87rem; }
.warn-box{ background:rgba(240,185,11,.08); border-left:3px solid var(--gold); padding:13px 16px; border-radius:8px; margin:16px 0; font-size:.87rem; }
.success-box{ background:rgba(38,166,154,.08); border-left:3px solid var(--green); padding:13px 16px; border-radius:8px; margin:16px 0; font-size:.87rem; }
.text-center{ text-align:center; }
.flex-between{ display:flex; justify-content:space-between; align-items:center; }
.hidden{ display:none !important; }

/* ============================================================
   BOTÓN COPIAR FLOTANTE (subido para no chocar con el banner)
============================================================ */
.copy-fab{
  position:fixed; bottom:130px; right:24px;
  background:linear-gradient(135deg,var(--gold),var(--orange));
  color:#000; border:none; padding:14px 22px; border-radius:50px;
  font-weight:800; cursor:pointer; box-shadow:0 4px 24px rgba(240,185,11,.5);
  z-index:999; display:flex; align-items:center; gap:8px;
  transition:var(--transition); font-size:.9rem;
}
.copy-fab:hover{ transform:translateY(-3px) scale(1.02); box-shadow:0 8px 32px rgba(240,185,11,.7); }

/* TOAST */
.toast{
  position:fixed; bottom:190px; right:24px;
  background:var(--green); color:#fff; padding:13px 22px;
  border-radius:10px; font-weight:700; z-index:1000;
  opacity:0; transform:translateY(20px); transition:.3s; pointer-events:none;
  box-shadow:0 8px 32px rgba(0,0,0,.4);
}
.toast.show{ opacity:1; transform:none; }
.toast.error{ background:var(--red); }

/* ============================================================
   FOOTER
============================================================ */
footer{
  text-align:center; padding:36px 20px; color:var(--muted);
  font-size:.82rem; border-top:1px solid var(--border); margin-top:40px;
  line-height:1.8;
}

/* ============================================================
   RESPONSIVE
============================================================ */
@media(max-width:768px){
  header{ padding:10px 14px; }
  .ticker-bar{ max-width:100%; order:3; flex-basis:100%; }
  main{ padding:18px 12px 50px; }
  h1{ font-size:1.4rem; }
  .price{ font-size:1.2rem; }
  .grid-4{ grid-template-columns:repeat(2,1fr); }
  .nav-btn{ padding:10px 10px; font-size:.78rem; }
}
@media(max-width:480px){
  .grid-4{ grid-template-columns:1fr; }
  .copy-fab{ bottom:120px; right:16px; padding:12px 16px; font-size:.8rem; }
  .toast{ bottom:180px; right:16px; }
}
</style>
</head>
<body>

<!-- ============================================================
     HEADER
============================================================ -->
<header>
  <div class="logo" onclick="go('dashboard')">CryptoMarket Pro <span>2026</span></div>
  <div class="ticker-bar" id="tickerBar"><span class="loading">Cargando precios...</span></div>
  <div class="header-actions">
    <button class="theme-toggle" onclick="toggleTheme()" title="Cambiar tema" id="themeBtn">🌙</button>
  </div>
</header>

<!-- ============================================================
     NAVEGACIÓN
============================================================ -->
<nav><div class="nav-inner" id="navBar"></div></nav>

<main id="app">

<!-- ============================================================
     PÁGINA 1: DASHBOARD
============================================================ -->
<section class="page active" id="page-dashboard">
  <h1>📊 Dashboard General</h1>
  <p class="subtitle">Vista panorámica del mercado en tiempo real · CoinGecko & TradingView</p>
  <div class="grid grid-4" id="topCoins"><div class="loading">Cargando precios...</div></div>

  <div class="grid grid-2" style="margin-top:16px;">
    <div class="card" id="fearGreedCard">
      <div class="card-title">😱 Índice Miedo y Codicia</div>
      <div id="fearGreed"><div class="loading">Cargando...</div></div>
    </div>
    <div class="card" id="dominanceCard">
      <div class="card-title">👑 Dominancia de Bitcoin</div>
      <div id="dominance"><div class="loading">Cargando...</div></div>
    </div>
  </div>

  <h2>📈 Bitcoin en Vivo</h2>
  <div class="tv-container"><div id="tv_dashboard" style="height:420px;"></div></div>

  <h2>🔥 Tendencias del Mercado</h2>
  <div class="card" id="trending"><div class="loading">Cargando tendencias...</div></div>

  <h2>🗺️ Mapa de Calor del Mercado</h2>
  <div class="tv-container"><div id="tv_heatmap" style="height:500px;"></div></div>
</section>

<!-- ============================================================
     PÁGINA 2: CRIPTOMONEDAS
============================================================ -->
<section class="page" id="page-crypto">
  <h1>🪙 Mercado Cripto</h1>
  <p class="subtitle">Top 50 criptomonedas por capitalización · Datos actualizados automáticamente</p>
  <div class="flex-between" style="margin-bottom:14px;flex-wrap:wrap;gap:10px;">
    <input type="text" id="cryptoSearch" placeholder="🔍 Buscar criptomoneda..." style="max-width:300px;margin:0;" oninput="filterCryptoTable()">
    <div class="badge badge-green" id="lastUpdate">Actualizado ahora</div>
  </div>
  <div class="card"><div class="table-wrap">
    <table id="cryptoTable">
      <thead><tr><th>#</th><th>Moneda</th><th>Precio</th><th>24h</th><th>7d</th><th>Cap. Mercado</th><th>Volumen 24h</th><th>Acciones</th></tr></thead>
      <tbody><tr><td colspan="8" class="loading">Cargando datos...</td></tr></tbody>
    </table>
  </div></div>
  <h2>📊 Gráfico BTC/USDT</h2>
  <div class="tv-container"><div id="tv_crypto" style="height:520px;"></div></div>
</section>

<!-- ============================================================
     PÁGINA 3: BOLSA
============================================================ -->
<section class="page" id="page-stocks">
  <h1>📈 Mercado de Valores</h1>
  <p class="subtitle">Acciones, ETFs e índices · Screener profesional de TradingView</p>
  <div class="tv-container"><div id="tv_stocks" style="height:600px;"></div></div>
  <h2>🇺🇸 S&P 500 en Vivo</h2>
  <div class="tv-container"><div id="tv_sp500" style="height:420px;"></div></div>
  <h2>🏆 Principales Índices</h2>
  <div class="grid grid-3" id="indexCards"></div>
</section>

<!-- ============================================================
     PÁGINA 4: ANÁLISIS TÉCNICO
============================================================ -->
<section class="page" id="page-analysis">
  <h1>📉 Análisis Técnico Profesional</h1>
  <p class="subtitle">Gráficos interactivos con más de 100 indicadores y herramientas de dibujo</p>
  <div class="card" style="margin-bottom:16px;">
    <label>Selecciona el activo</label>
    <select id="analysisSymbol" onchange="loadAnalysisChart()">
      <optgroup label="Criptomonedas">
        <option value="BINANCE:BTCUSDT">Bitcoin (BTC/USDT)</option>
        <option value="BINANCE:ETHUSDT">Ethereum (ETH/USDT)</option>
        <option value="BINANCE:SOLUSDT">Solana (SOL/USDT)</option>
        <option value="BINANCE:BNBUSDT">BNB (BNB/USDT)</option>
        <option value="BINANCE:XRPUSDT">XRP (XRP/USDT)</option>
        <option value="BINANCE:DOGEUSDT">Dogecoin (DOGE/USDT)</option>
      </optgroup>
      <optgroup label="Bolsa USA">
        <option value="NASDAQ:AAPL">Apple (AAPL)</option>
        <option value="NASDAQ:TSLA">Tesla (TSLA)</option>
        <option value="NASDAQ:NVDA">NVIDIA (NVDA)</option>
        <option value="NASDAQ:MSFT">Microsoft (MSFT)</option>
        <option value="NASDAQ:AMZN">Amazon (AMZN)</option>
      </optgroup>
      <optgroup label="Índices y Materias Primas">
        <option value="SP:SPX">S&P 500</option>
        <option value="TVC:GOLD">Oro</option>
        <option value="TVC:SILVER">Plata</option>
        <option value="NYMEX:CL1!">Petróleo WTI</option>
      </optgroup>
    </select>
  </div>
  <div class="tv-container"><div id="tv_analysis" style="height:620px;"></div></div>
  <div class="info-box">💡 <b>Consejo:</b> 1h y 4h para trading intradía, 1D/1W para análisis de tendencia macro.</div>
  <h2>📋 Watchlist Personal</h2>
  <div class="card" id="watchlistBox"><div class="loading">Añade activos desde la tabla de cripto.</div></div>
</section>

<!-- ============================================================
     PÁGINA 5: NOTICIAS
============================================================ -->
<section class="page" id="page-news">
  <h1>📰 Noticias y Análisis</h1>
  <p class="subtitle">Últimas noticias del mercado cripto y financiero global</p>
  <div class="grid grid-2">
    <div class="card" id="newsList"><div class="loading">Cargando noticias...</div></div>
    <div class="card">
      <h3>📡 Timeline en Vivo</h3>
      <div class="tv-container"><div id="tv_news" style="height:600px;"></div></div>
    </div>
  </div>
</section>

<!-- ============================================================
     PÁGINA 6: CALENDARIO ECONÓMICO
============================================================ -->
<section class="page" id="page-calendar">
  <h1>📅 Calendario Económico</h1>
  <p class="subtitle">Eventos macroeconómicos que mueven los mercados globales</p>
  <div class="tv-container"><div id="tv_calendar" style="height:680px;"></div></div>
  <div class="warn-box">⚠️ Los eventos de alto impacto (rojo) suelen generar alta volatilidad.</div>
</section>

<!-- ============================================================
     PÁGINA 7: GUÍAS Y EDUCACIÓN
============================================================ -->
<section class="page" id="page-guides">
  <h1>📚 Guías y Educación Financiera</h1>
  <p class="subtitle">Aprende desde cero hasta nivel avanzado</p>
  <div class="grid grid-3" id="guidesGrid"></div>
  <h2>🎓 Glosario de Términos</h2>
  <div class="card" id="glossaryBox"></div>
</section>

<!-- ============================================================
     PÁGINA 8: EXCHANGES
============================================================ -->
<section class="page" id="page-exchanges">
  <h1>🏦 Comparativa de Exchanges</h1>
  <p class="subtitle">Los mejores exchanges para operar · Enlaces de afiliado</p>
  <div class="warn-box">💡 Sustituye los enlaces por tus códigos de afiliado reales.</div>
  <div class="grid grid-3" id="exchangeGrid"></div>
  <h2>📊 Tabla Comparativa</h2>
  <div class="card"><div class="table-wrap">
    <table id="exchangeTable">
      <thead><tr><th>Exchange</th><th>Comisión Maker</th><th>Comisión Taker</th><th>Más de 100 criptos</th><th>Regulación</th><th>Valoración</th></tr></thead>
      <tbody></tbody>
    </table>
  </div></div>
</section>

<!-- ============================================================
     PÁGINA 9: CALCULADORA DE IMPUESTOS
============================================================ -->
<section class="page" id="page-tax">
  <h1>🧮 Calculadora de Impuestos Cripto</h1>
  <p class="subtitle">Estima tus ganancias patrimoniales (España, simplificado 2024-2026)</p>
  <div class="grid grid-2">
    <div class="card">
      <h3>Datos de la operación</h3>
      <label>Precio de compra (€)</label>
      <input type="number" id="taxBuy" placeholder="Ej: 10000" step="0.01">
      <label>Precio de venta (€)</label>
      <input type="number" id="taxSell" placeholder="Ej: 25000" step="0.01">
      <label>Comisiones totales (€)</label>
      <input type="number" id="taxFees" placeholder="Ej: 200" step="0.01" value="0">
      <label>Método de cálculo</label>
      <select id="taxMethod">
        <option value="fifo">FIFO (First In, First Out)</option>
        <option value="lifo">LIFO (Last In, First Out)</option>
        <option value="average">Coste medio ponderado</option>
      </select>
      <button class="action" onclick="calcTax()">Calcular Impuestos</button>
    </div>
    <div class="card">
      <h3>Resultado</h3>
      <div id="taxResult"><p class="loading">Introduce los datos y pulsa calcular.</p></div>
    </div>
  </div>
  <div class="info-box">ℹ️ Cálculo orientativo con tramos del ahorro en España. Consulta con un asesor fiscal.</div>
</section>

<!-- ============================================================
     PÁGINA 10: PORTFOLIO TRACKER
============================================================ -->
<section class="page" id="page-portfolio">
  <h1>💼 Portfolio Tracker</h1>
  <p class="subtitle">Sigue tu cartera de criptomonedas · Datos guardados en tu navegador</p>
  <div class="grid grid-2">
    <div class="card">
      <h3>Añadir transacción</h3>
      <label>Criptomoneda</label>
      <select id="pfCoin">
        <option value="bitcoin">Bitcoin (BTC)</option>
        <option value="ethereum">Ethereum (ETH)</option>
        <option value="solana">Solana (SOL)</option>
        <option value="binancecoin">BNB</option>
        <option value="ripple">XRP</option>
        <option value="cardano">Cardano (ADA)</option>
        <option value="dogecoin">Dogecoin (DOGE)</option>
        <option value="polkadot">Polkadot (DOT)</option>
        <option value="chainlink">Chainlink (LINK)</option>
        <option value="avalanche-2">Avalanche (AVAX)</option>
      </select>
      <label>Cantidad</label>
      <input type="number" id="pfAmount" placeholder="Ej: 0.5" step="0.00000001">
      <label>Precio de compra (USD)</label>
      <input type="number" id="pfBuyPrice" placeholder="Ej: 40000" step="0.01">
      <button class="action" onclick="addPosition()">Añadir al Portfolio</button>
      <button class="action secondary" onclick="clearPortfolio()">Vaciar Portfolio</button>
    </div>
    <div class="card">
      <h3>Resumen de la Cartera</h3>
      <div id="pfSummary"><div class="loading">Sin posiciones</div></div>
      <div style="margin-top:16px;max-width:280px;margin-left:auto;margin-right:auto;"><canvas id="pfChart"></canvas></div>
    </div>
  </div>
  <h2>Posiciones Abiertas</h2>
  <div class="card"><div class="table-wrap">
    <table id="pfTable">
      <thead><tr><th>Moneda</th><th>Cantidad</th><th>Compra</th><th>Actual</th><th>Valor</th><th>P&L</th><th></th></tr></thead>
      <tbody><tr><td colspan="7" class="loading">Portfolio vacío</td></tr></tbody>
    </table>
  </div></div>
</section>

<!-- ============================================================
     PÁGINA 11: HERRAMIENTAS
============================================================ -->
<section class="page" id="page-tools">
  <h1>🛠️ Herramientas y Calculadoras</h1>
  <p class="subtitle">Utilidades gratuitas para traders e inversores</p>

  <div class="card" style="margin-bottom:18px;">
    <h3>💱 Conversor de Criptomonedas</h3>
    <div class="grid grid-3">
      <div><label>Cantidad</label><input type="number" id="convAmount" value="1" step="0.0001"></div>
      <div><label>Desde</label><select id="convFrom" onchange="convertCurrency()"><option value="bitcoin">BTC</option><option value="ethereum">ETH</option><option value="solana">SOL</option><option value="usd">USD</option><option value="eur">EUR</option></select></div>
      <div><label>Hacia</label><select id="convTo" onchange="convertCurrency()"><option value="usd">USD</option><option value="eur">EUR</option><option value="bitcoin">BTC</option><option value="ethereum">ETH</option><option value="solana">SOL</option></select></div>
    </div>
    <button class="action" onclick="convertCurrency()">Convertir</button>
    <div id="convResult" style="text-align:center;font-size:1.3rem;font-weight:700;padding:12px;"></div>
  </div>

  <div class="card" style="margin-bottom:18px;">
    <h3>📆 Calculadora DCA (Dollar Cost Averaging)</h3>
    <p style="color:var(--muted);font-size:.85rem;margin-bottom:12px;">Simula invertir una cantidad fija periódicamente.</p>
    <div class="grid grid-2">
      <div>
        <label>Importe por compra (USD)</label>
        <input type="number" id="dcaAmount" value="100" step="1">
        <label>Frecuencia</label>
        <select id="dcaFreq"><option value="7">Semanal</option><option value="30">Mensual</option></select>
        <label>Número de compras</label>
        <input type="number" id="dcaPeriods" value="52" step="1">
      </div>
      <div>
        <label>Criptomoneda</label>
        <select id="dcaCoin"><option value="bitcoin">Bitcoin (BTC)</option><option value="ethereum">Ethereum (ETH)</option><option value="solana">Solana (SOL)</option></select>
        <button class="action" onclick="calcDCA()" style="margin-top:20px;">Simular DCA</button>
      </div>
    </div>
    <div id="dcaResult"></div>
  </div>

  <div class="card" style="margin-bottom:18px;">
    <h3>⚠️ Calculadora de Gestión de Riesgo</h3>
    <div class="grid grid-2">
      <div>
        <label>Capital total (USD)</label>
        <input type="number" id="riskCapital" value="10000" step="1">
        <label>Riesgo por operación (%)</label>
        <input type="number" id="riskPercent" value="2" step="0.1">
        <label>Precio de entrada</label>
        <input type="number" id="riskEntry" value="50000" step="0.01">
        <label>Stop Loss</label>
        <input type="number" id="riskStop" value="48000" step="0.01">
      </div>
      <div>
        <button class="action" onclick="calcRisk()" style="margin-top:28px;">Calcular Posición</button>
        <div id="riskResult"></div>
      </div>
    </div>
  </div>

  <div class="card">
    <h3>📈 Calculadora de Rentabilidad</h3>
    <div class="grid grid-2">
      <div>
        <label>Inversión inicial (USD)</label>
        <input type="number" id="roiInvest" value="1000" step="1">
        <label>Valor final (USD)</label>
        <input type="number" id="roiFinal" value="2500" step="1">
        <label>Años</label>
        <input type="number" id="roiYears" value="2" step="0.5">
      </div>
      <div>
        <button class="action" onclick="calcROI()" style="margin-top:20px;">Calcular ROI</button>
        <div id="roiResult"></div>
      </div>
    </div>
  </div>
</section>

<!-- ============================================================
     PÁGINA 12: ALERTAS
============================================================ -->
<section class="page" id="page-alerts">
  <h1>🔔 Alertas de Precios</h1>
  <p class="subtitle">Configura alertas · Se comprueban cada 30 segundos mientras la web esté abierta</p>
  <div class="grid grid-2">
    <div class="card">
      <h3>Crear alerta</h3>
      <label>Criptomoneda</label>
      <select id="alertCoin">
        <option value="bitcoin">Bitcoin (BTC)</option>
        <option value="ethereum">Ethereum (ETH)</option>
        <option value="solana">Solana (SOL)</option>
        <option value="binancecoin">BNB</option>
        <option value="ripple">XRP</option>
      </select>
      <label>Condición</label>
      <select id="alertCondition"><option value="above">Precio POR ENCIMA de</option><option value="below">Precio POR DEBAJO de</option></select>
      <label>Precio objetivo (USD)</label>
      <input type="number" id="alertPrice" placeholder="Ej: 100000" step="0.01">
      <button class="action" onclick="addAlert()">Crear Alerta</button>
    </div>
    <div class="card">
      <h3>Alertas activas</h3>
      <div id="alertList"><div class="loading">No hay alertas configuradas.</div></div>
    </div>
  </div>
</section>

<!-- ============================================================
     PÁGINA 13: COMPARADOR
============================================================ -->
<section class="page" id="page-compare">
  <h1>⚖️ Comparador de Criptomonedas</h1>
  <p class="subtitle">Compara dos activos cara a cara</p>
  <div class="grid grid-2">
    <div class="card">
      <label>Criptomoneda A</label>
      <select id="compareA"><option value="bitcoin">Bitcoin</option><option value="ethereum">Ethereum</option><option value="solana">Solana</option><option value="cardano">Cardano</option><option value="polkadot">Polkadot</option></select>
    </div>
    <div class="card">
      <label>Criptomoneda B</label>
      <select id="compareB"><option value="ethereum">Ethereum</option><option value="bitcoin">Bitcoin</option><option value="solana">Solana</option><option value="chainlink">Chainlink</option><option value="avalanche-2">Avalanche</option></select>
    </div>
  </div>
  <button class="action" onclick="compareCoins()" style="max-width:300px;">Comparar</button>
  <div class="card" id="compareResult" style="margin-top:16px;"><div class="loading">Selecciona dos activos y pulsa comparar.</div></div>
</section>

<!-- ============================================================
     PÁGINA 14: DEFI
============================================================ -->
<section class="page" id="page-defi">
  <h1>⛓️ On-Chain & DeFi</h1>
  <p class="subtitle">Datos de protocolos DeFi y métricas on-chain (DeFiLlama)</p>
  <div class="grid grid-3" id="defiCards"><div class="loading">Cargando datos DeFi...</div></div>
  <h2>🏦 Top Protocolos DeFi por TVL</h2>
  <div class="card"><div class="table-wrap">
    <table id="defiTable">
      <thead><tr><th>#</th><th>Protocolo</th><th>Cadena</th><th>TVL</th><th>Cambio 1d</th></tr></thead>
      <tbody><tr><td colspan="5" class="loading">Cargando...</td></tr></tbody>
    </table>
  </div></div>
</section>

</main>

<button class="copy-fab" onclick="copyAllCode()">📋 Copiar Código</button>
<div class="toast" id="toast">¡Copiado!</div>

<footer>
  ⚠️ <b>Aviso legal:</b> Herramienta educativa. No constituye asesoramiento financiero. Invierte con responsabilidad.<br>
  © 2026 CryptoMarket Pro · Datos: CoinGecko, TradingView, Alternative.me, DeFiLlama<br>
  <span style="font-size:.75rem;">Hecho con ❤️ para la comunidad cripto hispanohablante</span>
</footer>

<script src="https://cdn.jsdelivr.net/npm/chart.js@4.4.0/dist/chart.umd.min.js"></script>
<script>
/* ============================================================
   CONFIGURACIÓN GLOBAL
============================================================ */
const API = {
  coingecko: 'https://api.coingecko.com/api/v3',
  alternative: 'https://api.alternative.me',
  defillama: 'https://api.llama.fi'
};
const state = {
  cryptoData: [],
  watchlist: JSON.parse(localStorage.getItem('watchlist') || '[]'),
  alerts: JSON.parse(localStorage.getItem('priceAlerts') || '[]'),
  portfolio: JSON.parse(localStorage.getItem('cryptoPortfolio') || '[]'),
  theme: localStorage.getItem('theme') || 'dark'
};
let pfChartInstance = null;

/* ============================================================
   NAVEGACIÓN SPA
============================================================ */
const pages = [
  {id:'dashboard', label:'🏠 Dashboard'},
  {id:'crypto', label:'🪙 Cripto'},
  {id:'stocks', label:'📈 Bolsa'},
  {id:'analysis', label:'📉 Análisis'},
  {id:'news', label:'📰 Noticias'},
  {id:'calendar', label:'📅 Calendario'},
  {id:'guides', label:'📚 Guías'},
  {id:'exchanges', label:'🏦 Exchanges'},
  {id:'tax', label:'🧮 Impuestos'},
  {id:'portfolio', label:'💼 Portfolio'},
  {id:'tools', label:'🛠️ Herramientas'},
  {id:'alerts', label:'🔔 Alertas'},
  {id:'compare', label:'⚖️ Comparar'},
  {id:'defi', label:'⛓️ DeFi'}
];

function buildNav(){
  const nav = document.getElementById('navBar');
  nav.innerHTML = '';
  pages.forEach(p => {
    const btn = document.createElement('button');
    btn.className = 'nav-btn';
    btn.textContent = p.label;
    btn.dataset.page = p.id;
    btn.onclick = () => go(p.id);
    nav.appendChild(btn);
  });
}

function go(id){
  document.querySelectorAll('.page').forEach(p => p.classList.remove('active'));
  document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
  document.getElementById('page-' + id).classList.add('active');
  const btn = document.querySelector(`.nav-btn[data-page="${id}"]`);
  if(btn) btn.classList.add('active');
  window.scrollTo({top:0, behavior:'smooth'});
  if(id === 'dashboard'){ loadDashboardChart(); loadHeatmap(); }
  if(id === 'crypto'){ loadCryptoChart(); }
  if(id === 'stocks'){ loadStocksWidget(); loadIndexCards(); }
  if(id === 'analysis'){ loadAnalysisChart(); renderWatchlist(); }
  if(id === 'news'){ loadNewsWidget(); }
  if(id === 'calendar'){ loadCalendarWidget(); }
  if(id === 'defi'){ loadDefiData(); }
}

/* ============================================================
   TEMA CLARO / OSCURO
============================================================ */
function toggleTheme(){
  state.theme = state.theme === 'dark' ? 'light' : 'dark';
  document.documentElement.setAttribute('data-theme', state.theme === 'light' ? 'light' : '');
  document.getElementById('themeBtn').textContent = state.theme === 'dark' ? '🌙' : '☀️';
  localStorage.setItem('theme', state.theme);
  ['tv_dashboard','tv_crypto','tv_stocks','tv_sp500','tv_analysis','tv_news','tv_calendar','tv_heatmap'].forEach(id => {
    const el = document.getElementById(id);
    if(el){ el.dataset.loaded = ''; el.innerHTML = ''; }
  });
  const activePage = document.querySelector('.page.active').id.replace('page-','');
  if(activePage === 'dashboard'){ loadDashboardChart(); loadHeatmap(); }
  if(activePage === 'crypto') loadCryptoChart();
  if(activePage === 'stocks') loadStocksWidget();
  if(activePage === 'analysis') loadAnalysisChart();
  if(activePage === 'news') loadNewsWidget();
  if(activePage === 'calendar') loadCalendarWidget();
  if(pfChartInstance) renderPortfolio();
}

if(state.theme === 'light'){
  document.documentElement.setAttribute('data-theme', 'light');
  document.getElementById('themeBtn').textContent = '☀️';
}

/* ============================================================
   UTILIDADES
============================================================ */
function fmt(n){
  if(n === null || n === undefined) return '—';
  if(Math.abs(n) >= 1000) return n.toLocaleString('en-US',{maximumFractionDigits:0});
  if(Math.abs(n) >= 1) return n.toFixed(2);
  return n.toFixed(6);
}
function fmtBig(n){
  if(!n) return '—';
  if(n >= 1e12) return '$' + (n/1e12).toFixed(2) + 'T';
  if(n >= 1e9) return '$' + (n/1e9).toFixed(2) + 'B';
  if(n >= 1e6) return '$' + (n/1e6).toFixed(2) + 'M';
  return '$' + n.toLocaleString();
}
function fmtPct(n){
  if(n === null || n === undefined) return '—';
  return (n >= 0 ? '▲ ' : '▼ ') + Math.abs(n).toFixed(2) + '%';
}
function clsPct(n){ return n >= 0 ? 'up' : 'down'; }

/* ============================================================
   HELPER: Widgets TradingView (external-embedding)
============================================================ */
function createTVEmbed(containerId, scriptSrc, config){
  const container = document.getElementById(containerId);
  if(!container) return;
  container.innerHTML = '';
  const widgetDiv = document.createElement('div');
  widgetDiv.className = 'tradingview-widget-container';
  widgetDiv.style.height = '100%';
  widgetDiv.style.width = '100%';
  const innerDiv = document.createElement('div');
  innerDiv.className = 'tradingview-widget-container__widget';
  innerDiv.style.height = '100%';
  innerDiv.style.width = '100%';
  widgetDiv.appendChild(innerDiv);
  container.appendChild(widgetDiv);
  const script = document.createElement('script');
  script.type = 'text/javascript';
  script.src = scriptSrc;
  script.async = true;
  script.innerHTML = JSON.stringify(config);
  widgetDiv.appendChild(script);
}

/* ============================================================
   HELPER: Chart widget de TradingView (tv.js)
============================================================ */
function createTVWidget(containerId, symbol, height, interval, force){
  const container = document.getElementById(containerId);
  if(!container) return;
  if(force) container.innerHTML = '';
  const innerId = containerId + '_inner_' + Date.now();
  const div = document.createElement('div');
  div.id = innerId;
  div.style.height = height + 'px';
  div.style.width = '100%';
  container.innerHTML = '';
  container.appendChild(div);
  const script = document.createElement('script');
  script.src = 'https://s3.tradingview.com/tv.js';
  script.async = true;
  script.onload = () => {
    try{
      new TradingView.widget({
        container_id: innerId, autosize: false, width: '100%', height: height,
        symbol: symbol, interval: interval, timezone: 'Etc/UTC',
        theme: state.theme === 'light' ? 'light' : 'dark',
        style: '1', locale: 'es', toolbar_bg: state.theme === 'light' ? '#f0f3f6' : '#1c2128',
        enable_publishing: false, hide_side_toolbar: false, allow_symbol_change: true,
        details: true, withdateranges: true
      });
    }catch(e){ console.warn('TV widget error', e); }
  };
  document.head.appendChild(script);
}

/* ============================================================
   TICKER SUPERIOR
============================================================ */
async function loadTicker(){
  try{
    const r = await fetch(`${API.coingecko}/simple/price?ids=bitcoin,ethereum,solana,binancecoin,ripple,cardano&vs_currencies=usd&include_24hr_change=true`);
    const d = await r.json();
    const symbols = {bitcoin:'BTC', ethereum:'ETH', solana:'SOL', binancecoin:'BNB', ripple:'XRP', cardano:'ADA'};
    const bar = document.getElementById('tickerBar');
    bar.innerHTML = '';
    for(const [k,v] of Object.entries(d)){
      const ch = v.usd_24h_change || 0;
      bar.innerHTML += `<div class="ticker-item"><b>${symbols[k]}</b> $${fmt(v.usd)} <span class="${clsPct(ch)}">${fmtPct(ch)}</span></div>`;
    }
  }catch(e){ console.warn('Ticker error', e); }
}

/* ============================================================
   DASHBOARD
============================================================ */
async function loadTopCoins(){
  try{
    const r = await fetch(`${API.coingecko}/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=4&page=1&sparkline=false`);
    const d = await r.json();
    document.getElementById('topCoins').innerHTML = d.map(c => {
      const ch = c.price_change_percentage_24h || 0;
      return `<div class="card">
        <div class="card-title">${c.symbol.toUpperCase()}</div>
        <div class="coin-cell" style="margin-bottom:8px;"><img src="${c.image}" alt="${c.name}"><b>${c.name}</b></div>
        <div class="price">$${fmt(c.current_price)}</div>
        <div class="change ${clsPct(ch)}">${fmtPct(ch)}</div>
      </div>`;
    }).join('');
  }catch(e){ document.getElementById('topCoins').innerHTML = '<div class="loading">Error cargando precios.</div>'; }
}

async function loadFearGreed(){
  try{
    const r = await fetch(`${API.alternative}/fng/?limit=1`);
    const d = await r.json();
    const v = d.data[0];
    const val = parseInt(v.value);
    const color = val >= 75 ? 'var(--green)' : val >= 50 ? 'var(--gold)' : val >= 25 ? 'var(--orange)' : 'var(--red)';
    const emoji = val >= 75 ? '🤑' : val >= 50 ? '😊' : val >= 25 ? '😟' : '😱';
    document.getElementById('fearGreed').innerHTML = `
      <div style="display:flex;align-items:center;gap:16px;">
        <div style="font-size:2.5rem;">${emoji}</div>
        <div>
          <div style="font-size:2rem;font-weight:800;color:${color}">${val}/100</div>
          <div style="font-size:.9rem;color:var(--muted);">${v.value_classification}</div>
        </div>
      </div>`;
  }catch(e){ document.getElementById('fearGreed').innerHTML = '<div class="loading">No disponible</div>'; }
}

async function loadDominance(){
  try{
    const r = await fetch(`${API.coingecko}/global`);
    const d = await r.json();
    const btc = d.data.market_cap_percentage.btc;
    const eth = d.data.market_cap_percentage.eth;
    document.getElementById('dominance').innerHTML = `
      <div style="margin-bottom:10px;"><span style="font-size:1.6rem;font-weight:800;color:var(--gold)">${btc.toFixed(1)}%</span> <span style="color:var(--muted)">BTC</span></div>
      <div style="margin-bottom:10px;"><span style="font-size:1.6rem;font-weight:800;color:var(--purple)">${eth.toFixed(1)}%</span> <span style="color:var(--muted)">ETH</span></div>
      <div style="font-size:.8rem;color:var(--muted);">Cap. total: ${fmtBig(d.data.total_market_cap.usd)}</div>`;
  }catch(e){ document.getElementById('dominance').innerHTML = '<div class="loading">No disponible</div>'; }
}

async function loadTrending(){
  try{
    const r = await fetch(`${API.coingecko}/search/trending`);
    const d = await r.json();
    document.getElementById('trending').innerHTML = d.coins.slice(0,7).map((c,i) => {
      const item = c.item;
      return `<div class="news-item">
        <h4>${i+1}. ${item.name} <span class="badge badge-blue">${item.symbol}</span></h4>
        <p>Market Cap Rank: #${item.market_cap_rank || '—'}</p>
      </div>`;
    }).join('');
  }catch(e){ document.getElementById('trending').innerHTML = '<div class="loading">No disponible</div>'; }
}

function loadDashboardChart(){
  const c = document.getElementById('tv_dashboard');
  if(c.dataset.loaded) return;
  c.dataset.loaded = 1;
  createTVWidget('tv_dashboard', 'BINANCE:BTCUSDT', 420, '60');
}

function loadHeatmap(){
  const c = document.getElementById('tv_heatmap');
  if(c.dataset.loaded) return;
  c.dataset.loaded = 1;
  createTVEmbed(
    'tv_heatmap',
    'https://s3.tradingview.com/external-embedding/embed-widget-stock-heatmap.js',
    {
      exchanges: [],
      dataSource: "Crypto",
      grouping: "no_group",
      blockSize: "market_cap_basic",
      blockColor: "change",
      locale: "es",
      symbolUrl: "",
      colorTheme: state.theme === 'light' ? 'light' : 'dark',
      hasTopBar: true,
      isDataSetEnabled: true,
      isZoomEnabled: true,
      hasSymbolTooltip: true,
      width: "100%",
      height: 500
    }
  );
}

/* ============================================================
   CRIPTOMONEDAS
============================================================ */
async function loadCryptoTable(){
  try{
    const r = await fetch(`${API.coingecko}/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=50&page=1&sparkline=false&price_change_percentage=7d`);
    state.cryptoData = await r.json();
    renderCryptoTable(state.cryptoData);
    document.getElementById('lastUpdate').textContent = 'Actualizado ' + new Date().toLocaleTimeString('es-ES');
  }catch(e){ document.querySelector('#cryptoTable tbody').innerHTML = '<tr><td colspan="8" class="loading">Error cargando datos. Recarga en unos segundos.</td></tr>'; }
}

function renderCryptoTable(data){
  const tb = document.querySelector('#cryptoTable tbody');
  if(!data.length){ tb.innerHTML = '<tr><td colspan="8" class="loading">Sin resultados</td></tr>'; return; }
  tb.innerHTML = data.map(c => {
    const ch = c.price_change_percentage_24h || 0;
    const ch7 = c.price_change_percentage_7d_in_currency || 0;
    const inWatch = state.watchlist.includes(c.id);
    return `<tr>
      <td>${c.market_cap_rank}</td>
      <td><div class="coin-cell"><img src="${c.image}" alt="${c.name}"><div><b>${c.name}</b> <span class="sym">${c.symbol.toUpperCase()}</span></div></div></td>
      <td class="mono">$${fmt(c.current_price)}</td>
      <td class="${clsPct(ch)}">${fmtPct(ch)}</td>
      <td class="${clsPct(ch7)}">${fmtPct(ch7)}</td>
      <td class="mono">${fmtBig(c.market_cap)}</td>
      <td class="mono">${fmtBig(c.total_volume)}</td>
      <td><button class="action small secondary" onclick="toggleWatch('${c.id}','${c.symbol}')">${inWatch ? '★' : '☆'}</button></td>
    </tr>`;
  }).join('');
}

function filterCryptoTable(){
  const q = document.getElementById('cryptoSearch').value.toLowerCase();
  const filtered = state.cryptoData.filter(c => c.name.toLowerCase().includes(q) || c.symbol.toLowerCase().includes(q));
  renderCryptoTable(filtered);
}

function loadCryptoChart(){
  const c = document.getElementById('tv_crypto');
  if(c.dataset.loaded) return;
  c.dataset.loaded = 1;
  createTVWidget('tv_crypto', 'BINANCE:BTCUSDT', 520, 'D');
}

/* ============================================================
   WATCHLIST
============================================================ */
function toggleWatch(id, sym){
  const idx = state.watchlist.indexOf(id);
  if(idx >= 0){ state.watchlist.splice(idx,1); }
  else{ state.watchlist.push(id); }
  localStorage.setItem('watchlist', JSON.stringify(state.watchlist));
  renderCryptoTable(state.cryptoData);
  showToast(state.watchlist.includes(id) ? `⭐ ${sym.toUpperCase()} añadido` : `Eliminado`);
}

function renderWatchlist(){
  const box = document.getElementById('watchlistBox');
  if(!state.watchlist.length){ box.innerHTML = '<div class="loading">Añade activos desde la tabla de cripto (estrella ☆).</div>'; return; }
  const items = state.watchlist.map(id => {
    const coin = state.cryptoData.find(c => c.id === id);
    if(!coin) return `<span class="badge badge-blue" style="margin:4px;">${id}</span>`;
    const ch = coin.price_change_percentage_24h || 0;
    return `<div style="display:inline-flex;align-items:center;gap:8px;background:var(--bg2);padding:8px 14px;border-radius:8px;margin:4px;border:1px solid var(--border);">
      <img src="${coin.image}" style="width:20px;height:20px;border-radius:50%;">
      <b>${coin.symbol.toUpperCase()}</b>
      <span class="mono">$${fmt(coin.current_price)}</span>
      <span class="${clsPct(ch)}" style="font-size:.8rem;">${fmtPct(ch)}</span>
      <button class="action small danger" style="padding:2px 8px;font-size:.7rem;" onclick="toggleWatch('${coin.id}','${coin.symbol}')">✕</button>
    </div>`;
  }).join('');
  box.innerHTML = items;
}

/* ============================================================
   BOLSA
============================================================ */
function loadStocksWidget(){
  const c = document.getElementById('tv_stocks');
  if(!c.dataset.loaded){
    c.dataset.loaded = 1;
    createTVEmbed(
      'tv_stocks',
      'https://s3.tradingview.com/external-embedding/embed-widget-screener.js',
      {
        width: "100%",
        height: 600,
        defaultColumn: "overview",
        defaultScreen: "general",
        market: "america",
        showToolbar: true,
        colorTheme: state.theme === 'light' ? 'light' : 'dark',
        isTransparent: false,
        locale: "es"
      }
    );
  }
  const sp = document.getElementById('tv_sp500');
  if(!sp.dataset.loaded){
    sp.dataset.loaded = 1;
    createTVWidget('tv_sp500', 'SP:SPX', 420, 'D');
  }
}

function loadIndexCards(){
  const grid = document.getElementById('indexCards');
  if(grid.dataset.loaded) return;
  grid.dataset.loaded = 1;
  const indices = [
    {name:'S&P 500', sym:'SP:SPX', color:'var(--accent)'},
    {name:'Nasdaq 100', sym:'NASDAQ:NDX', color:'var(--purple)'},
    {name:'Dow Jones', sym:'DJ:DJI', color:'var(--gold)'},
    {name:'IBEX 35', sym:'BME:IBC', color:'var(--orange)'},
    {name:'DAX', sym:'XETR:DAX', color:'var(--green)'},
    {name:'Nikkei 225', sym:'TVC:NI225', color:'var(--pink)'}
  ];
  grid.innerHTML = indices.map(i => `
    <div class="card" style="text-align:center;">
      <div class="card-title">${i.name}</div>
      <div style="font-size:1.8rem;margin:10px 0;color:${i.color};">📊</div>
      <div style="font-size:.8rem;color:var(--muted);">${i.sym}</div>
    </div>`).join('');
}

/* ============================================================
   ANÁLISIS
============================================================ */
function loadAnalysisChart(){
  const sym = document.getElementById('analysisSymbol').value;
  createTVWidget('tv_analysis', sym, 620, '60', true);
}

/* ============================================================
   NOTICIAS
============================================================ */
const fallbackNews = [
  {t:'Bitcoin supera los $100K: ¿nuevo ciclo alcista?', d:'El BTC alcanza un nuevo máximo histórico impulsado por la adopción institucional.', c:'Mercados', time:'Hace 2h'},
  {t:'Ethereum completa su actualización Pectra', d:'Mejora la escalabilidad y reduce las comisiones de gas en un 40%.', c:'Tecnología', time:'Hace 5h'},
  {t:'La SEC aprueba nuevos ETFs de Solana', d:'Tres gestoras obtienen luz verde para lanzar productos cotizados respaldados por SOL.', c:'Regulación', time:'Hace 8h'},
  {t:'Wall Street cierra mixto tras datos de inflación', d:'El S&P 500 cae un 0.3% mientras el Nasdaq sube un 0.5%.', c:'Bolsa', time:'Hace 12h'},
  {t:'Binance refuerza sus controles KYC en Europa', d:'Nuevas medidas de compliance tras la entrada en vigor de MiCA.', c:'Regulación', time:'Hace 1d'},
  {t:'El oro marca máximos históricos por encima de $2.800', d:'La incertidumbre geopolítica impulsa al metal precioso.', c:'Materias Primas', time:'Hace 1d'},
  {t:'DeFi supera los $200B en TVL', d:'Los protocolos recuperan niveles previos al mercado bajista.', c:'DeFi', time:'Hace 2d'},
  {t:'BlackRock aumenta su exposición a Bitcoin', d:'El gigante de la gestión de activos revela compras adicionales de BTC.', c:'Institucional', time:'Hace 2d'}
];

function loadNews(){
  document.getElementById('newsList').innerHTML = fallbackNews.map(n => `
    <div class="news-item">
      <h4>${n.t} <span class="badge badge-blue">${n.c}</span></h4>
      <p>${n.d}</p>
      <div class="meta"><span>🕒 ${n.time}</span><span>📰 CryptoMarket Pro</span></div>
    </div>`).join('');
}

function loadNewsWidget(){
  const c = document.getElementById('tv_news');
  if(c.dataset.loaded) return;
  c.dataset.loaded = 1;
  createTVEmbed(
    'tv_news',
    'https://s3.tradingview.com/external-embedding/embed-widget-timeline.js',
    {
      feedMode: "all_symbols",
      isTransparent: false,
      displayMode: "regular",
      width: "100%",
      height: 560,
      colorTheme: state.theme === 'light' ? 'light' : 'dark',
      locale: "es"
    }
  );
}

/* ============================================================
   CALENDARIO
============================================================ */
function loadCalendarWidget(){
  const c = document.getElementById('tv_calendar');
  if(c.dataset.loaded) return;
  c.dataset.loaded = 1;
  createTVEmbed(
    'tv_calendar',
    'https://s3.tradingview.com/external-embedding/embed-widget-events.js',
    {
      colorTheme: state.theme === 'light' ? 'light' : 'dark',
      isTransparent: false,
      width: "100%",
      height: 640,
      locale: "es",
      importanceFilter: "0,1",
      countryFilter: "us,eu,es,gb,jp,cn"
    }
  );
}

/* ============================================================
   GUÍAS
============================================================ */
const guides = [
  {icon:'📊', t:'Análisis técnico para principiantes', d:'Aprende a leer gráficos de velas, soportes, resistencias y patrones básicos.'},
  {icon:'🔐', t:'Cómo guardar tus criptos de forma segura', d:'Hot wallets vs cold wallets, seed phrases y mejores prácticas.'},
  {icon:'💎', t:'Qué es el staking y cómo genera rendimiento', d:'Guía completa para ganar intereses sobre tus criptomonedas.'},
  {icon:'📉', t:'Gestión del riesgo en trading', d:'Stop loss, take profit, position sizing y psicología del trader.'},
  {icon:'🌐', t:'Qué es DeFi y cómo funciona', d:'Exchanges descentralizados, pools de liquidez y yield farming.'},
  {icon:'📈', t:'Análisis fundamental vs técnico', d:'Cuándo usar cada enfoque y cómo combinarlos.'},
  {icon:'🧾', t:'Fiscalidad cripto en España', d:'Cómo declarar tus ganancias y evitar sustos con Hacienda.'},
  {icon:'⚡', t:'Layer 2 y escalabilidad', d:'Rollups, sidechains y las soluciones que revolucionan Ethereum.'},
  {icon:'🤖', t:'Trading algorítmico básico', d:'Introducción a los bots y estrategias automatizadas.'}
];

const glossary = [
  {t:'HODL', d:'Estrategia de mantener criptomonedas a largo plazo sin vender.'},
  {t:'FOMO', d:'Miedo a perderse una oportunidad de inversión.'},
  {t:'FUD', d:'Miedo, incertidumbre y duda. Noticias negativas que hacen caer el precio.'},
  {t:'Staking', d:'Bloquear criptos para validar transacciones y ganar recompensas.'},
  {t:'Yield Farming', d:'Proporcionar liquidez a protocolos DeFi a cambio de intereses.'},
  {t:'Gas', d:'Comisión que se paga por realizar transacciones en una blockchain.'},
  {t:'Wallet', d:'Monedero digital donde se almacenan claves privadas.'},
  {t:'DeFi', d:'Finanzas descentralizadas: servicios financieros sin intermediarios.'},
  {t:'NFT', d:'Token no fungible que representa un activo digital único.'},
  {t:'Altcoin', d:'Cualquier criptomoneda que no sea Bitcoin.'}
];

function loadGuides(){
  document.getElementById('guidesGrid').innerHTML = guides.map(g => `
    <div class="card">
      <div style="font-size:2rem;margin-bottom:10px;">${g.icon}</div>
      <h3>${g.t}</h3>
      <p style="color:var(--muted);font-size:.87rem;">${g.d}</p>
    </div>`).join('');
  document.getElementById('glossaryBox').innerHTML = `<div class="grid grid-2">${glossary.map(g => `
    <div style="padding:10px 0;border-bottom:1px solid var(--border);">
      <b style="color:var(--accent);">${g.t}</b><br><span style="color:var(--muted);font-size:.85rem;">${g.d}</span>
    </div>`).join('')}</div>`;
}

/* ============================================================
   EXCHANGES
============================================================ */
const exchanges = [
  {n:'Binance', d:'El exchange más grande del mundo. Comisiones desde 0.1%.', b:'badge-green', url:'https://www.binance.com/es/register?ref=TU_CODIGO', maker:'0.10%', taker:'0.10%', coins:'+350', reg:'Global'},
  {n:'Coinbase', d:'Ideal para principiantes. Interfaz sencilla y regulado en USA.', b:'badge-blue', url:'https://www.coinbase.com/join/TU_CODIGO', maker:'0.40%', taker:'0.60%', coins:'+250', reg:'USA (NASDAQ: COIN)'},
  {n:'Kraken', d:'Máxima seguridad y regulación. Excelente para Europa.', b:'badge-blue', url:'https://www.kraken.com/register?ref=TU_CODIGO', maker:'0.16%', taker:'0.26%', coins:'+200', reg:'USA, Europa (MiCA)'},
  {n:'Bybit', d:'Derivados y trading avanzado con apalancamiento.', b:'badge-blue', url:'https://www.bybit.com/register?affiliate_id=TU_CODIGO', maker:'0.02%', taker:'0.055%', coins:'+300', reg:'Dubai, global'},
  {n:'OKX', d:'Exchange global con Web3 wallet integrada.', b:'badge-blue', url:'https://www.okx.com/join/TU_CODIGO', maker:'0.08%', taker:'0.10%', coins:'+300', reg:'Global'},
  {n:'Bitget', d:'Copy trading y futuros. Popular entre traders activos.', b:'badge-blue', url:'https://www.bitget.com/register?ref=TU_CODIGO', maker:'0.02%', taker:'0.06%', coins:'+400', reg:'Seychelles, global'}
];

function loadExchanges(){
  document.getElementById('exchangeGrid').innerHTML = exchanges.map(e => `
    <div class="card">
      <div class="flex-between" style="margin-bottom:10px;">
        <h3>${e.n}</h3><span class="badge ${e.b}">Verificado</span>
      </div>
      <p style="color:var(--muted);font-size:.87rem;margin-bottom:14px;">${e.d}</p>
      <a href="${e.url}" target="_blank" rel="noopener" class="action" style="display:block;text-align:center;text-decoration:none;">Registrarse →</a>
    </div>`).join('');
  document.querySelector('#exchangeTable tbody').innerHTML = exchanges.map(e => `
    <tr>
      <td><b>${e.n}</b></td><td class="mono">${e.maker}</td><td class="mono">${e.taker}</td>
      <td>${e.coins}</td><td style="font-size:.8rem;">${e.reg}</td><td>⭐⭐⭐⭐⭐</td>
    </tr>`).join('');
}

/* ============================================================
   CALCULADORA IMPUESTOS
============================================================ */
function calcTax(){
  const buy = parseFloat(document.getElementById('taxBuy').value) || 0;
  const sell = parseFloat(document.getElementById('taxSell').value) || 0;
  const fees = parseFloat(document.getElementById('taxFees').value) || 0;
  const method = document.getElementById('taxMethod').value;
  const profit = sell - buy - fees;
  const box = document.getElementById('taxResult');
  if(sell <= 0){ box.innerHTML = '<p class="loading">Introduce un precio de venta válido.</p>'; return; }
  if(profit <= 0){
    box.innerHTML = `<p class="price" style="color:var(--muted)">Pérdida de ${Math.abs(profit).toFixed(2)} €</p>
      <p style="color:var(--muted);margin-top:8px;font-size:.9rem;">No hay impuestos a pagar.</p>`;
    return;
  }
  const brackets = [
    {limit: 6000, rate: 0.19},
    {limit: 50000, rate: 0.21},
    {limit: 200000, rate: 0.23},
    {limit: 300000, rate: 0.27},
    {limit: Infinity, rate: 0.28}
  ];
  let remaining = profit, tax = 0, prev = 0, breakdown = [];
  for(const b of brackets){
    if(remaining <= 0) break;
    const taxable = Math.min(remaining, b.limit - prev);
    const t = taxable * b.rate;
    tax += t;
    breakdown.push(`Tramo ${prev.toLocaleString()}–${b.limit === Infinity ? '∞' : b.limit.toLocaleString()} € (${(b.rate*100).toFixed(0)}%): ${t.toFixed(2)} €`);
    remaining -= taxable;
    prev = b.limit;
  }
  const net = profit - tax;
  box.innerHTML = `
    <div style="margin-bottom:12px;"><div class="card-title">Ganancia patrimonial</div><div class="price profit">${profit.toLocaleString('es-ES',{minimumFractionDigits:2})} €</div></div>
    <div style="margin-bottom:12px;"><div class="card-title">Impuestos estimados</div><div class="price" style="color:var(--gold)">${tax.toLocaleString('es-ES',{minimumFractionDigits:2})} €</div></div>
    <div style="margin-bottom:12px;"><div class="card-title">Beneficio neto</div><div class="price profit">${net.toLocaleString('es-ES',{minimumFractionDigits:2})} €</div></div>
    <details style="margin-top:10px;"><summary style="cursor:pointer;color:var(--muted);font-size:.85rem;">Desglose por tramos (${method.toUpperCase()})</summary><p style="font-size:.82rem;color:var(--muted);margin-top:8px;">${breakdown.join('<br>')}</p></details>`;
}

/* ============================================================
   PORTFOLIO
============================================================ */
function savePortfolio(){ localStorage.setItem('cryptoPortfolio', JSON.stringify(state.portfolio)); }
function clearPortfolio(){ if(confirm('¿Vaciar todo el portfolio?')){ state.portfolio = []; savePortfolio(); renderPortfolio(); } }

function addPosition(){
  const coin = document.getElementById('pfCoin').value;
  const amount = parseFloat(document.getElementById('pfAmount').value);
  const buy = parseFloat(document.getElementById('pfBuyPrice').value);
  if(!amount || amount <= 0 || !buy || buy <= 0){ alert('Introduce cantidad y precio válidos.'); return; }
  state.portfolio.push({id: Date.now(), coin, amount, buy});
  savePortfolio();
  document.getElementById('pfAmount').value = '';
  document.getElementById('pfBuyPrice').value = '';
  renderPortfolio();
}

function removePosition(id){
  state.portfolio = state.portfolio.filter(p => p.id !== id);
  savePortfolio();
  renderPortfolio();
}

async function renderPortfolio(){
  const tb = document.querySelector('#pfTable tbody');
  const summary = document.getElementById('pfSummary');
  if(state.portfolio.length === 0){
    tb.innerHTML = '<tr><td colspan="7" class="loading">Portfolio vacío. Añade tu primera transacción.</td></tr>';
    summary.innerHTML = '<div class="loading">Sin datos</div>';
    if(pfChartInstance){ pfChartInstance.destroy(); pfChartInstance = null; }
    return;
  }
  const ids = [...new Set(state.portfolio.map(p => p.coin))].join(',');
  let prices = {};
  try{
    const r = await fetch(`${API.coingecko}/simple/price?ids=${ids}&vs_currencies=usd`);
    prices = await r.json();
  }catch(e){ console.warn(e); }
  let totalInvested = 0, totalCurrent = 0;
  tb.innerHTML = state.portfolio.map(p => {
    const price = prices[p.coin]?.usd || 0;
    const invested = p.amount * p.buy;
    const current = p.amount * price;
    const pl = current - invested;
    const plPct = invested > 0 ? (pl / invested) * 100 : 0;
    totalInvested += invested; totalCurrent += current;
    const cls = pl >= 0 ? 'profit' : 'loss';
    return `<tr>
      <td><b>${p.coin.charAt(0).toUpperCase() + p.coin.slice(1)}</b></td>
      <td class="mono">${p.amount}</td>
      <td class="mono">$${p.buy.toLocaleString()}</td>
      <td class="mono">$${price.toLocaleString(undefined,{maximumFractionDigits:2})}</td>
      <td class="mono">$${current.toLocaleString(undefined,{maximumFractionDigits:2})}</td>
      <td class="${cls}">${pl >= 0 ? '+' : ''}$${pl.toFixed(2)} (${plPct.toFixed(1)}%)</td>
      <td><button class="action small danger" onclick="removePosition(${p.id})">✕</button></td>
    </tr>`;
  }).join('');
  const totalPl = totalCurrent - totalInvested;
  const totalPlPct = totalInvested > 0 ? (totalPl / totalInvested) * 100 : 0;
  const cls = totalPl >= 0 ? 'profit' : 'loss';
  summary.innerHTML = `
    <div style="margin-bottom:12px;"><div class="card-title">Invertido</div><div class="price">$${totalInvested.toLocaleString(undefined,{maximumFractionDigits:2})}</div></div>
    <div style="margin-bottom:12px;"><div class="card-title">Valor actual</div><div class="price">$${totalCurrent.toLocaleString(undefined,{maximumFractionDigits:2})}</div></div>
    <div><div class="card-title">P&L Total</div><div class="price ${cls}">${totalPl >= 0 ? '+' : ''}$${totalPl.toFixed(2)}</div><div class="${cls}" style="font-size:1rem;">${totalPlPct >= 0 ? '+' : ''}${totalPlPct.toFixed(2)}%</div></div>`;
  const ctx = document.getElementById('pfChart');
  if(pfChartInstance) pfChartInstance.destroy();
  const labels = state.portfolio.map(p => p.coin.toUpperCase());
  const values = state.portfolio.map(p => p.amount * (prices[p.coin]?.usd || 0));
  pfChartInstance = new Chart(ctx, {
    type: 'doughnut',
    data: { labels, datasets: [{ data: values, backgroundColor: ['#f0b90b','#2962ff','#26a69a','#a371f7','#ff9800','#f778ba','#58a6ff','#ef5350','#8b949e','#d29922'] }] },
    options: { responsive: true, plugins: { legend: { position: 'bottom', labels: { color: getComputedStyle(document.body).color, font: { size: 10 } } } } }
  });
}

/* ============================================================
   HERRAMIENTAS
============================================================ */
async function convertCurrency(){
  const amount = parseFloat(document.getElementById('convAmount').value) || 0;
  const from = document.getElementById('convFrom').value;
  const to = document.getElementById('convTo').value;
  const box = document.getElementById('convResult');
  if(amount <= 0){ box.textContent = 'Introduce una cantidad válida.'; return; }
  box.textContent = 'Convirtiendo...';
  try{
    if(from === 'usd'){
      const r = await fetch(`${API.coingecko}/simple/price?ids=${to}&vs_currencies=usd`);
      const d = await r.json();
      const price = d[to]?.usd || 0;
      box.innerHTML = `${amount} USD = <b style="color:var(--green)">${(amount / price).toFixed(6)} ${to.toUpperCase()}</b>`;
      return;
    }
    const r = await fetch(`${API.coingecko}/simple/price?ids=${from}&vs_currencies=usd,eur`);
    const d = await r.json();
    const usd = d[from]?.usd || 0;
    const eur = d[from]?.eur || 0;
    if(to === 'usd') box.innerHTML = `${amount} ${from.toUpperCase()} = <b style="color:var(--green)">$${(amount * usd).toFixed(2)} USD</b>`;
    else if(to === 'eur') box.innerHTML = `${amount} ${from.toUpperCase()} = <b style="color:var(--green)">${(amount * eur).toFixed(2)} EUR</b>`;
    else{
      const r2 = await fetch(`${API.coingecko}/simple/price?ids=${to}&vs_currencies=usd`);
      const d2 = await r2.json();
      const toPrice = d2[to]?.usd || 0;
      box.innerHTML = `${amount} ${from.toUpperCase()} = <b style="color:var(--green)">${(amount * usd / toPrice).toFixed(6)} ${to.toUpperCase()}</b>`;
    }
  }catch(e){ box.textContent = 'Error en la conversión.'; }
}

async function calcDCA(){
  const amount = parseFloat(document.getElementById('dcaAmount').value) || 0;
  const freq = parseInt(document.getElementById('dcaFreq').value);
  const periods = parseInt(document.getElementById('dcaPeriods').value) || 0;
  const coin = document.getElementById('dcaCoin').value;
  const box = document.getElementById('dcaResult');
  if(amount <= 0 || periods <= 0){ box.innerHTML = '<div class="warn-box">Introduce valores válidos.</div>'; return; }
  box.innerHTML = '<div class="loading">Simulando...</div>';
  try{
    const r = await fetch(`${API.coingecko}/coins/${coin}/market_chart?vs_currency=usd&days=${freq * periods}&interval=daily`);
    const d = await r.json();
    if(!d.prices || d.prices.length < periods){ box.innerHTML = '<div class="warn-box">Sin suficientes datos históricos.</div>'; return; }
    const prices = d.prices.map(p => p[1]);
    const step = Math.floor(prices.length / periods);
    let totalCoins = 0, totalInvested = 0;
    for(let i = 0; i < periods; i++){
      const idx = Math.min(i * step, prices.length - 1);
      totalCoins += amount / prices[idx];
      totalInvested += amount;
    }
    const finalPrice = prices[prices.length - 1];
    const finalValue = totalCoins * finalPrice;
    const pl = finalValue - totalInvested;
    const roi = (pl / totalInvested) * 100;
    const avgPrice = totalInvested / totalCoins;
    box.innerHTML = `<div class="success-box">
      Total invertido: <b>$${totalInvested.toLocaleString()}</b><br>
      Cripto acumulada: <b>${totalCoins.toFixed(6)} ${coin.toUpperCase()}</b><br>
      Precio medio: <b>$${avgPrice.toFixed(2)}</b><br>
      Valor final: <b>$${finalValue.toFixed(2)}</b><br>
      <span class="${pl >= 0 ? 'profit' : 'loss'}">P&L: ${pl >= 0 ? '+' : ''}$${pl.toFixed(2)} (${roi.toFixed(2)}%)</span>
    </div>`;
  }catch(e){ box.innerHTML = '<div class="warn-box">Error obteniendo datos. CoinGecko puede limitar peticiones.</div>'; }
}

function calcRisk(){
  const capital = parseFloat(document.getElementById('riskCapital').value) || 0;
  const riskPct = parseFloat(document.getElementById('riskPercent').value) || 0;
  const entry = parseFloat(document.getElementById('riskEntry').value) || 0;
  const stop = parseFloat(document.getElementById('riskStop').value) || 0;
  const box = document.getElementById('riskResult');
  if(capital <= 0 || riskPct <= 0 || entry <= 0 || stop <= 0){ box.innerHTML = '<div class="warn-box">Completa todos los campos.</div>'; return; }
  const riskAmount = capital * (riskPct / 100);
  const stopDistance = Math.abs(entry - stop);
  const stopPct = (stopDistance / entry) * 100;
  const positionSize = riskAmount / (stopDistance / entry);
  const positionValue = positionSize * entry;
  box.innerHTML = `<div class="info-box">
    <b>Riesgo máximo:</b> $${riskAmount.toFixed(2)}<br>
    <b>Distancia al stop:</b> $${stopDistance.toFixed(2)} (${stopPct.toFixed(2)}%)<br>
    <b>Tamaño de posición:</b> ${positionSize.toFixed(6)} unidades<br>
    <b>Valor de posición:</b> $${positionValue.toFixed(2)}<br>
    <b>Apalancamiento:</b> ${(positionValue / capital).toFixed(2)}x
  </div>`;
}

function calcROI(){
  const invest = parseFloat(document.getElementById('roiInvest').value) || 0;
  const final = parseFloat(document.getElementById('roiFinal').value) || 0;
  const years = parseFloat(document.getElementById('roiYears').value) || 1;
  const box = document.getElementById('roiResult');
  if(invest <= 0 || final <= 0 || years <= 0){ box.innerHTML = '<div class="warn-box">Completa todos los campos.</div>'; return; }
  const profit = final - invest;
  const roi = (profit / invest) * 100;
  const cagr = (Math.pow(final / invest, 1 / years) - 1) * 100;
  box.innerHTML = `<div class="success-box">
    <b>Beneficio:</b> <span class="${profit >= 0 ? 'profit' : 'loss'}">$${profit.toFixed(2)}</span><br>
    <b>ROI total:</b> <span class="${roi >= 0 ? 'profit' : 'loss'}">${roi.toFixed(2)}%</span><br>
    <b>CAGR anualizado:</b> <span class="${cagr >= 0 ? 'profit' : 'loss'}">${cagr.toFixed(2)}%</span>
  </div>`;
}

/* ============================================================
   ALERTAS
============================================================ */
function saveAlerts(){ localStorage.setItem('priceAlerts', JSON.stringify(state.alerts)); }
function addAlert(){
  const coin = document.getElementById('alertCoin').value;
  const cond = document.getElementById('alertCondition').value;
  const price = parseFloat(document.getElementById('alertPrice').value);
  if(!price || price <= 0){ alert('Introduce un precio válido.'); return; }
  state.alerts.push({id: Date.now(), coin, cond, price, triggered: false});
  saveAlerts();
  document.getElementById('alertPrice').value = '';
  renderAlerts();
  showToast('🔔 Alerta creada');
}
function removeAlert(id){
  state.alerts = state.alerts.filter(a => a.id !== id);
  saveAlerts();
  renderAlerts();
}
function renderAlerts(){
  const box = document.getElementById('alertList');
  if(!state.alerts.length){ box.innerHTML = '<div class="loading">No hay alertas configuradas.</div>'; return; }
  box.innerHTML = state.alerts.map(a => `
    <div class="news-item" style="display:flex;justify-content:space-between;align-items:center;">
      <div>
        <b>${a.coin.toUpperCase()}</b> ${a.cond === 'above' ? 'por encima de' : 'por debajo de'} <b class="mono">$${a.price.toLocaleString()}</b>
        ${a.triggered ? '<span class="badge badge-gold">✅ Disparada</span>' : '<span class="badge badge-green">Activa</span>'}
      </div>
      <button class="action small danger" onclick="removeAlert(${a.id})">✕</button>
    </div>`).join('');
}
async function checkAlerts(){
  if(!state.alerts.length) return;
  const coins = [...new Set(state.alerts.map(a => a.coin))].join(',');
  try{
    const r = await fetch(`${API.coingecko}/simple/price?ids=${coins}&vs_currencies=usd`);
    const d = await r.json();
    state.alerts.forEach(a => {
      const p = d[a.coin]?.usd;
      if(!p) return;
      if(a.cond === 'above' && p >= a.price && !a.triggered){ a.triggered = true; showToast(`🚀 ${a.coin.toUpperCase()} superó $${a.price}!`, 'error'); }
      if(a.cond === 'below' && p <= a.price && !a.triggered){ a.triggered = true; showToast(`⚠️ ${a.coin.toUpperCase()} cayó bajo $${a.price}!`, 'error'); }
    });
    saveAlerts(); renderAlerts();
  }catch(e){ console.warn(e); }
}

/* ============================================================
   COMPARADOR
============================================================ */
async function compareCoins(){
  const a = document.getElementById('compareA').value;
  const b = document.getElementById('compareB').value;
  const box = document.getElementById('compareResult');
  box.innerHTML = '<div class="loading">Comparando...</div>';
  try{
    const r = await fetch(`${API.coingecko}/coins/markets?vs_currency=usd&ids=${a},${b}&sparkline=false&price_change_percentage=24h,7d`);
    const d = await r.json();
    if(d.length < 2){ box.innerHTML = '<div class="warn-box">No se pudieron obtener datos.</div>'; return; }
    box.innerHTML = `<div class="grid grid-2">
      ${d.map(c => `
        <div class="card" style="text-align:center;">
          <img src="${c.image}" style="width:48px;height:48px;border-radius:50%;margin-bottom:8px;">
          <h3>${c.name} (${c.symbol.toUpperCase()})</h3>
          <div class="price" style="margin:10px 0;">$${fmt(c.current_price)}</div>
          <div>24h: <span class="${clsPct(c.price_change_percentage_24h)}">${fmtPct(c.price_change_percentage_24h)}</span></div>
          <div>7d: <span class="${clsPct(c.price_change_percentage_7d_in_currency)}">${fmtPct(c.price_change_percentage_7d_in_currency)}</span></div>
          <div>Cap: ${fmtBig(c.market_cap)}</div>
          <div>Vol: ${fmtBig(c.total_volume)}</div>
        </div>`).join('')}
    </div>`;
  }catch(e){ box.innerHTML = '<div class="warn-box">Error en la comparación.</div>'; }
}

/* ============================================================
   DEFI
============================================================ */
async function loadDefiData(){
  try{
    const r = await fetch(`${API.defillama}/protocols`);
    const d = await r.json();
    const top = d.sort((a,b) => (b.tvl||0) - (a.tvl||0)).slice(0, 10);
    document.querySelector('#defiTable tbody').innerHTML = top.map((p,i) => `
      <tr>
        <td>${i+1}</td>
        <td><b>${p.name}</b></td>
        <td>${p.chain || 'Multi-chain'}</td>
        <td class="mono">${fmtBig(p.tvl)}</td>
        <td class="${(p.change_1d||0) >= 0 ? 'up' : 'down'}">${fmtPct(p.change_1d || 0)}</td>
      </tr>`).join('');
    const totalTvl = d.reduce((s,p) => s + (p.tvl||0), 0);
    const topChain = {};
    d.forEach(p => { if(p.chain) topChain[p.chain] = (topChain[p.chain]||0) + (p.tvl||0); });
    const sortedChains = Object.entries(topChain).sort((a,b) => b[1]-a[1]).slice(0,3);
    document.getElementById('defiCards').innerHTML = `
      <div class="card"><div class="card-title">TVL Total DeFi</div><div class="price">${fmtBig(totalTvl)}</div></div>
      ${sortedChains.map(([chain, tvl]) => `<div class="card"><div class="card-title">Top Chain: ${chain}</div><div class="price">${fmtBig(tvl)}</div></div>`).join('')}`;
  }catch(e){ document.getElementById('defiCards').innerHTML = '<div class="loading">No se pudieron cargar los datos DeFi.</div>'; }
}

/* ============================================================
   TOAST Y COPIAR
============================================================ */
function showToast(msg, type){
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.className = 'toast show' + (type === 'error' ? ' error' : '');
  setTimeout(() => t.className = 'toast', 3000);
}

async function copyAllCode(){
  try{
    const r = await fetch(window.location.href);
    const text = await r.text();
    await navigator.clipboard.writeText(text);
    showToast('✅ ¡Código HTML copiado!');
  }catch(e){
    try{
      const text = '<!DOCTYPE html>\n' + document.documentElement.outerHTML;
      await navigator.clipboard.writeText(text);
      showToast('✅ Código copiado (versión DOM)');
    }catch(err){ showToast('❌ No se pudo copiar. Usa Ctrl+U.', 'error'); }
  }
}

/* ============================================================
   INICIALIZACIÓN
============================================================ */
function init(){
  buildNav();
  loadTicker();
  loadTopCoins();
  loadFearGreed();
  loadDominance();
  loadTrending();
  loadCryptoTable();
  loadNews();
  loadGuides();
  loadExchanges();
  renderPortfolio();
  renderAlerts();
  loadDashboardChart();
  loadHeatmap();
  setInterval(loadTicker, 60000);
  setInterval(loadCryptoTable, 120000);
  setInterval(renderPortfolio, 120000);
  setInterval(checkAlerts, 30000);
  setInterval(loadFearGreed, 300000);
}

document.addEventListener('DOMContentLoaded', init);
</script>

<!-- ============================================================
     A-ADS STICKY BANNER — Anuncio inferior
============================================================ -->
<!-- BEGIN AADS AD UNIT 2462580 -->
<div style="position: absolute; z-index: 99999">
  <input autocomplete="off" type="checkbox" id="aadsstickymwmhymdu" hidden />
  <div style="padding-top: 0; padding-bottom: auto;">
    <div style="width:100%;height:auto;position:fixed;text-align:center;font-size:0;bottom:0;left:0;right:0;margin:auto">
      <label for="aadsstickymwmhymdu" style="top: 50%;transform: translateY(-50%);right:24px;position: absolute;border-radius: 4px; background: rgba(248, 248, 249, 0.70); padding: 4px;z-index: 99999;cursor:pointer">
        <svg fill="#000000" height="16px" width="16px" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 490 490">
          <polygon points="456.851,0 245,212.564 33.149,0 0.708,32.337 212.669,245.004 0.708,457.678 33.149,490 245,277.443 456.851,490 489.292,457.678 277.331,245.004 489.292,32.337 "/>
        </svg>
      </label>
      <div id="frame" style="width: 100%;margin: auto;position: relative; z-index: 99998;">
        <iframe data-aa="2462580" src="//acceptable.a-ads.com/2462580/?size=Adaptive" style="border:0; padding:0; width:70%; height:auto; overflow:hidden; margin: auto"></iframe>
      </div>
    </div>
    <style>
      #aadsstickymwmhymdu:checked + div { display: none; }
    </style>
  </div>
</div>
<!-- END AADS AD UNIT 2462580 -->

<script>
/* ============================================================
   AJUSTE DINÁMICO DEL LAYOUT SEGÚN EL ANUNCIO
   El banner está en la parte inferior. Reservamos padding-bottom
   para que no tape el footer, el copy-fab ni los toasts.
============================================================ */
(function(){
  const cb = document.getElementById('aadsstickymwmhymdu');
  const copyFab = document.querySelector('.copy-fab');
  const toast = document.getElementById('toast');
  if(!cb) return;

  const AD_HEIGHT = 110;
  const FAB_OFFSET = AD_HEIGHT + 20;
  const TOAST_OFFSET = AD_HEIGHT + 80;

  function applyLayout(){
    const active = !cb.checked;
    document.body.style.paddingBottom = active ? AD_HEIGHT + 'px' : '20px';
    if(copyFab) copyFab.style.bottom = active ? FAB_OFFSET + 'px' : '24px';
    if(toast) toast.style.bottom = active ? TOAST_OFFSET + 'px' : '90px';
  }

  applyLayout();
  cb.addEventListener('change', applyLayout);
})();
</script>

</body>
</html>
