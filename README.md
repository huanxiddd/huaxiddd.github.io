# huaxiddd.github.io
<!DOCTYPE html>
<html lang="zh-CN">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no, viewport-fit=cover" />
<meta name="format-detection" content="telephone=no" />
<meta name="theme-color" content="#07060f" />
<meta name="apple-mobile-web-app-capable" content="yes" />
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent" />
<meta name="description" content="一份小小的生日祝福" />
<title>生日快乐</title>
<style>
/* ============================================================
   可修改的配色 / 字体
   ============================================================ */
:root{
  --bg0:#07060f;
  --gold:#ffd27a;
  --pink:#ff9ec7;
  --mint:#8ff0d9;
  --text:#f6eefb;
  --muted:rgba(246,238,251,.60);
  --card:rgba(255,255,255,.065);
  --stroke:rgba(255,255,255,.14);
  --font-cn:"PingFang SC","HarmonyOS Sans SC","Source Han Sans SC","Noto Sans CJK SC","Microsoft YaHei",system-ui,-apple-system,"Helvetica Neue",sans-serif;
  --font-en:"Didot","Bodoni 72","Playfair Display","Times New Roman",Georgia,serif;
}

*{margin:0;padding:0;box-sizing:border-box;-webkit-tap-highlight-color:transparent}
html,body{height:100%;width:100%;overflow:hidden;background:var(--bg0)}
body{
  font-family:var(--font-cn);
  color:var(--text);
  -webkit-font-smoothing:antialiased;
  -moz-osx-font-smoothing:grayscale;
  -webkit-user-select:none;user-select:none;
  -webkit-touch-callout:none;
  touch-action:manipulation;
  overscroll-behavior:none;
}

