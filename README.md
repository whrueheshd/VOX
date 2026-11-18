<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>vøx</title>
<link href="https://fonts.googleapis.com/css2?family=Tajawal:wght@400;500;700;800&family=Cinzel:wght@600;800&display=swap" rel="stylesheet">
<style>
:root{--b:#1d4ed8;--b2:#3b82f6;--bd:#0b1e5b;--bg:#f4f8ff;--w:#fff;--line:#dbe7ff;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px)}
*{box-sizing:border-box;margin:0}
html{scroll-padding-top:env(safe-area-inset-top,0px)}
body{font-family:'Tajawal',system-ui,sans-serif;background:radial-gradient(circle at 80% -10%,#dbe8ff,transparent 50%),var(--bg);color:var(--bd);min-height:100vh}
header{display:flex;align-items:center;justify-content:space-between;padding:14px 18px;background:rgba(255,255,255,.85);backdrop-filter:blur(10px);border-bottom:1px solid var(--line);position:sticky;top:env(safe-area-inset-top,0px);z-index:20}
.logo{font-size:28px;font-weight:800;letter-spacing:2px;background:linear-gradient(135deg,var(--bd),var(--b2));-webkit-background-clip:text;background-clip:text;color:transparent;direction:ltr}
.ib{width:42px;height:42px;border-radius:12px;border:1px solid var(--line);background:var(--w);cursor:pointer;display:grid;place-items:center;box-shadow:0 4px 14px rgba(29,78,216,.1)}
.ib span{display:block;width:18px;height:2px;background:var(--b);border-radius:2px;margin:2.5px 0}
.dots{display:flex;flex-direction:column;gap:3px}.dots i{width:5px;height:5px;border-radius:50%;background:var(--b)}
.menu{position:fixed;top:0;right:0;height:100%;width:min(280px,80vw);background:linear-gradient(180deg,var(--bd),var(--b));color:#fff;transform:translateX(100%);transition:.35s;z-index:40;padding:70px 18px 18px;box-shadow:-10px 0 40px rgba(0,0,0,.25)}
.menu.open{transform:none}
.menu h3{opacity:.7;font-size:13px;margin-bottom:14px}
.menu button{display:block;width:100%;text-align:right;padding:14px 16px;margin-bottom:10px;border:1px solid rgba(255,255,255,.25);background:rgba(255,255,255,.08);color:#fff;font:inherit;font-size:17px;font-weight:700;border-radius:14px;cursor:pointer}
.menu button.on{background:#fff;color:var(--b)}
.shade{position:fixed;inset:0;background:rgba(11,30,91,.45);opacity:0;pointer-events:none;transition:.3s;z-index:30}
.shade.show{opacity:1;pointer-events:auto}
main{max-width:720px;margin:0 auto;padding:22px 16px 60px}
.title{font-size:24px;font-weight:800;margin-bottom:16px}
.card{background:var(--w);border:1px solid var(--line);border-radius:20px;padding:18px;margin-bottom:14px;box-shadow:0 10px 30px rgba(29,78,216,.08)}
.name{font-size:20px;font-weight:800;direction:ltr;text-align:right}
.circles{display:flex;gap:12px;margin-top:14px}
.c{width:30px;height:30px;border-radius:50%;border:3px solid #fff;box-shadow:0 0 0 1px var(--line),0 4px 12px rgba(0,0,0,.15)}
.c.g{background:#16a34a}.c.r{background:#dc2626}
.admin .c{cursor:pointer}
.empty{text-align:center;color:#6b84c7;padding:40px 0}
.sc img{width:100%;max-height:200px;object-fit:cover;border-radius:14px;margin-bottom:12px}
pre{background:#0b1e5b;color:#dbe8ff;padding:14px;border-radius:12px;overflow-x:auto;direction:ltr;text-align:left;font-size:13px;margin:12px 0;white-space:pre-wrap;word-break:break-all}
.btn{border:0;background:linear-gradient(135deg,var(--b),var(--b2));color:#fff;font:inherit;font-weight:700;padding:11px 20px;border-radius:12px;cursor:pointer}
.btn.d{background:#dc2626}.btn.o{background:#fff;color:var(--b);border:1px solid var(--line)}
.row{display:flex;gap:8px;flex-wrap:wrap}
input,textarea{width:100%;font:inherit;padding:12px;border:1px solid var(--line);border-radius:12px;margin-bottom:10px;background:#fff;color:var(--bd)}
textarea{min-height:130px;direction:ltr;font-family:monospace}
.adm{display:none;margin-bottom:16px}.admin .adm{display:block}
.badge{display:none;font-size:12px;background:#dcfce7;color:#166534;padding:3px 10px;border-radius:20px;margin-right:8px}.admin .badge{display:inline-block}
.modal{position:fixed;inset:0;display:none;place-items:center;background:rgba(11,30,91,.55);z-index:60;padding:20px}
.modal.show{display:grid}
.box{background:#fff;border-radius:22px;padding:24px;width:min(380px,100%)}
.box h2{margin-bottom:14px}
#welcome{position:fixed;inset:0;z-index:80;display:grid;place-items:center;text-align:center;padding:30px;background:linear-gradient(160deg,var(--bd),var(--b) 60%,var(--b2));color:#fff;transition:opacity .6s,visibility .6s}
#welcome.hide{opacity:0;visibility:hidden}
#welcome .v{font-size:64px;font-weight:800;letter-spacing:6px;direction:ltr}
#welcome p{font-size:21px;line-height:1.9;margin:18px auto 28px;max-width:420px}
#welcome button{background:#fff;color:var(--b);border:0;font:inherit;font-size:18px;font-weight:800;padding:13px 40px;border-radius:30px;cursor:pointer;box-shadow:0 10px 30px rgba(0,0,0,.25)}
.err{color:#dc2626;font-size:14px;min-height:20px}
.note{font-size:13px;color:#6b84c7;margin-top:10px}
/* luxury layer */
body{background:radial-gradient(900px 500px at 90% -10%,#cfe0ff,transparent 60%),radial-gradient(700px 500px at -10% 30%,#e3eeff,transparent 60%),linear-gradient(180deg,#f7faff,#eaf1ff);background-attachment:fixed}
header{background:rgba(255,255,255,.72);backdrop-filter:blur(18px) saturate(160%);border-bottom:1px solid rgba(59,130,246,.18);box-shadow:0 8px 30px rgba(11,30,91,.07)}
.logo{font-family:'Cinzel',serif;font-size:30px;letter-spacing:5px;background:linear-gradient(110deg,#0b1e5b 20%,#3b82f6 45%,#9cc2ff 50%,#3b82f6 55%,#0b1e5b 80%);background-size:250% 100%;-webkit-background-clip:text;background-clip:text;color:transparent;animation:shine 5s linear infinite}
@keyframes shine{to{background-position:-250% 0}}
.ib{background:linear-gradient(145deg,#fff,#eaf1ff);border:1px solid rgba(59,130,246,.25);transition:.25s}
.ib:hover{transform:translateY(-2px);box-shadow:0 10px 24px rgba(29,78,216,.22)}
.menu{background:linear-gradient(170deg,#06133d,#0b1e5b 45%,#1d4ed8);border-left:1px solid rgba(255,255,255,.15)}
.menu button{background:linear-gradient(135deg,rgba(255,255,255,.12),rgba(255,255,255,.04));backdrop-filter:blur(6px);transition:.25s}
.menu button:hover{transform:translateX(-4px);background:rgba(255,255,255,.2)}
.menu button.on{background:linear-gradient(135deg,#fff,#dbe8ff);box-shadow:0 8px 24px rgba(0,0,0,.25)}
.title{font-size:28px;display:flex;align-items:center;gap:12px;color:#0b1e5b}
.title:after{content:'';flex:1;height:2px;border-radius:2px;background:linear-gradient(90deg,transparent,#3b82f6)}
.card{position:relative;background:linear-gradient(160deg,rgba(255,255,255,.95),rgba(236,243,255,.85));border:1px solid rgba(59,130,246,.2);border-radius:24px;padding:22px;box-shadow:0 18px 45px rgba(29,78,216,.12),inset 0 1px 0 #fff;animation:rise .6s both;transition:.3s;overflow:hidden}
.card:before{content:'';position:absolute;top:0;right:0;left:0;height:3px;background:linear-gradient(90deg,#0b1e5b,#3b82f6,#9cc2ff)}
.card:hover{transform:translateY(-4px);box-shadow:0 26px 60px rgba(29,78,216,.2)}
@keyframes rise{from{opacity:0;transform:translateY(18px)}to{opacity:1;transform:none}}
.name{font-size:22px;letter-spacing:1px}
.circles{gap:16px}
.c{width:34px;height:34px;border:3px solid #fff;transition:.25s}
.c.g{background:radial-gradient(circle at 30% 30%,#6ee7a0,#16a34a);box-shadow:0 0 0 1px #bbf7d0,0 0 18px rgba(22,163,74,.55)}
.c.r{background:radial-gradient(circle at 30% 30%,#fca5a5,#dc2626);box-shadow:0 0 0 1px #fecaca,0 0 18px rgba(220,38,38,.5)}
.admin .c:hover{transform:scale(1.18)}
.btn{background:linear-gradient(135deg,#0b1e5b,#1d4ed8 55%,#3b82f6);box-shadow:0 8px 20px rgba(29,78,216,.35),inset 0 1px 0 rgba(255,255,255,.35);transition:.25s}
.btn:hover{transform:translateY(-2px);box-shadow:0 14px 28px rgba(29,78,216,.45)}
.btn.d{background:linear-gradient(135deg,#991b1b,#dc2626)}
.btn.o{background:#fff}
input,textarea{border:1px solid rgba(59,130,246,.25);background:rgba(255,255,255,.9);transition:.2s}
input:focus,textarea:focus{outline:0;border-color:#3b82f6;box-shadow:0 0 0 4px rgba(59,130,246,.18)}
pre{background:linear-gradient(160deg,#06133d,#0b1e5b);border:1px solid rgba(156,194,255,.25);box-shadow:inset 0 0 30px rgba(59,130,246,.15)}
.box{background:linear-gradient(160deg,#fff,#eef4ff);border:1px solid rgba(59,130,246,.25);box-shadow:0 30px 80px rgba(6,19,61,.45);animation:rise .4s both}
.modal{backdrop-filter:blur(8px)}
#welcome{background:radial-gradient(600px 400px at 20% 20%,rgba(96,165,250,.55),transparent 60%),radial-gradient(700px 500px at 85% 85%,rgba(59,130,246,.5),transparent 60%),linear-gradient(160deg,#050f33,#0b1e5b 55%,#1d4ed8);overflow:hidden}
#welcome:before,#welcome:after{content:'';position:absolute;border-radius:50%;border:1px solid rgba(255,255,255,.14);animation:pulse 6s ease-in-out infinite}
#welcome:before{width:420px;height:420px}
#welcome:after{width:700px;height:700px;animation-delay:1.5s}
@keyframes pulse{0%,100%{transform:scale(.92);opacity:.5}50%{transform:scale(1.08);opacity:1}}
#welcome>div{position:relative;z-index:2;animation:rise 1.1s both}
#welcome .v{font-family:'Cinzel',serif;font-size:76px;letter-spacing:12px;text-shadow:0 0 40px rgba(156,194,255,.8);padding-right:0}
#welcome p{font-weight:500;color:#e6efff}
#welcome p:before{content:'';display:block;width:90px;height:2px;margin:0 auto 20px;background:linear-gradient(90deg,transparent,#9cc2ff,transparent)}
#welcome button{background:linear-gradient(135deg,#fff,#cfe0ff);transition:.3s}
#welcome button:hover{transform:translateY(-3px) scale(1.04);box-shadow:0 16px 40px rgba(156,194,255,.55)}
.empty{border:1px dashed rgba(59,130,246,.35);border-radius:22px;background:rgba(255,255,255,.5)}
</style>
</head>
<body>
<div id="welcome"><div><div class="v">vøx</div><p>حياك الله في موقعنا الذي يتميز بجميع السكربتات والهاكات</p><button id="enter">دخول</button></div></div>

<header>
  <button class="ib" id="burger" aria-label="القائمة"><div><span></span><span></span><span></span></div></button>
  <div class="logo">vøx<span class="badge">مشرف</span></div>
  <button class="ib" id="dotsBtn" aria-label="الإدارة"><div class="dots"><i></i><i></i><i></i></div></button>
</header>
<div class="shade" id="shade"></div>
<nav class="menu" id="menu">
  <h3>القائمة</h3>
  <button data-t="status" class="on">حالات الهاكات</button>
  <button data-t="scripts">سكربتات</button>
</nav>

<main id="app"></main>

<div class="modal" id="pw"><div class="box"><h2>ضع كلمة المرور</h2>
  <input type="password" id="pwi" dir="ltr" placeholder="••••••">
  <div class="err" id="pwe"></div>
  <div class="row"><button class="btn" id="pwok">دخول</button><button class="btn o" id="pwno">إلغاء</button></div></div></div>

<script>
const PASS='@@&/:';
let tab='status',admin=false;
const $=s=>document.querySelector(s);
const esc=s=>String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
function load(k,d){try{const v=localStorage.getItem(k);return v?JSON.parse(v):d}catch(e){return d}}
function save(k,v){try{localStorage.setItem(k,JSON.stringify(v))}catch(e){}}
let statuses=load('vox_status',[{name:'del/ta',c:['g','g','g']}]);
let scripts=load('vox_scripts',[]);
let draftImg='';

function render(){
  document.body.classList.toggle('admin',admin);
  let h='';
  if(tab==='status'){
    h+='<div class="title">حالات الهاكات</div>';
    h+=`<div class="card adm"><input id="sn" dir="ltr" placeholder="اسم الهاك"><button class="btn" onclick="addStatus()">إضافة</button><div class="note">اضغط على الدوائر لتغيير اللون بين الأخضر والأحمر.</div></div>`;
    h+=statuses.map((s,i)=>`<div class="card"><div class="name">${esc(s.name)}</div><div class="circles">${s.c.map((c,j)=>`<div class="c ${c}" onclick="tog(${i},${j})"></div>`).join('')}</div>${admin?`<div class="row" style="margin-top:14px"><button class="btn d" onclick="delStatus(${i})">حذف</button></div>`:''}</div>`).join('')||'<div class="empty">لا توجد حالات</div>';
  }else{
    h+='<div class="title">سكربتات</div>';
    h+=`<div class="card adm"><input id="xn" placeholder="اسم السكربت"><input type="file" id="xi" accept="image/*"><textarea id="xs" placeholder="ضع السكربت هنا"></textarea><button class="btn" onclick="addScript()">نشر السكربت</button></div>`;
    h+=scripts.map((s,i)=>`<div class="card sc">${s.img?`<img src="${s.img}" alt="">`:''}<div class="name" style="text-align:right">${esc(s.name)}</div><pre>${esc(s.code)}</pre><div class="row"><button class="btn" onclick="cp(${i},this)">نسخ</button>${admin?`<button class="btn d" onclick="delScript(${i})">حذف</button>`:''}</div></div>`).join('')||'<div class="empty">لا توجد سكربتات بعد</div>';
  }
  $('#app').innerHTML=h;
  const xi=$('#xi');if(xi)xi.onchange=pick;
}
function tog(i,j){if(!admin)return;const c=statuses[i].c;c[j]=c[j]==='g'?'r':'g';save('vox_status',statuses);render()}
function addStatus(){const n=$('#sn').value.trim();if(!n)return;statuses.push({name:n,c:['r','r','r']});save('vox_status',statuses);render()}
function delStatus(i){statuses.splice(i,1);save('vox_status',statuses);render()}
function pick(e){
  const f=e.target.files[0];if(!f)return;
  const r=new FileReader();r.onload=()=>{const im=new Image();im.onload=()=>{const m=600,k=Math.min(1,m/im.width),cv=document.createElement('canvas');cv.width=im.width*k;cv.height=im.height*k;cv.getContext('2d').drawImage(im,0,0,cv.width,cv.height);draftImg=cv.toDataURL('image/jpeg',.8)};im.src=r.result};r.readAsDataURL(f);
}
function addScript(){
  const n=$('#xn').value.trim(),c=$('#xs').value;if(!n||!c.trim())return;
  scripts.unshift({name:n,img:draftImg,code:c});draftImg='';save('vox_scripts',scripts);render();
}
function delScript(i){scripts.splice(i,1);save('vox_scripts',scripts);render()}
function cp(i,b){
  const t=scripts[i].code;
  const done=()=>{b.textContent='تم النسخ ✓';setTimeout(()=>b.textContent='نسخ',1500)};
  if(navigator.clipboard&&navigator.clipboard.writeText){navigator.clipboard.writeText(t).then(done,fb)}else fb();
  function fb(){const a=document.createElement('textarea');a.value=t;document.body.appendChild(a);a.select();try{document.execCommand('copy')}catch(e){}a.remove();done()}
}
function menu(o){$('#menu').classList.toggle('open',o);$('#shade').classList.toggle('show',o)}
$('#burger').onclick=()=>menu(true);$('#shade').onclick=()=>menu(false);
document.querySelectorAll('.menu button').forEach(b=>b.onclick=()=>{tab=b.dataset.t;document.querySelectorAll('.menu button').forEach(x=>x.classList.toggle('on',x===b));menu(false);render()});
$('#dotsBtn').onclick=()=>{if(admin){admin=false;render();return}$('#pwi').value='';$('#pwe').textContent='';$('#pw').classList.add('show');setTimeout(()=>$('#pwi').focus(),50)};
$('#pwno').onclick=()=>$('#pw').classList.remove('show');
$('#pwok').onclick=()=>{if($('#pwi').value===PASS){admin=true;$('#pw').classList.remove('show');render()}else $('#pwe').textContent='كلمة المرور خاطئة'};
$('#pwi').onkeydown=e=>{if(e.key==='Enter')$('#pwok').click()};
$('#enter').onclick=()=>$('#welcome').classList.add('hide');
render();
</script>
</body>
</html>
