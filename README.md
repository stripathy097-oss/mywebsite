<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0">
<title>AKSHARA — Smruti Ranjan Tripathy</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Cormorant+Garamond:ital,wght@0,500;0,600;1,500&family=Noto+Serif:wght@400;600&family=Noto+Serif+Oriya:wght@400;600&family=IBM+Plex+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root{
    --ink:#1f160d;
    --ink-soft:#4a3a24;
    --leaf:#e4ce9c;
    --leaf-dim:#d8be85;
    --leaf-line:rgba(31,22,13,0.14);
    --rust:#a8412b;
    --rust-deep:#8a3121;
    --gold:#b98a2e;
    --whatsapp:#25d366;
    --whatsapp-deep:#1da851;
  }
  *{box-sizing:border-box;}
  html{scroll-behavior:smooth;}
  body{
    margin:0;
    background:var(--ink);
    color:var(--leaf);
    font-family:'Noto Serif', serif;
    display:flex;
    justify-content:center;
  }
  @media (prefers-reduced-motion: reduce){
    *{animation:none !important; transition-duration:0.001ms !important;}
  }
  .lang-or{ font-family:'Noto Serif Oriya', serif; }
  #app{ width:100%; max-width:920px; min-height:100vh; position:relative; }

  /* ---------- HERO ---------- */
  header.hero{
    padding:64px 28px 44px;
    text-align:center;
  }
  .emblem{ width:76px; height:76px; margin:0 auto 22px; }
  .emblem svg{ width:100%; height:100%; animation:spin 60s linear infinite; }
  @keyframes spin{ from{transform:rotate(0deg);} to{transform:rotate(360deg);} }

  .brand{
    font-family:'Cormorant Garamond', serif;
    font-weight:600;
    font-size:3.4rem;
    letter-spacing:0.06em;
    margin:0;
    color:var(--leaf);
    outline:none;
  }
  .brand:focus{ box-shadow:0 0 0 2px var(--gold); border-radius:6px; }
  .byline{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.78rem;
    letter-spacing:0.08em;
    text-transform:uppercase;
    color:var(--gold);
    margin-top:10px;
    outline:none;
  }
  .byline:focus{ box-shadow:0 0 0 2px var(--gold); border-radius:4px; }
  .tagline{
    font-family:'Cormorant Garamond', serif;
    font-style:italic;
    font-size:1.25rem;
    color:var(--leaf-dim);
    margin-top:16px;
    outline:none;
  }
  .tagline.lang-or{ font-style:normal; font-size:1.1rem; }
  .tagline:focus{ box-shadow:0 0 0 2px var(--gold); border-radius:4px; }

  .lang-pills{
    display:flex; justify-content:center; gap:10px; margin-top:30px; flex-wrap:wrap;
  }
  .pill{
    font-family:'IBM Plex Mono', monospace;
    font-size:0.75rem;
    padding:8px 18px;
    border-radius:100px;
    border:1px solid rgba(228,206,156,0.35);
    background:transparent;
    color:var(--leaf-dim);
    cursor:pointer;
    min-height:38px;
  }
  .pill.active{ background:var(--gold); color:var(--ink); border-color:var(--gold); font-weight:600; }

  .etched-rule{
    width:100%; max-width:920px; margin:0 auto;
    border:none; height:6px;
    background-image:repeating-linear-gradient(90deg, var(--leaf-line) 0 2px, transparent 2px 10px);
    opacity:0.6;
  }

  /* ---------- MAIN PANEL ---------- */
  main{
    background:var(--leaf);
    color:var(--ink);
    border-radius:32px 32px 0 0;
    padding:34px 26px 100px;
    box-shadow:0 -10px 34px rgba(0,0,0,0.3);
  }
  .toolbar{
    display:flex; justify-content:space-between; align-items:center; margin-bottom:24px; flex-wrap:wrap; gap:10px;
  }
  .count{ font-family:'IBM Plex Mono', monospace; font-size:0.75rem; color:var(--ink-soft); }
  button{ font-family:'Noto Serif', serif; cursor:pointer; border:none; border-radius:100px; }
  .btn-primary{
    background:var(--ink); color:var(--leaf); font-weight:600; font-size:0.9rem;
    padding:12px 22px; min-height:44px;
  }
  .btn-primary:active{ background:var(--ink-soft); }
  .btn-ghost{
    background:transparent; color:var(--ink); font-weight:600; font-size:0.85rem;
    padding:10px 6px; min-height:44px; display:flex; align-items:center; gap:6px;
  }
  .icon-btn{
    background:var(--leaf-dim); width:42px; height:42px; border-radius:50%;
    display:flex; align-items:center; justify-content:center; font-size:1.1rem;
  }
  button:focus-visible, [contenteditable]:focus-visible, textarea:focus-visible, input:focus-visible, select:focus-visible{
    outline:2px solid var(--rust); outline-offset:2px;
  }

  /* Entry cards */
  .entry{
    background:#fbf5e4; border:1px solid var(--leaf-line); border-radius:20px;
    padding:22px 22px 16px; margin-bottom:18px;
  }
  .entry-meta{
    display:flex; justify-content:space-between; align-items:center;
    font-family:'IBM Plex Mono', monospace; font-size:0.7rem; color:var(--rust-deep);
    margin-bottom:10px;
  }
  .lang-tag{
    padding:3px 10px; border-radius:100px; background:var(--rust); color:#fff; font-weight:600; font-size:0.65rem; letter-spacing:0.04em;
  }
  .lang-tag.or{ background:var(--gold); }
  .entry h2{
    font-family:'Cormorant Garamond', serif; font-weight:600; font-size:1.7rem;
    margin:0 0 10px; line-height:1.2;
  }
  .entry h2.lang-or{ font-family:'Noto Serif Oriya', serif; font-size:1.4rem; font-weight:600; }
  .entry p{ font-size:0.95rem; line-height:1.6; color:#3a2c19; margin:0 0 16px; white-space:pre-wrap; }
  .entry-actions{ display:flex; gap:10px; align-items:center; flex-wrap:wrap; }
  .share-btn{
    background:var(--whatsapp); color:#fff; font-weight:600; font-size:0.8rem;
    padding:9px 14px; display:flex; align-items:center; gap:6px; min-height:40px; text-decoration:none;
  }
  .share-btn:active{ background:var(--whatsapp-deep); }
  .delete-btn{ color:var(--rust-deep); background:none; font-size:0.8rem; font-weight:600; padding:8px; min-height:40px; }

  .empty{ text-align:center; padding:60px 10px; color:var(--ink-soft); }
  .empty .glyph{ font-size:2.4rem; margin-bottom:12px; }
  .empty p{ font-family:'Cormorant Garamond', serif; font-style:italic; font-size:1.2rem; }

  /* Write view */
  .write-view input[type="text"], .write-view textarea, .write-view select{
    width:100%; border:1px solid var(--leaf-line); border-radius:12px; padding:13px 15px;
    font-size:0.95rem; background:#fbf5e4; color:var(--ink); margin-bottom:14px; font-family:'Noto Serif', serif;
  }
  .write-view input[type="text"]{ font-family:'Cormorant Garamond', serif; font-size:1.3rem; font-weight:600; }
  .write-view textarea{ min-height:240px; resize:vertical; line-height:1.6; }
  .write-top{ display:flex; align-items:center; gap:10px; margin-bottom:20px; }
  .write-top h3{ font-family:'Cormorant Garamond', serif; font-size:1.25rem; margin:0; }
  .lang-select-row{ display:flex; gap:10px; margin-bottom:16px; }
  .lang-select-row button{
    flex:1; padding:11px; border:1px solid var(--leaf-line); background:transparent; color:var(--ink-soft); font-weight:600; font-size:0.85rem; border-radius:10px;
  }
  .lang-select-row button.active{ background:var(--ink); color:var(--leaf); border-color:var(--ink); }

  /* Detail view */
  .detail-top{ display:flex; align-items:center; gap:10px; margin-bottom:20px; }
  .detail h2{ font-family:'Cormorant Garamond', serif; font-size:2rem; margin:16px 0 6px; }
  .detail h2.lang-or{ font-family:'Noto Serif Oriya', serif; font-size:1.7rem; }
  .detail .entry-meta{ margin-bottom:18px; }
  .detail p{ font-size:1rem; line-height:1.75; color:#2c2013; white-space:pre-wrap; margin-bottom:26px; }

  /* About / footer */
  .about{
    margin-top:36px; padding-top:30px; border-top:1px dashed var(--leaf-line);
  }
  .about h3{ font-family:'IBM Plex Mono', monospace; font-size:0.72rem; text-transform:uppercase; letter-spacing:0.08em; color:var(--rust-deep); margin:0 0 10px; }
  .about p{ font-size:0.92rem; line-height:1.6; color:#3a2c19; outline:none; }
  .about p:focus{ box-shadow:0 0 0 2px var(--gold); border-radius:4px; }
  footer.site-footer{
    text-align:center; margin-top:40px; font-family:'IBM Plex Mono', monospace; font-size:0.68rem; color:var(--ink-soft);
  }

  /* Floating WhatsApp */
  .wa-float{
    position:fixed; bottom:24px; right:calc(50% - 460px + 24px);
    width:58px; height:58px; border-radius:50%; background:var(--whatsapp);
    display:flex; align-items:center; justify-content:center; box-shadow:0 6px 18px rgba(0,0,0,0.3); z-index:20;
  }
  @media (max-width:968px){ .wa-float{ right:24px; } }
  .wa-float svg{ width:29px; height:29px; }

  /* Settings sheet */
  .sheet-overlay{
    position:fixed; inset:0; background:rgba(31,22,13,0.6); display:none;
    align-items:flex-end; justify-content:center; z-index:30;
  }
  .sheet-overlay.open{ display:flex; }
  .sheet{ background:var(--leaf); width:100%; max-width:520px; border-radius:24px 24px 0 0; padding:26px 24px 32px; }
  .sheet h3{ font-family:'Cormorant Garamond', serif; margin:0 0 4px; font-size:1.3rem; }
  .sheet p.note{ font-size:0.8rem; color:var(--ink-soft); margin:0 0 18px; }
  .sheet label{ font-family:'IBM Plex Mono', monospace; font-size:0.7rem; color:var(--ink-soft); display:block; margin-bottom:6px; }
  .sheet input{
    width:100%; padding:12px 14px; border-radius:10px; border:1px solid var(--leaf-line);
    font-family:'Noto Serif', serif; font-size:0.95rem; margin-bottom:16px; background:#fbf5e4; color:var(--ink);
  }
  .sheet-actions{ display:flex; gap:10px; }
  .toast{
    position:fixed; top:20px; left:50%; transform:translateX(-50%); background:var(--ink); color:var(--leaf);
    padding:10px 18px; border-radius:100px; font-size:0.85rem; z-index:50; opacity:0; pointer-events:none; transition:opacity 0.25s;
  }
  .toast.show{ opacity:1; }
  .hidden{ display:none !important; }
</style>
</head>
<body>
<div id="app">

  <header class="hero">
    <div class="emblem" aria-hidden="true">
      <svg viewBox="0 0 100 100" fill="none">
        <circle cx="50" cy="50" r="46" stroke="#b98a2e" stroke-width="2"/>
        <circle cx="50" cy="50" r="6" fill="#a8412b"/>
        <g stroke="#e4ce9c" stroke-width="1.6">
          <line x1="50" y1="6" x2="50" y2="94"/>
          <line x1="6" y1="50" x2="94" y2="50"/>
          <line x1="16" y1="16" x2="84" y2="84"/>
          <line x1="84" y1="16" x2="16" y2="84"/>
          <line x1="50" y1="16" x2="50" y2="84" transform="rotate(22.5 50 50)"/>
          <line x1="50" y1="16" x2="50" y2="84" transform="rotate(67.5 50 50)"/>
          <line x1="50" y1="16" x2="50" y2="84" transform="rotate(112.5 50 50)"/>
          <line x1="50" y1="16" x2="50" y2="84" transform="rotate(157.5 50 50)"/>
        </g>
      </svg>
    </div>
    <h1 class="brand" id="brandTitle" contenteditable="true" spellcheck="false">AKSHARA</h1>
    <div class="byline" id="authorName" contenteditable="true" spellcheck="false">by Smruti Ranjan Tripathy</div>
    <div class="tagline" id="tagline" contenteditable="true" spellcheck="false">words, kept like letters on a palm leaf</div>

    <div class="lang-pills">
      <button class="pill active" data-filter="all">All</button>
      <button class="pill" data-filter="en">English</button>
      <button class="pill" data-filter="or">ଓଡ଼ିଆ</button>
    </div>
  </header>

  <hr class="etched-rule">

  <main>
    <!-- LIST VIEW -->
    <div id="listView">
      <div class="toolbar">
        <span class="count" id="entryCount">0 entries</span>
        <div style="display:flex; gap:8px; align-items:center;">
          <button class="icon-btn" id="settingsBtn" aria-label="Settings">⚙️</button>
          <button class="btn-primary" id="newEntryBtn">✎ Write</button>
        </div>
      </div>
      <div id="entriesList"></div>
      <div id="emptyState" class="empty hidden">
        <div class="glyph">ॐ</div>
        <p>No letters written yet.<br>Begin the first one.</p>
      </div>

      <div class="about">
        <h3>About</h3>
        <p id="aboutText" contenteditable="true" spellcheck="false">Smruti Ranjan Tripathy writes here in Odia and English — on work, family, money, and the small things worth remembering.</p>
      </div>
      <footer class="site-footer">AKSHARA · a personal journal · tap text above to edit</footer>
    </div>

    <!-- WRITE VIEW -->
    <div id="writeView" class="write-view hidden">
      <div class="write-top">
        <button class="btn-ghost" id="cancelWriteBtn">← Back</button>
        <h3>New letter</h3>
      </div>
      <div class="lang-select-row">
        <button type="button" class="lang-choice active" data-lang="en">English</button>
        <button type="button" class="lang-choice" data-lang="or">ଓଡ଼ିଆ</button>
      </div>
      <input type="text" id="postTitleInput" placeholder="Title">
      <textarea id="postBodyInput" placeholder="Write what's on your mind..."></textarea>
      <button class="btn-primary" id="publishBtn" style="width:100%;">Publish</button>
    </div>

    <!-- DETAIL VIEW -->
    <div id="detailView" class="hidden">
      <div class="detail-top">
        <button class="btn-ghost" id="backFromDetailBtn">← Back</button>
      </div>
      <div class="detail" id="detailContent"></div>
    </div>
  </main>

  <a class="wa-float" id="waFloat" href="#" target="_blank" rel="noopener" aria-label="Chat on WhatsApp">
    <svg viewBox="0 0 32 32" fill="white"><path d="M16.001 3C9.101 3 3.5 8.6 3.5 15.5c0 2.43.71 4.69 1.93 6.6L3 29l7.09-2.37a12.44 12.44 0 0 0 5.9 1.5h.01c6.9 0 12.5-5.6 12.5-12.5S22.9 3 16.001 3zm0 22.7h-.01a10.2 10.2 0 0 1-5.2-1.43l-.37-.22-3.75 1.25 1.26-3.66-.24-.38a10.15 10.15 0 0 1-1.56-5.46c0-5.62 4.58-10.2 10.2-10.2a10.14 10.14 0 0 1 7.21 2.99 10.14 10.14 0 0 1 2.99 7.21c0 5.62-4.58 10.2-10.2 10.2zm5.6-7.64c-.31-.15-1.82-.9-2.1-1-.28-.1-.49-.15-.69.16-.2.3-.79 1-.97 1.2-.18.2-.36.23-.67.08-.31-.16-1.3-.48-2.48-1.53-.92-.82-1.54-1.83-1.72-2.14-.18-.31-.02-.47.13-.63.14-.14.31-.36.46-.54.16-.18.2-.31.31-.51.1-.2.05-.39-.03-.54-.08-.16-.69-1.66-.95-2.28-.25-.6-.5-.52-.69-.53-.18-.01-.39-.01-.6-.01-.2 0-.54.08-.82.39-.28.31-1.08 1.05-1.08 2.56 0 1.51 1.1 2.97 1.26 3.17.15.2 2.17 3.32 5.27 4.65.74.32 1.31.51 1.76.65.74.24 1.41.2 1.94.12.59-.09 1.82-.74 2.08-1.46.26-.72.26-1.33.18-1.46-.08-.13-.28-.2-.59-.35z"/></svg>
  </a>

  <div class="sheet-overlay" id="sheetOverlay">
    <div class="sheet">
      <h3>Settings</h3>
      <p class="note">Your WhatsApp number connects the chat button and share links. Kept only in this journal.</p>
      <label for="waNumberInput">WhatsApp number (with country code, digits only)</label>
      <input type="text" id="waNumberInput" placeholder="e.g. 91XXXXXXXXXX">
      <div class="sheet-actions">
        <button class="btn-primary" id="saveSettingsBtn" style="flex:1;">Save</button>
        <button class="btn-ghost" id="closeSettingsBtn">Close</button>
      </div>
    </div>
  </div>

  <div class="toast" id="toast"></div>
</div>

<script>
(function(){
  const META_KEY = 'akshara-meta';
  const POSTS_KEY = 'akshara-posts';
  let posts = [];
  let meta = { waNumber: "" };
  let filter = 'all';
  let writeLang = 'en';

  const $ = (id) => document.getElementById(id);
  const listView = $('listView'), writeView = $('writeView'), detailView = $('detailView');
  const entriesList = $('entriesList'), emptyState = $('emptyState'), entryCount = $('entryCount');
  const toast = $('toast');

  function showToast(msg){
    toast.textContent = msg;
    toast.classList.add('show');
    setTimeout(()=>toast.classList.remove('show'), 1800);
  }

  function view(name){
    listView.classList.add('hidden');
    writeView.classList.add('hidden');
    detailView.classList.add('hidden');
    if(name==='list') listView.classList.remove('hidden');
    if(name==='write') writeView.classList.remove('hidden');
    if(name==='detail') detailView.classList.remove('hidden');
  }

  function formatDate(ts){
    return new Date(ts).toLocaleDateString('en-IN', { day:'numeric', month:'short', year:'numeric' });
  }
  function excerpt(text){
    const clean = text.trim();
    return clean.length > 150 ? clean.slice(0,150).trim() + '…' : clean;
  }
  function waLink(number){
    const digits = (number||'').replace(/[^0-9]/g,'');
    return digits ? `https://wa.me/${digits}` : '#';
  }
  function shareUrl(post){
    const text = `AKSHARA · Smruti Ranjan Tripathy\n\n"${post.title}"\n\n${excerpt(post.body)}`;
    return `https://wa.me/?text=${encodeURIComponent(text)}`;
  }
  function escapeHtml(str){
    const d = document.createElement('div');
    d.textContent = str;
    return d.innerHTML;
  }

  async function loadAll(){
    try{
      const m = await window.storage.get(META_KEY, false);
      if(m && m.value) meta = JSON.parse(m.value);
    }catch(e){}
    try{
      const p = await window.storage.get(POSTS_KEY, false);
      if(p && p.value) posts = JSON.parse(p.value);
    }catch(e){ posts = []; }

    $('waNumberInput').value = meta.waNumber || '';
    $('waFloat').href = waLink(meta.waNumber);
    renderList();
  }

  async function saveMeta(){
    try{ await window.storage.set(META_KEY, JSON.stringify(meta), false); }
    catch(e){ showToast("Couldn't save settings"); }
    $('waFloat').href = waLink(meta.waNumber);
  }
  async function savePosts(){
    try{ await window.storage.set(POSTS_KEY, JSON.stringify(posts), false); }
    catch(e){ showToast("Couldn't save entry"); }
  }

  function renderList(){
    entriesList.innerHTML = '';
    const visible = posts.filter(p => filter==='all' || p.lang===filter);
    if(visible.length === 0){
      emptyState.classList.remove('hidden');
      entryCount.textContent = `${posts.length} ${posts.length===1?'entry':'entries'}`;
      return;
    }
    emptyState.classList.add('hidden');
    entryCount.textContent = `${posts.length} ${posts.length===1?'entry':'entries'}`;

    const sorted = [...visible].sort((a,b)=>b.createdAt - a.createdAt);
    sorted.forEach((post)=>{
      const isOr = post.lang === 'or';
      const card = document.createElement('div');
      card.className = 'entry';
      card.innerHTML = `
        <div class="entry-meta">
          <span class="lang-tag ${isOr?'or':''}">${isOr?'ଓଡ଼ିଆ':'ENGLISH'}</span>
          <span>${formatDate(post.createdAt)}</span>
        </div>
        <h2 class="${isOr?'lang-or':''}">${escapeHtml(post.title)}</h2>
        <p class="${isOr?'lang-or':''}">${escapeHtml(excerpt(post.body))}</p>
        <div class="entry-actions">
          <button class="btn-ghost read-btn" data-id="${post.id}">Read →</button>
          <a class="share-btn" href="${shareUrl(post)}" target="_blank" rel="noopener">
            <svg width="14" height="14" viewBox="0 0 32 32" fill="white"><path d="M16.001 3C9.101 3 3.5 8.6 3.5 15.5c0 2.43.71 4.69 1.93 6.6L3 29l7.09-2.37a12.44 12.44 0 0 0 5.9 1.5h.01c6.9 0 12.5-5.6 12.5-12.5S22.9 3 16.001 3z"/></svg>
            Share
          </a>
          <button class="delete-btn" data-id="${post.id}">Delete</button>
        </div>
      `;
      entriesList.appendChild(card);
    });

    entriesList.querySelectorAll('.read-btn').forEach(btn=>{
      btn.addEventListener('click', ()=>openDetail(btn.dataset.id));
    });
    entriesList.querySelectorAll('.delete-btn').forEach(btn=>{
      btn.addEventListener('click', ()=>deletePost(btn.dataset.id));
    });
  }

  function openDetail(id){
    const post = posts.find(p=>p.id===id);
    if(!post) return;
    const isOr = post.lang === 'or';
    $('detailContent').innerHTML = `
      <div class="entry-meta">
        <span class="lang-tag ${isOr?'or':''}">${isOr?'ଓଡ଼ିଆ':'ENGLISH'}</span>
        <span>${formatDate(post.createdAt)}</span>
      </div>
      <h2 class="${isOr?'lang-or':''}">${escapeHtml(post.title)}</h2>
      <p class="${isOr?'lang-or':''}">${escapeHtml(post.body)}</p>
      <a class="share-btn" href="${shareUrl(post)}" target="_blank" rel="noopener">
        <svg width="14" height="14" viewBox="0 0 32 32" fill="white"><path d="M16.001 3C9.101 3 3.5 8.6 3.5 15.5c0 2.43.71 4.69 1.93 6.6L3 29l7.09-2.37a12.44 12.44 0 0 0 5.9 1.5h.01c6.9 0 12.5-5.6 12.5-12.5S22.9 3 16.001 3z"/></svg>
        Share on WhatsApp
      </a>
    `;
    view('detail');
  }

  async function deletePost(id){
    posts = posts.filter(p=>p.id!==id);
    await savePosts();
    renderList();
    showToast('Entry deleted');
  }

  document.querySelectorAll('.pill').forEach(pill=>{
    pill.addEventListener('click', ()=>{
      document.querySelectorAll('.pill').forEach(p=>p.classList.remove('active'));
      pill.classList.add('active');
      filter = pill.dataset.filter;
      renderList();
    });
  });

  document.querySelectorAll('.lang-choice').forEach(btn=>{
    btn.addEventListener('click', ()=>{
      document.querySelectorAll('.lang-choice').forEach(b=>b.classList.remove('active'));
      btn.classList.add('active');
      writeLang = btn.dataset.lang;
      const titleEl = $('postTitleInput'), bodyEl = $('postBodyInput');
      if(writeLang==='or'){
        titleEl.style.fontFamily = "'Noto Serif Oriya', serif";
        bodyEl.style.fontFamily = "'Noto Serif Oriya', serif";
        titleEl.placeholder = 'ଶୀର୍ଷକ';
        bodyEl.placeholder = 'ଆପଣଙ୍କ ମନରେ ଥିବା କଥା ଲେଖନ୍ତୁ...';
      }else{
        titleEl.style.fontFamily = "'Cormorant Garamond', serif";
        bodyEl.style.fontFamily = "'Noto Serif', serif";
        titleEl.placeholder = 'Title';
        bodyEl.placeholder = "Write what's on your mind...";
      }
    });
  });

  $('newEntryBtn').addEventListener('click', ()=>{
    $('postTitleInput').value = '';
    $('postBodyInput').value = '';
    view('write');
  });
  $('cancelWriteBtn').addEventListener('click', ()=>view('list'));
  $('backFromDetailBtn').addEventListener('click', ()=>view('list'));

  $('publishBtn').addEventListener('click', async ()=>{
    const title = $('postTitleInput').value.trim();
    const body = $('postBodyInput').value.trim();
    if(!title || !body){ showToast(writeLang==='or' ? 'ଶୀର୍ଷକ ଓ କିଛି ଧାଡି ଲେଖନ୍ତୁ' : 'Add a title and a few lines first'); return; }
    posts.push({ id: 'p_'+Date.now(), title, body, lang: writeLang, createdAt: Date.now() });
    await savePosts();
    renderList();
    view('list');
    showToast(writeLang==='or' ? 'ପ୍ରକାଶିତ' : 'Published');
  });

  ['brandTitle','authorName','tagline','aboutText'].forEach(id=>{
    $(id).addEventListener('blur', async ()=>{
      // stored implicitly via DOM; also persist to meta for reload consistency
      meta.brandTitle = $('brandTitle').textContent.trim();
      meta.authorName = $('authorName').textContent.trim();
      meta.tagline = $('tagline').textContent.trim();
      meta.aboutText = $('aboutText').textContent.trim();
      await saveMeta();
    });
  });

  $('settingsBtn').addEventListener('click', ()=> $('sheetOverlay').classList.add('open'));
  $('closeSettingsBtn').addEventListener('click', ()=> $('sheetOverlay').classList.remove('open'));
  $('sheetOverlay').addEventListener('click', (e)=>{ if(e.target.id==='sheetOverlay') $('sheetOverlay').classList.remove('open'); });
  $('saveSettingsBtn').addEventListener('click', async ()=>{
    meta.waNumber = $('waNumberInput').value.trim();
    await saveMeta();
    $('sheetOverlay').classList.remove('open');
    showToast('Settings saved');
  });

  async function restoreEditableFields(){
    if(meta.brandTitle) $('brandTitle').textContent = meta.brandTitle;
    if(meta.authorName) $('authorName').textContent = meta.authorName;
    if(meta.tagline) $('tagline').textContent = meta.tagline;
    if(meta.aboutText) $('aboutText').textContent = meta.aboutText;
  }

  (async ()=>{
    await loadAll();
    restoreEditableFields();
  })();
})();
</script>
</body>
</html>