/* ---------- 背景 ---------- */
#bg{
  position:fixed;top:0;left:0;right:0;bottom:0;z-index:0;
  background:
    radial-gradient(130% 90% at 50% -15%, #2b1a45 0%, #17102c 42%, #080611 100%);
}
.orb{
  position:fixed;border-radius:50%;pointer-events:none;z-index:0;
  filter:blur(48px);opacity:.40;
}
.orb.a{width:260px;height:260px;background:#ff5f9e;top:-110px;left:-80px;animation:drift 16s ease-in-out infinite alternate}
.orb.b{width:300px;height:300px;background:#5f57ff;bottom:-140px;right:-100px;animation:drift 21s ease-in-out infinite alternate-reverse}
.orb.c{width:190px;height:190px;background:#ffb665;top:38%;right:-110px;opacity:.24;animation:drift 26s ease-in-out infinite alternate}
@keyframes drift{
  from{transform:translate3d(0,0,0) scale(1)}
  to{transform:translate3d(18px,26px,0) scale(1.12)}
}
#stars{position:fixed;top:0;left:0;right:0;bottom:0;z-index:1;pointer-events:none}
#fx{position:fixed;top:0;left:0;right:0;bottom:0;z-index:6;pointer-events:none}

/* ---------- 舞台 / 场景 ---------- */
#stage{
  position:fixed;top:0;left:0;right:0;bottom:0;z-index:3;
  overflow:hidden;
}
.scene{
  position:absolute;top:0;left:0;right:0;bottom:0;
  display:flex;align-items:center;justify-content:center;
  padding:calc(38px + env(safe-area-inset-top)) 24px calc(34px + env(safe-area-inset-bottom));
  opacity:0;visibility:hidden;
  transform:translateY(16px) scale(.985);
  transition:opacity .75s ease, transform .85s cubic-bezier(.16,.8,.3,1), visibility .75s;
  overflow-y:auto;-webkit-overflow-scrolling:touch;
}
.scene.on{opacity:1;visibility:visible;transform:none}
.inner{width:100%;max-width:400px;margin:auto;text-align:center;position:relative;z-index:2}

/* ---------- 通用文字 ---------- */
.eyebrow{
  font-size:10px;letter-spacing:.34em;text-transform:uppercase;
  color:rgba(255,210,122,.85);font-weight:500;
  padding-left:.34em;margin-bottom:22px;
  white-space:nowrap;
}
.eyebrow.soft{color:var(--muted);letter-spacing:.34em}

/* ---------- 第一幕 ---------- */
.t1{
  font-size:33px;line-height:1.5;font-weight:600;letter-spacing:.02em;
  text-shadow:0 6px 30px rgba(255,120,180,.25);
}
.t1 .hl{
  color:var(--gold);
  background:linear-gradient(100deg,#ffd27a,#ffb0c9 55%,#ffd27a);
  -webkit-background-clip:text;background-clip:text;
  -webkit-text-fill-color:transparent;
  background-size:220% 100%;
  animation:shine 6s linear infinite;
}
@keyframes shine{0%{background-position:0% 0}100%{background-position:220% 0}}
.date{
  margin-top:18px;font-family:var(--font-en);font-style:italic;
  font-size:15px;letter-spacing:.22em;color:var(--muted);
}
.cta{
  margin-top:52px;display:inline-flex;flex-direction:column;align-items:center;justify-content:center;
  width:100%;max-width:250px;padding:17px 20px 14px;
  border:1px solid rgba(255,210,122,.45);border-radius:999px;
  background:linear-gradient(180deg,rgba(255,210,122,.16),rgba(255,210,122,.05));
  color:#ffe6b8;font-family:var(--font-cn);font-size:16.5px;font-weight:600;letter-spacing:.14em;
  box-shadow:0 0 0 0 rgba(255,210,122,.45), 0 14px 34px rgba(255,150,90,.14), inset 0 1px 0 rgba(255,255,255,.16);
  animation:pulse 2.6s ease-out infinite;
  cursor:pointer;
  -webkit-appearance:none;appearance:none;
}
.cta:active{transform:scale(.975);transition:transform .12s}
.cta small{
  display:block;margin-top:5px;font-size:10.5px;letter-spacing:.28em;
  color:rgba(255,214,168,.62);font-weight:400;padding-left:.28em;
}
@keyframes pulse{
  0%{box-shadow:0 0 0 0 rgba(255,210,122,.38), 0 14px 34px rgba(255,150,90,.14)}
  70%{box-shadow:0 0 0 18px rgba(255,210,122,0), 0 14px 34px rgba(255,150,90,.14)}
  100%{box-shadow:0 0 0 0 rgba(255,210,122,0), 0 14px 34px rgba(255,150,90,.14)}
}

/* ---------- 第二幕：蛋糕 ---------- */
.hint-top{
  font-size:13px;letter-spacing:.3em;color:rgba(255,255,255,.72);
  padding-left:.3em;margin-bottom:6px;
}
.hint-top b{color:var(--gold);font-weight:600}

.cake-wrap{
  margin:34px auto 0;width:100%;height:300px;position:relative;
  display:flex;align-items:flex-end;justify-content:center;
  transform-origin:50% 100%;
}
.cake{position:relative;width:236px;height:252px}

.cake-glow{
  position:absolute;left:50%;bottom:96px;width:230px;height:230px;
  transform:translateX(-50%);
  background:radial-gradient(circle, rgba(255,168,72,.34) 0%, rgba(255,120,60,.12) 42%, rgba(255,120,60,0) 70%);
  animation:breathe 3.4s ease-in-out infinite;
  pointer-events:none;
}
@keyframes breathe{0%,100%{opacity:.75;transform:translateX(-50%) scale(1)}50%{opacity:1;transform:translateX(-50%) scale(1.08)}}

.plate{
  position:absolute;left:50%;bottom:0;transform:translateX(-50%);
  width:238px;height:24px;border-radius:50%;
  background:radial-gradient(ellipse at 50% 26%,#f2f0ff 0%,#b9b3d9 52%,#6d678f 100%);
  box-shadow:0 22px 34px rgba(0,0,0,.5), 0 6px 0 rgba(0,0,0,.18);
}

.tier{
  position:absolute;left:50%;transform:translateX(-50%);
  border-radius:10px 10px 9px 9px;
  background:linear-gradient(180deg,#fde8cf 0%,#f6d3b1 52%,#e5b590 100%);
  box-shadow:inset 0 -10px 16px rgba(176,116,74,.20), inset 6px 0 10px rgba(255,255,255,.30), 0 12px 22px rgba(0,0,0,.30);
}
.tier-bot{width:190px;height:68px;bottom:16px}
.tier-top{width:124px;height:56px;bottom:84px}
/* 奶油 */
.tier::before{
  content:"";position:absolute;top:-1px;left:0;right:0;height:20px;
  background:
    linear-gradient(#fffaf4,#fff3e8) top left/100% 9px no-repeat,
    radial-gradient(circle at 11px 9px,#fffaf4 8.6px,rgba(255,250,244,0) 9.4px) 0 0/22px 20px repeat-x;
}
/* 草莓点缀 */
.tier::after{
  content:"";position:absolute;left:8px;right:8px;top:22px;height:8px;opacity:.75;
  background:
    radial-gradient(circle at 4px 4px,#ff7f9f 3.4px,transparent 3.8px) 0 0/34px 8px repeat-x;
}

.candles{
  position:absolute;left:50%;bottom:138px;transform:translateX(-50%);
  display:flex;align-items:flex-end;gap:16px;
}
.candle{
  position:relative;width:14px;height:48px;
  cursor:pointer;
}
.candle .stick{
  position:absolute;left:50%;bottom:0;transform:translateX(-50%);
  width:8px;height:38px;border-radius:3px;
  background:repeating-linear-gradient(48deg,#ff9dc2 0 5px,#fff2f7 5px 10px);
  box-shadow:inset -2px 0 3px rgba(120,40,70,.22), 0 2px 6px rgba(0,0,0,.25);
}
.candle .wick{
  position:absolute;left:50%;bottom:37px;transform:translateX(-50%);
  width:1.5px;height:6px;border-radius:1px;background:#3a2b33;
}
.flame{
  position:absolute;left:50%;bottom:41px;
  width:14px;height:22px;margin-left:-7px;
  border-radius:50% 50% 46% 46%/64% 64% 36% 36%;
  background:radial-gradient(ellipse at 50% 76%,#fffdf0 0%,#ffe9a8 26%,#ffbe55 55%,#ff7b28 80%,rgba(255,110,20,0) 100%);
  box-shadow:0 0 14px 3px rgba(255,178,72,.62), 0 0 40px 14px rgba(255,120,20,.26);
  transform-origin:50% 100%;
  animation:flick .85s ease-in-out infinite alternate;
  transition:opacity .3s ease, transform .3s ease;
}
.flame i{
  position:absolute;left:50%;bottom:2px;width:5px;height:9px;margin-left:-2.5px;
  border-radius:50% 50% 40% 40%;background:rgba(255,255,255,.85);
  filter:blur(1px);
}
@keyframes flick{
  0%{transform:scale(1,.96) rotate(-2.2deg);opacity:.92}
  40%{transform:scale(1.04,1.06) rotate(1.4deg);opacity:1}
  100%{transform:scale(.97,1.02) rotate(2.4deg);opacity:.95}
}
.candle.out .flame{opacity:0;transform:scale(.15) translateY(6px)}
.candle.out .wick{background:#221a20}

.smoke{
  position:absolute;left:50%;bottom:44px;width:12px;height:12px;margin-left:-6px;
  border-radius:50%;
  background:radial-gradient(circle,rgba(226,224,240,.55) 0%,rgba(226,224,240,0) 72%);
  opacity:0;pointer-events:none;
}
.smoke.go{animation:smoke 1.9s ease-out forwards}
@keyframes smoke{
  0%{opacity:.85;transform:translateY(0) scale(.55)}
  55%{opacity:.45}
  100%{opacity:0;transform:translateY(-58px) scale(2.4)}
}

.tip{
  margin-top:26px;font-size:12.5px;letter-spacing:.12em;color:rgba(255,255,255,.55);
  line-height:1.9;
}
.ghost{
  margin-top:20px;display:inline-block;padding:12px 26px;
  border:1px solid rgba(255,255,255,.20);border-radius:999px;
  background:rgba(255,255,255,.06);color:rgba(255,255,255,.86);
  font-family:var(--font-cn);font-size:13.5px;letter-spacing:.16em;padding-left:calc(26px + .16em);
  -webkit-appearance:none;appearance:none;cursor:pointer;
}
.ghost:active{transform:scale(.97);background:rgba(255,255,255,.12)}
.ghost[disabled]{opacity:.45}
.mic-bar{
  margin:16px auto 0;width:132px;height:34px;border-radius:999px;
  background:rgba(255,255,255,.05);position:relative;overflow:hidden;
  display:none;align-items:center;justify-content:center;gap:3px;
}
.mic-bar.on{display:flex}
.mic-bar span{
  display:block;width:3px;height:6px;border-radius:2px;background:rgba(255,255,255,.35);
  transition:height .08s linear, background .2s;
}

/* ---------- 第三幕 ---------- */
.big-en{
  font-family:var(--font-en);font-style:italic;
  font-size:40px;line-height:1.1;letter-spacing:.02em;
  background:linear-gradient(96deg,#ffe6b0 0%,#ffb0cd 42%,#cfc2ff 72%,#ffe6b0 100%);
  -webkit-background-clip:text;background-clip:text;
  -webkit-text-fill-color:transparent;
  background-size:240% 100%;
  animation:shine 9s linear infinite;
  padding:4px 0 8px;
  filter:drop-shadow(0 8px 24px rgba(255,140,190,.22));
}
.who{
  margin-top:14px;font-size:19px;font-weight:600;letter-spacing:.16em;
  color:rgba(255,255,255,.94);padding-left:.16em;
}
.who em{
  font-style:normal;color:var(--gold);
  text-shadow:0 0 22px rgba(255,190,90,.45);
}
.rule{
  margin:26px auto;width:72px;height:1px;
  background:linear-gradient(90deg,transparent,rgba(255,210,122,.6),transparent);
  position:relative;
}
.rule::after{
  content:"✦";position:absolute;left:50%;top:50%;transform:translate(-50%,-50%);
  font-size:9px;color:rgba(255,210,122,.9);background:transparent;
  text-shadow:0 0 8px rgba(0,0,0,.6);
}
.message{min-height:104px}
.message p{
  font-size:15px;line-height:2.15;letter-spacing:.1em;
  color:rgba(255,255,255,.86);margin-bottom:2px;
}
.caret{
  display:inline-block;width:1px;height:1em;vertical-align:-.12em;
  background:rgba(255,210,122,.9);margin-left:2px;
  animation:blink .9s steps(1) infinite;
}
@keyframes blink{50%{opacity:0}}
.from{
  margin-top:30px;font-size:12.5px;letter-spacing:.2em;color:rgba(255,255,255,.5);
  opacity:0;transition:opacity .9s ease .2s;
}
.from.on{opacity:1}
.from b{color:rgba(255,210,122,.9);font-weight:500;letter-spacing:.2em}
.again{
  margin-top:34px;display:inline-flex;align-items:center;gap:8px;
  padding:11px 22px;border-radius:999px;
  border:1px solid rgba(255,255,255,.16);background:rgba(255,255,255,.05);
  color:rgba(255,255,255,.72);font-family:var(--font-cn);font-size:12.5px;letter-spacing:.14em;
  -webkit-appearance:none;appearance:none;cursor:pointer;
  opacity:0;transition:opacity .9s ease .5s;
}
.again.on{opacity:1}
.again:active{background:rgba(255,255,255,.11)}
.again svg{width:13px;height:13px;fill:currentColor;opacity:.8}

/* ---------- 音效开关 ---------- */
#snd{
  position:fixed;top:calc(14px + env(safe-area-inset-top));right:calc(14px + env(safe-area-inset-right));
  z-index:12;width:38px;height:38px;border-radius:50%;
  display:flex;align-items:center;justify-content:center;
  border:1px solid rgba(255,255,255,.14);background:rgba(255,255,255,.06);
  color:rgba(255,255,255,.72);cursor:pointer;
  -webkit-appearance:none;appearance:none;
  opacity:0;transition:opacity .6s ease;
}
#snd.on{opacity:1}
#snd svg{width:16px;height:16px;fill:currentColor}
#snd .off{display:none}
#snd.muted .on-i{display:none}
#snd.muted .off{display:block}

/* ---------- 提示条 ---------- */
#toast{
  position:fixed;left:50%;bottom:calc(38px + env(safe-area-inset-bottom));transform:translate(-50%,14px);
  z-index:20;padding:11px 20px;border-radius:999px;
  background:rgba(20,16,32,.9);border:1px solid rgba(255,255,255,.12);
  color:rgba(255,255,255,.86);font-size:12.5px;letter-spacing:.06em;
  opacity:0;pointer-events:none;transition:opacity .35s, transform .35s;
  max-width:86vw;text-align:center;line-height:1.6;
}
#toast.on{opacity:1;transform:translate(-50%,0)}

/* ---------- 小屏适配 ---------- */
@media (max-height:667px){
  .t1{font-size:28px}
  .cta{margin-top:36px}
  .cake-wrap{height:262px;margin-top:18px;transform:scale(.9)}
  .big-en{font-size:34px}
  .message p{font-size:14px;line-height:2}
  .eyebrow{margin-bottom:16px}
}
@media (max-height:600px){
  .cake-wrap{transform:scale(.78);margin-top:6px}
}
@media (min-width:520px){
  .big-en{font-size:46px}
  .t1{font-size:38px}
}
</style>
</head>
<body>

<div id="bg"></div>
<div class="orb a"></div>
<div class="orb b"></div>
<div class="orb c"></div>
<canvas id="stars"></canvas>
<canvas id="fx"></canvas>

<div id="stage">

  <!-- ========== 第一幕 ========== -->
  <section class="scene on" id="scene1">
    <div class="inner">
      <p class="eyebrow">just for you today</p>
      <h1 class="t1">今天，是<span class="hl">你的</span>日子</h1>
      <p class="date" id="dateText">2026 · 11 · 12</p>
      <button class="cta" id="startBtn">
        点亮生日蜡烛
        <small>轻触屏幕开始</small>
      </button>
    </div>
  </section>

  <!-- ========== 第二幕：蛋糕 ========== -->
  <section class="scene" id="scene2">
    <div class="inner">
      <p class="hint-top">闭上眼，许个<b>心愿</b></p>

      <div class="cake-wrap">
        <div class="cake">
          <div class="cake-glow"></div>
          <div class="plate"></div>
          <div class="tier tier-bot"></div>
          <div class="tier tier-top"></div>
          <div class="candles" id="candles"><!-- js 生成 --></div>
        </div>
      </div>

      <p class="tip" id="blowTip">对着蜡烛吹一口气<br>或者，轻轻点一下它们</p>
      <div class="mic-bar" id="micBar"><span></span><span></span><span></span><span></span><span></span></div>
      <button class="ghost" id="micBtn">用嘴吹灭</button>
    </div>
  </section>

  <!-- ========== 第三幕：祝福 ========== -->
  <section class="scene" id="scene3">
    <div class="inner">
      <div class="big-en">Happy Birthday</div>
      <div class="who" id="who">亲爱的 <em>你</em></div>
      <div class="rule"></div>
      <div class="message" id="message"></div>
      <div class="from" id="fromLine"></div>
      <button class="again" id="againBtn">
        <svg viewBox="0 0 24 24"><path d="M12 5V2L7 6l5 4V7a5 5 0 1 1-5 5H5a7 7 0 1 0 7-7z"/></svg>
        再听一遍
      </button>
    </div>
  </section>

</div>

<button id="snd" aria-label="声音开关">
  <svg class="on-i" viewBox="0 0 24 24"><path d="M3 10v4h4l5 4V6L7 10H3zm13.5 2a4.5 4.5 0 0 0-2.5-4v8a4.5 4.5 0 0 0 2.5-4zM14 2.2v2.1a7.5 7.5 0 0 1 0 15.4v2.1a9.5 9.5 0 0 0 0-19.6z"/></svg>
  <svg class="off" viewBox="0 0 24 24"><path d="M3 10v4h4l5 4V6L7 10H3zm18.3 2-2.1-2.1-1.4 1.4 2.1 2.1-.9.9 1.4 1.4 2.1-2.1 2.1 2.1 1.4-1.4-1.5-1.5 1.5-1.5-1.4-1.4z" transform="translate(-4 0)"/></svg>
</button>

<div id="toast"></div>

<script>
(function(){
"use strict";

/* ============================================================
   ① 可以在这里改内容（也可以不改，直接用链接参数覆盖）
   ============================================================ */
var CONFIG = {
  to:        "你",                    // 收祝福的人
  from:      "",                      // 落款，留空则不显示
  date:      "",                      // 留空 = 今天
  lines: [
    "愿你所求皆如愿，所行化坦途",
    "愿你眼里有光，心中有海",
    "愿你岁岁平安，年年有今日"
  ]
};

/* ② 链接参数覆盖：?to=小明&from=阿伟&date=2026.11.12&msg=第一句|第二句 */
(function(){
  try{
    var q = new URLSearchParams(location.search);
    if(q.get("to"))   CONFIG.to   = q.get("to");
    if(q.get("from")) CONFIG.from = q.get("from");
    if(q.get("date")) CONFIG.date = q.get("date");
    if(q.get("msg"))  CONFIG.lines = q.get("msg").split("|").filter(Boolean);
  }catch(e){}
})();

var $ = function(id){ return document.getElementById(id); };
var DPR = Math.min(window.devicePixelRatio || 1, 2);
var W = 0, H = 0;

/* ============================================================
   星空背景
   ============================================================ */
var starCv = $("stars"), sctx = starCv.getContext("2d");
var stars = [], shots = [];

function buildStars(){
  stars = [];
  var n = Math.round(Math.min(120, Math.max(58, (W * H) / 5200)));
  for(var i = 0; i < n; i++){
    stars.push({
      x: Math.random() * W,
      y: Math.random() * H * 0.92,
      r: Math.random() * 1.35 + 0.35,
      a: Math.random() * 0.55 + 0.22,
      sp: Math.random() * 0.9 + 0.35,
      ph: Math.random() * Math.PI * 2
    });
  }
}

function resize(){
  W = window.innerWidth;
  H = window.innerHeight;
  [starCv, fx].forEach(function(cv){
    cv.width  = Math.floor(W * DPR);
    cv.height = Math.floor(H * DPR);
    cv.style.width  = W + "px";
    cv.style.height = H + "px";
    cv.getContext("2d").setTransform(DPR, 0, 0, DPR, 0, 0);
  });
  buildStars();
}

/* ============================================================
   粒子（彩带 / 心 / 火花 / 焰火）
   ============================================================ */
var fx = $("fx"), fctx = fx.getContext("2d");
var parts = [];
var PALETTE = ["#ffd27a", "#ff9ec7", "#8ff0d9", "#c3b6ff", "#fff1d0", "#ff7fa8"];

function pick(a){ return a[(Math.random() * a.length) | 0]; }

function addPart(p){ if(parts.length < 220) parts.push(p); }

function burstConfetti(x, y, n, power){
  n = n || 26; power = power || 1;
  for(var i = 0; i < n; i++){
    var ang = Math.random() * Math.PI * 2;
    var sp  = (Math.random() * 3.4 + 1.6) * power;
    addPart({
      t: Math.random() < 0.22 ? "heart" : "rect",
      x: x, y: y,
      vx: Math.cos(ang) * sp,
      vy: Math.sin(ang) * sp - 1.6 * power,
      g: 0.055,
      rot: Math.random() * 6.28,
      vr: (Math.random() - 0.5) * 0.24,
      w: Math.random() * 5 + 3,
      h: Math.random() * 7 + 4,
      c: pick(PALETTE),
      life: 1,
      drag: 0.988
    });
  }
}

function confettiRain(n){
  n = n || 60;
  for(var i = 0; i < n; i++){
    addPart({
      t: Math.random() < 0.25 ? "heart" : "rect",
      x: Math.random() * W,
      y: -Math.random() * H * 0.5 - 20,
      vx: (Math.random() - 0.5) * 0.9,
      vy: Math.random() * 1.4 + 0.9,
      g: 0.012,
      rot: Math.random() * 6.28,
      vr: (Math.random() - 0.5) * 0.18,
      w: Math.random() * 5 + 3,
      h: Math.random() * 8 + 4,
      c: pick(PALETTE),
      life: 1,
      drag: 1,
      sway: Math.random() * 6.28
    });
  }
}

function firework(x, y){
  var hue = pick(PALETTE);
  for(var i = 0; i < 34; i++){
    var ang = (Math.PI * 2 * i) / 34 + Math.random() * 0.12;
    var sp  = Math.random() * 3.6 + 2.2;
    addPart({
      t: "spark",
      x: x, y: y,
      vx: Math.cos(ang) * sp,
      vy: Math.sin(ang) * sp,
      g: 0.045,
      rot: 0, vr: 0,
      w: 2, h: 2,
      c: Math.random() < 0.5 ? hue : "#fff6e0",
      life: 1,
      drag: 0.955
    });
  }
}

function drawHeart(ctx, x, y, s, rot, color, alpha){
  ctx.save();
  ctx.translate(x, y);
  ctx.rotate(rot);
  ctx.scale(s / 10, s / 10);
  ctx.globalAlpha = alpha;
  ctx.fillStyle = color;
  ctx.beginPath();
  ctx.moveTo(0, 3.2);
  ctx.bezierCurveTo(-6, -2.4, -3.4, -8.4, 0, -4.4);
  ctx.bezierCurveTo(3.4, -8.4, 6, -2.4, 0, 3.2);
  ctx.closePath();
  ctx.fill();
  ctx.restore();
}

function stepParts(){
  for(var i = parts.length - 1; i >= 0; i--){
    var p = parts[i];
    p.vx *= p.drag;
    p.vy = p.vy * p.drag + p.g;
    p.x += p.vx;
    p.y += p.vy;
    p.rot += p.vr;
    if(p.t === "rect" && typeof p.sway === "number"){
      p.sway += 0.045;
      p.x += Math.sin(p.sway) * 0.5;
    }
    if(p.t === "spark") p.life -= 0.016;
    else p.life -= 0.0022;

    if(p.life <= 0 || p.y > H + 70 || p.x < -80 || p.x > W + 80){
      parts.splice(i, 1);
      continue;
    }
    var a = Math.min(1, p.life * 1.6);
    if(p.t === "heart"){
      drawHeart(fctx, p.x, p.y, p.w * 1.5, p.rot, p.c, a);
    }else if(p.t === "rect"){
      fctx.save();
      fctx.globalAlpha = a;
      fctx.translate(p.x, p.y);
      fctx.rotate(p.rot);
      fctx.fillStyle = p.c;
      fctx.fillRect(-p.w / 2, -p.h / 2, p.w, p.h);
      fctx.restore();
    }else{
      fctx.save();
      fctx.globalAlpha = a;
      fctx.fillStyle = p.c;
      fctx.beginPath();
      fctx.arc(p.x, p.y, p.w * (0.6 + p.life * 0.9), 0, 6.2832);
      fctx.fill();
      fctx.restore();
    }
  }
}

/* ============================================================
   动画主循环
   ============================================================ */
var t0 = performance.now();

function loop(now){
  var t = (now - t0) / 1000;

  /* 星星 */
  sctx.clearRect(0, 0, W, H);
  for(var i = 0; i < stars.length; i++){
    var s = stars[i];
    var tw = 0.55 + 0.45 * Math.sin(t * s.sp + s.ph);
    sctx.globalAlpha = s.a * tw;
    sctx.fillStyle = "#fff6e8";
    sctx.beginPath();
    sctx.arc(s.x, s.y, s.r, 0, 6.2832);
    sctx.fill();
    if(s.r > 1.15){
      sctx.globalAlpha = s.a * tw * 0.18;
      sctx.beginPath();
      sctx.arc(s.x, s.y, s.r * 4, 0, 6.2832);
      sctx.fill();
    }
  }
  sctx.globalAlpha = 1;

  /* 流星 */
  if(Math.random() < 0.0045 && shots.length < 2){
    shots.push({
      x: Math.random() * W * 0.8,
      y: Math.random() * H * 0.35,
      vx: 5.2 + Math.random() * 2.2,
      vy: 2.1 + Math.random() * 1.2,
      life: 1
    });
  }
  for(var k = shots.length - 1; k >= 0; k--){
    var sh = shots[k];
    sh.x += sh.vx; sh.y += sh.vy; sh.life -= 0.012;
    if(sh.life <= 0){ shots.splice(k, 1); continue; }
    var g = sctx.createLinearGradient(sh.x, sh.y, sh.x - sh.vx * 12, sh.y - sh.vy * 12);
    g.addColorStop(0, "rgba(255,240,214," + (0.85 * sh.life) + ")");
    g.addColorStop(1, "rgba(255,240,214,0)");
    sctx.strokeStyle = g;
    sctx.lineWidth = 1.6;
    sctx.beginPath();
    sctx.moveTo(sh.x, sh.y);
    sctx.lineTo(sh.x - sh.vx * 12, sh.y - sh.vy * 12);
    sctx.stroke();
  }

  /* 粒子 */
  fctx.clearRect(0, 0, W, H);
  stepParts();

  requestAnimationFrame(loop);
}

/* ============================================================
   声音：Happy Birthday（Web Audio 实时合成，不用任何音频文件）
   ============================================================ */
var actx = null, master = null, playing = null;
var muted = false;
var BEAT = 0.44;

var N = { G4:392.00, A4:440.00, B4:493.88, C5:523.25, D5:587.33, E5:659.25, F5:698.46, G5:783.99 };
var MELODY = [
  [N.G4,0.5],[N.G4,0.5],[N.A4,1],[N.G4,1],[N.C5,1],[N.B4,2],
  [N.G4,0.5],[N.G4,0.5],[N.A4,1],[N.G4,1],[N.D5,1],[N.C5,2],
  [N.G4,0.5],[N.G4,0.5],[N.G5,1],[N.E5,1],[N.C5,1],[N.B4,1],[N.A4,2],
  [N.F5,0.5],[N.F5,0.5],[N.E5,1],[N.C5,1],[N.D5,1],[N.C5,3]
];

function initAudio(){
  if(actx) return true;
  var AC = window.AudioContext || window.webkitAudioContext;
  if(!AC) return false;
  try{
    actx = new AC();
    master = actx.createGain();
    master.gain.value = 0.9;

    /* 简易混响：用噪声生成衰减脉冲响应，让声音不干 */
    var conv = actx.createConvolver();
    var len = Math.floor(actx.sampleRate * 2.2);
    var buf = actx.createBuffer(2, len, actx.sampleRate);
    for(var ch = 0; ch < 2; ch++){
      var d = buf.getChannelData(ch);
      for(var i = 0; i < len; i++){
        d[i] = (Math.random() * 2 - 1) * Math.pow(1 - i / len, 2.6) * 0.6;
      }
    }
    conv.buffer = buf;
    var wet = actx.createGain();
    wet.gain.value = 0.26;
    master.connect(conv);
    conv.connect(wet);
    wet.connect(actx.destination);
    master.connect(actx.destination);
    return true;
  }catch(e){
    actx = null;
    return false;
  }
}

function tone(freq, at, dur, vol, type){
  if(!actx || muted) return;
  var g = actx.createGain();
  var o1 = actx.createOscillator();
  var o2 = actx.createOscillator();
  var g2 = actx.createGain();
  o1.type = type || "triangle";
  o1.frequency.value = freq;
  o2.type = "sine";
  o2.frequency.value = freq * 2.005;
  g2.gain.value = 0.13;
  o1.connect(g);
  o2.connect(g2);
  g2.connect(g);
  g.connect(master);

  var v = vol == null ? 0.20 : vol;
  g.gain.setValueAtTime(0.0001, at);
  g.gain.exponentialRampToValueAtTime(v, at + 0.014);
  g.gain.exponentialRampToValueAtTime(v * 0.62, at + 0.10);
  g.gain.exponentialRampToValueAtTime(0.0001, at + Math.max(0.16, dur * 0.96));

  o1.start(at); o1.stop(at + dur + 0.08);
  o2.start(at); o2.stop(at + dur + 0.08);
}

function playSong(){
  if(!initAudio()) return;
  if(actx.state === "suspended") actx.resume();
  stopSong();
  var at = actx.currentTime + 0.12;
  var total = 0;
  for(var i = 0; i < MELODY.length; i++){
    var f = MELODY[i][0], b = MELODY[i][1];
    tone(f, at + total * BEAT, b * BEAT * 0.94, 0.19, "triangle");
    tone(f / 2, at + total * BEAT, b * BEAT * 0.9, 0.055, "sine");
    total += b;
  }
  var endAt = at + total * BEAT;
  playing = { end: endAt };
  return endAt;
}

function stopSong(){
  playing = null;
}

function sfx(name){
  if(!actx || muted) return;
  var now = actx.currentTime;
  if(name === "pop"){
    var o = actx.createOscillator(), g = actx.createGain();
    o.type = "sine";
    o.frequency.setValueAtTime(760, now);
    o.frequency.exponentialRampToValueAtTime(180, now + 0.14);
    g.gain.setValueAtTime(0.18, now);
    g.gain.exponentialRampToValueAtTime(0.0001, now + 0.16);
    o.connect(g); g.connect(master);
    o.start(now); o.stop(now + 0.2);
  }else if(name === "blow" || name === "whoosh"){
    var len = Math.floor(actx.sampleRate * 0.5);
    var buf = actx.createBuffer(1, len, actx.sampleRate);
    var d = buf.getChannelData(0);
    for(var i = 0; i < len; i++) d[i] = (Math.random() * 2 - 1) * (1 - i / len);
    var src = actx.createBufferSource();
    src.buffer = buf;
    var flt = actx.createBiquadFilter();
    flt.type = "lowpass";
    flt.frequency.setValueAtTime(1400, now);
    flt.frequency.exponentialRampToValueAtTime(320, now + 0.45);
    var gg = actx.createGain();
    gg.gain.setValueAtTime(0.0001, now);
    gg.gain.exponentialRampToValueAtTime(name === "blow" ? 0.30 : 0.13, now + 0.05);
    gg.gain.exponentialRampToValueAtTime(0.0001, now + 0.5);
    src.connect(flt); flt.connect(gg); gg.connect(master);
    src.start(now);
  }else if(name === "chime"){
    [1046.5, 1318.5, 1568, 2093].forEach(function(f, i){
      tone(f, now + i * 0.085, 0.9, 0.10, "sine");
    });
  }else if(name === "final"){
    [523.25, 659.25, 783.99, 1046.5].forEach(function(f, i){
      tone(f, now + 0.02 + i * 0.04, 2.4, 0.12, "triangle");
    });
    tone(261.63, now, 2.6, 0.10, "sine");
  }
}

/* ============================================================
   场景切换
   ============================================================ */
function show(id){
  ["scene1", "scene2", "scene3"].forEach(function(s){
    $(s).classList.toggle("on", s === id);
  });
}

/* ============================================================
   蜡烛
   ============================================================ */
var CANDLE_COUNT = 3;
var candles = [];
var litCount = 0;
var blowingDone = false;

function buildCandles(){
  var box = $("candles");
  box.innerHTML = "";
  candles = [];
  for(var i = 0; i < CANDLE_COUNT; i++){
    var d = document.createElement("div");
    d.className = "candle";
    d.innerHTML =
      '<div class="flame"><i></i></div>' +
      '<div class="wick"></div>' +
      '<div class="smoke"></div>' +
      '<div class="stick"></div>';
    d.addEventListener("click", function(e){ e.stopPropagation(); blowOne(this); });
    box.appendChild(d);
    candles.push(d);
  }
  litCount = CANDLE_COUNT;
  blowingDone = false;
}

function blowOne(el){
  if(!el || el.classList.contains("out")) return;
  el.classList.add("out");
  var sm = el.querySelector(".smoke");
  sm.classList.remove("go");
  void sm.offsetWidth;
  sm.classList.add("go");
  litCount--;
  sfx("whoosh");
  if(litCount <= 0 && !blowingDone) finishCandles();
}

function blowAll(){
  candles.forEach(function(c, i){
    setTimeout(function(){ blowOne(c); }, i * 260);
  });
}

function finishCandles(){
  blowingDone = true;
  stopBlowDetect();
  sfx("final");
  setTimeout(function(){
    confettiRain(70);
    var r = Math.random;
    firework(W * 0.22 + r() * 60, H * 0.26);
    setTimeout(function(){ firework(W * 0.72 - r() * 50, H * 0.22); }, 240);
    setTimeout(function(){ firework(W * 0.48, H * 0.34); }, 520);
    setTimeout(function(){ show("scene3"); startTyping(); }, 700);
  }, 380);
}

/* ============================================================
   麦克风吹气
   ============================================================ */
var micStream = null, micCtx = null, micRaf = 0, micLevel = 0;

function stopBlowDetect(){
  if(micRaf){ cancelAnimationFrame(micRaf); micRaf = 0; }
  if(micStream){
    micStream.getTracks().forEach(function(t){ try{ t.stop(); }catch(e){} });
    micStream = null;
  }
  $("micBar").classList.remove("on");
}

function startBlowDetect(){
  var md = navigator.mediaDevices;
  if(!md || !md.getUserMedia){
    toast("这个浏览器不支持麦克风，直接点蜡烛吧");
    return;
  }
  $("micBtn").disabled = true;
  $("micBtn").textContent = "正在打开麦克风…";
  md.getUserMedia({ audio: { echoCancellation: false, noiseSuppression: false, autoGainControl: false } })
    .then(function(stream){
      micStream = stream;
      var AC = window.AudioContext || window.webkitAudioContext;
      micCtx = new AC();
      var src = micCtx.createMediaStreamSource(stream);
      var an = micCtx.createAnalyser();
      an.fftSize = 512;
      src.connect(an);
      var data = new Uint8Array(an.fftSize);
      var hot = 0;

      $("micBtn").textContent = "正在听……吹吧";
      $("micBar").classList.add("on");
      $("blowTip").innerHTML = "对着手机麦克风，<br>轻轻吹一口气";
      bars = document.querySelectorAll(".mic-bar span");

      function tick(){
        an.getByteTimeDomainData(data);
        var sum = 0;
        for(var i = 0; i < data.length; i++){
          var v = (data[i] - 128) / 128;
          sum += v * v;
        }
        var rms = Math.sqrt(sum / data.length);
        micLevel = rms;
        for(var b = 0; b < bars.length; b++){
          var h = 6 + Math.min(26, rms * 190 + Math.random() * 4);
          bars[b].style.height = h + "px";
          bars[b].style.background = rms > 0.07 ? "rgba(255,210,122,.9)" : "rgba(255,255,255,.35)";
        }
        if(rms > 0.075){
          hot++;
          if(hot > 2){
            sfx("blow");
            stopBlowDetect();
            $("micBtn").textContent = "呼——";
            $("blowTip").innerHTML = "呼——";
            setTimeout(blowAll, 200);
            return;
          }
        }else{
          hot = Math.max(0, hot - 1);
        }
        micRaf = requestAnimationFrame(tick);
      }
      tick();
    })
    .catch(function(){
      $("micBtn").disabled = false;
      $("micBtn").textContent = "用嘴吹灭";
      toast("没拿到麦克风权限，直接点蜡烛也一样～");
    });
}

var bars = [];

/* ============================================================
   第三幕：打字机
   ============================================================ */
var typingTimer = null;

function startTyping(){
  var box = $("message");
  box.innerHTML = "";
  $("againBtn").classList.remove("on");
  clearTimeout(typingTimer);

  var lines = CONFIG.lines.slice();
  var li = 0;

  function nextLine(){
    if(li >= lines.length){
      $("fromLine").classList.add("on");
      $("againBtn").classList.add("on");
      return;
    }
    var p = document.createElement("p");
    var caret = document.createElement("span");
    caret.className = "caret";
    p.appendChild(caret);
    box.appendChild(p);

    var chars = Array.from(lines[li]);
    var ci = 0;
    (function tick(){
      if(ci >= chars.length){
        caret.remove();
        li++;
        typingTimer = setTimeout(nextLine, 340);
        return;
      }
      caret.insertAdjacentText("beforebegin", chars[ci]);
      ci++;
      typingTimer = setTimeout(tick, chars[ci - 1] === "，" ? 180 : 62);
    })();
  }
  nextLine();
}

/* ============================================================
   启动
   ============================================================ */
function fillContent(){
  var d = new Date();
  var dateStr = CONFIG.date || (d.getFullYear() + " · " + (d.getMonth() + 1) + " · " + d.getDate());
  $("dateText").textContent = dateStr;
  $("who").innerHTML = "亲爱的 <em>" + esc(CONFIG.to) + "</em>";
  document.title = "生日快乐 · " + CONFIG.to;
  if(CONFIG.from){
    $("fromLine").innerHTML = "—— 来自 <b>" + esc(CONFIG.from) + "</b>";
  }else{
    $("fromLine").innerHTML = "";
  }
}
function esc(s){
  return String(s).replace(/[&<>"']/g, function(c){
    return ({ "&":"&amp;", "<":"&lt;", ">":"&gt;", '"':"&quot;", "'":"&#39;" })[c];
  });
}

var toastTimer = null;
function toast(msg){
  var t = $("toast");
  t.textContent = msg;
  t.classList.add("on");
  clearTimeout(toastTimer);
  toastTimer = setTimeout(function(){ t.classList.remove("on"); }, 2600);
}

function start(){
  show("scene2");
  $("snd").classList.add("on");
  playSong();
  sfx("chime");
  confettiRain(26);
  setTimeout(function(){ burstConfetti(W / 2, H * 0.42, 22, 1.1); }, 60);
}

$("startBtn").addEventListener("click", start);

$("micBtn").addEventListener("click", function(){
  if(blowingDone) return;
  startBlowDetect();
});

$("againBtn").addEventListener("click", function(){
  playSong();
  confettiRain(40);
  firework(W * 0.3 + Math.random() * W * 0.4, H * 0.3);
});

$("snd").addEventListener("click", function(){
  muted = !muted;
  this.classList.toggle("muted", muted);
  if(actx){
    if(muted) master.gain.value = 0;
    else master.gain.value = 0.9;
  }
});

/* 屏幕被点一下也放个彩带（只在第三幕） */
$("scene3").addEventListener("click", function(e){
  if(e.target.closest("button")) return;
  burstConfetti(e.clientX, e.clientY, 8, 0.8);
});

document.addEventListener("visibilitychange", function(){
  if(document.hidden && micStream) stopBlowDetect();
});

/* ============================================================
   初始化
   ============================================================ */
window.addEventListener("resize", resize);
window.addEventListener("orientationchange", function(){
  setTimeout(resize, 260);
});

resize();
fillContent();
buildCandles();
requestAnimationFrame(loop);

/* 截图/预览用：?scene=3 直接看终幕 */
try{
  var qs = new URLSearchParams(location.search);
  var sc = qs.get("scene");
  if(sc === "3"){
    show("scene3");
    $("snd").classList.add("on");
    CONFIG.lines.forEach(function(l){
      var p = document.createElement("p");
      p.textContent = l;
      $("message").appendChild(p);
    });
    $("fromLine").classList.add("on");
    $("againBtn").classList.add("on");
    confettiRain(50);
    firework(W * 0.3, H * 0.28);
    firework(W * 0.7, H * 0.22);
  }else if(sc === "2"){
    show("scene2");
  }
}catch(e){}

})();
</script>
</body>
</html>
