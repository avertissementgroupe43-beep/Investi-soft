<!DOCTYPE html>
<html lang="fr"><head><meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1, viewport-fit=cover">
<title>InvestiSoft</title>
<style>
:root{--bg:#f3f6fb;--card:#fff;--tx:#14213d;--mut:#5b6b85;--bd:#dce4f0;--blue:#0a33b0;--green:#12a80f;--red:#d62828;--rl:#ffe4e4;--rt:#a61b1b;--gl:#e3f6e2;box-sizing:border-box;padding-top:env(safe-area-inset-top,0px);padding-bottom:env(safe-area-inset-bottom,0px);color-scheme:light}
@media(prefers-color-scheme:dark){:root:not([data-theme="light"]){--bg:#0d1325;--card:#162039;--tx:#eef2fb;--mut:#9fb0cc;--bd:#27345a;--rl:#4a1d24;--rt:#ffb3b3;--gl:#17381c;color-scheme:dark}}
:root[data-theme="dark"]{--bg:#0d1325;--card:#162039;--tx:#eef2fb;--mut:#9fb0cc;--bd:#27345a;--rl:#4a1d24;--rt:#ffb3b3;--gl:#17381c;color-scheme:dark}
*{box-sizing:border-box}
html,body{margin:0}
body{background:var(--bg);color:var(--tx);font:16px/1.5 "Trebuchet MS","Segoe UI",system-ui,sans-serif;background-color:var(--bg)}
main{max-width:760px;margin:0 auto;padding:16px}
h1,h2,h3{margin:0 0 8px;line-height:1.2}
h2{font-size:1.35rem}h3{font-size:1.1rem}
.mut{color:var(--mut)}
.top{background:#fff;border-radius:16px;padding:14px 18px;text-align:center;border:1px solid var(--bd)}
.top img{max-width:min(320px,80%);height:auto;display:block;margin:0 auto}
.card{background:var(--card);border:1px solid var(--bd);border-radius:14px;padding:16px;margin-top:14px}
.hide{display:none!important}
.co{display:flex;align-items:center;gap:14px;width:100%;text-align:left;background:var(--card);color:var(--tx);border:1px solid var(--bd);border-radius:14px;padding:12px 14px;margin-top:10px;cursor:pointer;font:inherit}
.co:hover,.co:focus-visible{border-color:var(--blue);outline:2px solid var(--blue);outline-offset:1px}
.co img,.cb img{width:56px;height:56px;border-radius:50%;object-fit:cover;flex:none;background:#fff}
.co b{display:block}
label{display:block;font-weight:700;margin:12px 0 4px;font-size:.95rem}
input,select{width:100%;padding:11px 12px;border-radius:10px;border:1px solid var(--bd);background:var(--bg);color:var(--tx);font:inherit}
input:focus,select:focus{outline:2px solid var(--blue);outline-offset:1px}
.row{display:flex;gap:10px}.row>*{flex:1;min-width:0}
.btn{display:inline-block;border:0;border-radius:10px;padding:12px 18px;font:inherit;font-weight:700;cursor:pointer;color:#fff;background:var(--blue);text-decoration:none;text-align:center}
.btn.g{background:#0e8a0c}.btn.r{background:var(--red)}.btn.o{background:transparent;color:var(--tx);border:1px solid var(--bd)}
.btn.w{width:100%;margin-top:14px}
.btn:focus-visible{outline:3px solid var(--tx);outline-offset:2px}
.err{color:var(--rt);font-weight:700;min-height:1.4em;margin:8px 0 0}
.phone{display:flex;gap:8px;align-items:center}.phone span{font-weight:700;white-space:nowrap}
.cb{display:flex;align-items:center;gap:12px;padding:14px 16px;border-radius:14px;color:#fff;background:linear-gradient(90deg,var(--red) 0%,var(--red) 45%,#0e8a0c 55%,#0e8a0c 100%)}
.cb b{font-size:1.15rem;display:block}.cb small{opacity:.95}
.cb .btn{margin-left:auto;padding:8px 12px;background:rgba(0,0,0,.28)}
.al{border-radius:12px;padding:14px;margin-top:14px;font-weight:700}
.al.late{background:var(--red);color:#fff;font-size:1.1rem}
.al.ok{background:var(--gl);color:var(--tx)}
.int{background:var(--rl);color:var(--rt);border-radius:10px;padding:10px 12px;margin-top:10px;font-weight:700}
.it{border:1px solid var(--bd);border-radius:12px;padding:12px;margin-top:10px}
.it.l{border-color:var(--red)}
.it .h{display:flex;justify-content:space-between;gap:8px;font-weight:700}
.tag{font-weight:700;border-radius:8px;padding:2px 8px;font-size:.85rem}
.tag.l{background:var(--rl);color:var(--rt)}.tag.o{background:var(--gl)}.tag.p{background:var(--bd)}
.acts{display:flex;gap:8px;margin-top:10px}.acts .btn{padding:7px 12px;font-size:.9rem}
.chips{display:flex;flex-wrap:wrap;gap:10px;margin-top:6px}
.chip{display:flex;align-items:center;gap:8px;padding:8px 12px;border-radius:999px;border:2px solid var(--bd);background:var(--card);color:var(--tx);font:inherit;cursor:pointer}
.chip i{width:20px;height:20px;border-radius:50%;border:1px solid rgba(128,128,128,.6)}
.chip[aria-pressed=true]{border-color:var(--blue);background:var(--gl)}
.chip:disabled{opacity:.5;cursor:not-allowed;text-decoration:line-through}
.pl{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:6px}
.pl button{padding:16px 10px;border-radius:12px;border:2px solid var(--bd);background:var(--card);color:var(--tx);font:inherit;cursor:pointer}
.pl button b{display:block;font-size:1.3rem}
.pl button[aria-pressed=true]{border-color:var(--blue);background:var(--gl)}
.msg{white-space:pre-wrap;background:var(--bg);border:1px dashed var(--bd);border-radius:10px;padding:12px;margin-top:12px}
dialog{border:0;border-radius:16px;padding:0;max-width:min(92vw,460px);width:100%;background:var(--card);color:var(--tx)}
dialog::backdrop{background:rgba(0,0,0,.55)}
.dl{padding:20px}
.pg{background:#fff;color:#111;border-radius:10px;padding:18px;margin:10px 0;border:1px solid var(--bd)}
.pg img{width:180px;max-width:70%;display:block;margin:0 auto 10px}
.pg h3{color:var(--red);text-align:center}
.gc{display:grid;grid-template-columns:1fr 1fr;gap:10px;margin-top:10px}
.gcard{border-radius:14px;padding:16px 12px;min-height:110px;display:flex;flex-direction:column;justify-content:space-between;box-shadow:0 2px 6px rgba(0,0,0,.25);text-shadow:0 1px 2px rgba(0,0,0,.4)}
.gcard b{font-size:.95rem;line-height:1.2}.gcard small,.gcard span{font-size:.8rem}
.gcard.off{background:var(--bd);color:var(--mut);box-shadow:none;text-shadow:none}.gcard.off b{text-decoration:line-through}
footer{text-align:center;color:var(--mut);font-size:.85rem;padding:22px 0 8px}
@media(max-width:480px){.row{flex-direction:column}.cb{flex-wrap:wrap}}
@media(prefers-reduced-motion:no-preference){.al.late{animation:p 1.6s ease-in-out 3}@keyframes p{50%{filter:brightness(1.25)}}}
</style></head><body><main>
<div class="top"><img id="logo" src="LOGO_INVESTISOFT" alt="InvestiSoft"></div>

<section id="v-home">
 <div class="card"><h2>Espace 1 · Choisissez votre entreprise</h2>
 <p class="mut">Touchez le nom de votre entreprise, puis entrez votre code d’accès.</p>
 <p class="mut" id="hrs"></p>
 <div id="cos"></div></div>
</section>

<section id="v-prof" class="hide">
 <div class="card"><h2>Votre profil</h2>
 <p class="mut">Complétez ces informations avant d’entrer dans votre tableau de bord.</p>
 <label for="pe">Adresse e-mail</label><input id="pe" type="email" autocomplete="email">
 <label for="pn">Nom de l’entreprise</label><input id="pn" type="text">
 <label for="ct">Continent</label><select id="ct"></select>
 <label for="pq">Chercher un pays</label><input id="pq" type="search" placeholder="Écrivez le nom de votre pays">
 <label for="cn">Pays</label><select id="cn"></select>
 <label for="pt">Numéro de téléphone</label>
 <div class="phone"><span id="dial">+</span><input id="pt" type="tel" inputmode="tel" autocomplete="tel-national"></div>
 <p class="err" id="perr" role="alert"></p>
 <button class="btn w" id="psave">Enregistrer et continuer</button>
 <button class="btn o w" id="pback">Retour</button></div>
</section>

<section id="v-dash" class="hide">
 <div class="cb" style="margin-top:14px"><img id="dlogo" alt="" style="width:48px;height:48px;border-radius:50%;object-fit:cover;background:#fff"><div><small>Tableau de bord</small><b id="dname"></b></div><button class="btn" id="out">Quitter</button></div>
 <div id="alert"></div>
 <div class="card"><h3>Ajouter un achat à crédit</h3>
  <label for="ia">Ce que vous avez pris à crédit</label><input id="ia" type="text" placeholder="Ex. : 10 sacs de ciment">
  <label for="ip">Prix dû (FCFA)</label><input id="ip" type="number" inputmode="numeric" min="0">
  <div class="row"><div><label for="id1">Date de début</label><input id="id1" type="date"></div>
  <div><label for="id2">Date de paiement</label><input id="id2" type="date"></div></div>
  <p class="err" id="ierr" role="alert"></p>
  <button class="btn w" id="iadd">Ajouter</button></div>
 <div class="card"><h3>Mes achats à crédit</h3><div id="list"></div></div>
 <div class="card hide" id="nbox"><h3>Avis de retard</h3><p class="mut">Un document est prêt pour vous.</p><button class="btn r w" id="nopen">Voir et télécharger l’avis</button></div>
 <div class="card"><h3>Vous avez besoin d’aide ???</h3><p class="mut">Cliquez sur ce bouton et vous pouvez demander ce que vous voulez, ce que vous ne comprenez pas.</p>
 <a class="btn g w" href="https://chat.whatsapp.com/GTYqE5WTG3J73UcwfvlMGs?s=cl&amp;p=a&amp;iam=2" target="_blank" rel="noopener">Demander de l’aide</a></div>
 <div class="card"><h3>Cartes de réduction</h3><p class="mut">Choisissez votre couleur et votre durée d’abonnement.</p><button class="btn w" id="tosub">Voir l’abonnement (Espace 2)</button></div>
</section>

<section id="v-sub" class="hide">
 <div class="card"><h2>Espace 2 · Abonnement</h2>
 <p class="mut">Un abonnement vous permet de créer vos cartes de réduction.</p>
 <label>Durée</label>
 <div class="pl"><button data-p="4000" data-d="1 semaine" aria-pressed="false"><b>4 000 FCFA</b>1 semaine</button><button data-p="10000" data-d="1 mois" aria-pressed="false"><b>10 000 FCFA</b>1 mois</button></div>
 <p class="err" id="serr" role="alert"></p>
 <a class="btn g w" id="pay" href="https://chat.whatsapp.com/Eft7n2kSLBAEOCTNPJcpZT?s=cl&amp;p=a&amp;iam=2" target="_blank" rel="noopener">Payer l’abonnement</a>
 <div class="msg hide" id="pmsg"></div>
 <p class="mut hide" id="phint">Collez ce message dans la discussion WhatsApp qui vient de s’ouvrir.</p>
 <button class="btn o w hide" id="pcopy">Copier le message</button>
 <button class="btn o w" id="sback">Retour au tableau de bord</button></div>
 <div class="card"><h3>Activer mon abonnement</h3>
  <div id="actin"><label for="ac">Code d’activation</label><input id="ac" type="text" autocomplete="off" autocapitalize="characters">
  <div id="adbox" class="hide"><label for="ae">Date d’expiration</label><input id="ae" type="date"></div>
  <p class="err" id="aerr" role="alert"></p><button class="btn w" id="aok">Valider le code</button></div>
  <div id="actok" class="hide"><div class="al ok" id="astat"></div><button class="btn w" id="to3">Ouvrir l’Espace 3 · Mes cartes</button></div></div>
</section>

<section id="v-cards" class="hide"><div class="card"><h2>Espace 3 · Cartes de réduction</h2><p class="mut" id="c3info"></p><div class="gc" id="gc"></div><button class="btn o w" id="c3back">Retour à l’abonnement</button></div></section>
<section id="v-closed" class="hide"><div class="card" style="text-align:center"><h2>Le site est fermé pour le moment</h2><p id="ctx"></p></div></section>
<section id="v-owner" class="hide"><div class="card"><h2 id="oh">Espace propriétaire</h2><p class="mut">Tout ce qui a été mis dans le site, au même endroit. Le site reste ouvert pour vous à toute heure.</p>
<h3 style="margin-top:14px">Mon compte</h3>
<label for="on">Mon nom</label><input id="on" type="text" autocomplete="name">
<label for="oe">Mon adresse e-mail</label><input id="oe" type="email" autocomplete="email">
<p class="err" id="oacc" role="alert"></p><button class="btn w" id="osave">Enregistrer mon compte</button>
<h3 style="margin-top:18px">Ce que mes clients doivent</h3><p class="mut" id="dbn"></p><div id="odue"></div>
<h3 style="margin-top:18px">Entreprises et codes</h3><div id="ocos"></div>
<h3 style="margin-top:14px">Abonnement et horaires</h3><p>Code d’activation : <b id="oact"></b></p><p>Ouvert de : <b id="ohrs"></b></p>
<button class="btn w" id="o2">Voir l’Espace 2 (abonnement)</button><button class="btn w" id="o3">Voir l’Espace 3 (cartes de réduction)</button>
<button class="btn o w" id="oout">Quitter l’espace propriétaire</button></div></section>
<footer>© 2026 InvestiSoft<br><button class="btn o" id="own" style="padding:6px 12px;font-size:.85rem;margin-top:8px">Compte propriétaire</button></footer>
<dialog id="downer"><div class="dl"><h3>Accès propriétaire</h3><label for="oc">Code propriétaire</label><input id="oc" type="text" autocomplete="off" autocapitalize="characters"><p class="err" id="oerr" role="alert"></p><div class="row" style="margin-top:12px"><button class="btn o" id="ono">Annuler</button><button class="btn" id="ook">Entrer</button></div></div></dialog>
</main>

<dialog id="dcode"><div class="dl"><h3 id="dct"></h3><label for="code">Code d’accès</label><input id="code" type="text" autocomplete="off" autocapitalize="characters"><p class="err" id="cerr" role="alert"></p>
<div class="row" style="margin-top:12px"><button class="btn o" id="cno">Annuler</button><button class="btn" id="cok">Entrer</button></div></div></dialog>

<dialog id="dn"><div class="dl"><div class="pg"><img id="nlogo" alt="InvestiSoft"><h3>Avis de retard</h3><p id="ntx"></p><p style="text-align:right;font-weight:700;margin:0">InvestiSoft</p></div>
<div class="row"><button class="btn o" id="nclose">Fermer</button><button class="btn r" id="npdf">Télécharger le PDF</button></div><p class="err" id="nerr" role="alert"></p></div></dialog>

<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.5.1/jspdf.umd.min.js"></script>
<script>
const CO=[{n:"CABINET GBELIDJI CONSULTING",c:"CJU-2026",l:"LOGO_CJU"},{n:"IZZY MANAGEMENT",c:"IZ-2026",l:"LOGO_IZZY"},{n:"BookIn store",c:"BT-2026",l:"LOGO_BOOKIN"}];
const W={"Afrique":"Afrique du Sud:27,Algérie:213,Angola:244,Bénin:229,Botswana:267,Burkina Faso:226,Burundi:257,Cameroun:237,Cap-Vert:238,Centrafrique:236,Comores:269,Congo:242,RD Congo:243,Côte d’Ivoire:225,Djibouti:253,Égypte:20,Érythrée:291,Eswatini:268,Éthiopie:251,Gabon:241,Gambie:220,Ghana:233,Guinée:224,Guinée-Bissau:245,Guinée équatoriale:240,Kenya:254,Lesotho:266,Libéria:231,Libye:218,Madagascar:261,Malawi:265,Mali:223,Maroc:212,Maurice:230,Mauritanie:222,Mozambique:258,Namibie:264,Niger:227,Nigéria:234,Ouganda:256,Rwanda:250,Sénégal:221,Sierra Leone:232,Somalie:252,Soudan:249,Soudan du Sud:211,Tanzanie:255,Tchad:235,Togo:228,Tunisie:216,Zambie:260,Zimbabwe:263",
"Amérique du Nord":"Belize:501,Canada:1,Costa Rica:506,Cuba:53,États-Unis:1,Guatemala:502,Haïti:509,Honduras:504,Jamaïque:1,Mexique:52,Nicaragua:505,Panama:507,République dominicaine:1,Salvador:503",
"Amérique du Sud":"Argentine:54,Bolivie:591,Brésil:55,Chili:56,Colombie:57,Équateur:593,Guyana:592,Paraguay:595,Pérou:51,Suriname:597,Uruguay:598,Venezuela:58",
"Asie":"Afghanistan:93,Arabie saoudite:966,Bahreïn:973,Bangladesh:880,Cambodge:855,Chine:86,Corée du Sud:82,Émirats arabes unis:971,Inde:91,Indonésie:62,Irak:964,Iran:98,Israël:972,Japon:81,Jordanie:962,Kazakhstan:7,Koweït:965,Laos:856,Liban:961,Malaisie:60,Mongolie:976,Myanmar:95,Népal:977,Oman:968,Ouzbékistan:998,Pakistan:92,Philippines:63,Qatar:974,Singapour:65,Sri Lanka:94,Syrie:963,Thaïlande:66,Turquie:90,Vietnam:84,Yémen:967",
"Europe":"Allemagne:49,Autriche:43,Belgique:32,Bulgarie:359,Croatie:385,Danemark:45,Espagne:34,Finlande:358,France:33,Grèce:30,Hongrie:36,Irlande:353,Italie:39,Luxembourg:352,Norvège:47,Pays-Bas:31,Pologne:48,Portugal:351,République tchèque:420,Roumanie:40,Royaume-Uni:44,Russie:7,Serbie:381,Suède:46,Suisse:41,Ukraine:380",
"Océanie":"Australie:61,Fidji:679,Nouvelle-Zélande:64,Papouasie-Nouvelle-Guinée:675"};
const COLORS=[["Rouge","#d62828"],["Vert","#12a80f"],["Bleu","#1d4ed8"],["Noir","#111111"],["Jaune","#f5c400"],["Rose","#ec4899"],["Violet","#7c3aed"]];
const RATE=5000;
const $=id=>document.getElementById(id);
const esc=s=>String(s).replace(/[&<>"]/g,c=>({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;"}[c]));
const fm=n=>Number(n).toLocaleString("fr-FR")+" FCFA";
const mem={};
const ld=k=>{try{const v=localStorage.getItem(k);if(v)return JSON.parse(v)}catch(e){}return mem[k]||null};
const sv=(k,v)=>{mem[k]=v;try{localStorage.setItem(k,JSON.stringify(v))}catch(e){}};
let cur=null,D=null,pick=null,dur=null,dialC="";
const LOGO=$("logo").src;$("nlogo").src=LOGO;
let last="v-home";
function show(id){if(id!=="v-closed")last=id;["v-home","v-prof","v-dash","v-sub","v-cards","v-closed","v-owner"].forEach(v=>$(v).classList.toggle("hide",v!==id));scrollTo(0,0)}
function days(due){const t=new Date();t.setHours(0,0,0,0);const d=new Date(due+"T00:00:00");return Math.max(0,Math.round((t-d)/864e5))}
function save(){sv("is_"+CO[cur].c,D);syncUp()}

$("cos").innerHTML=CO.map((c,i)=>`<button class="co" data-i="${i}"><img src="${c.l}" alt=""><span><b>${esc(c.n)}</b><span class="mut">Entrer mon code</span></span></button>`).join("");
$("cos").onclick=e=>{const b=e.target.closest(".co");if(!b)return;cur=+b.dataset.i;$("dct").textContent=CO[cur].n;$("code").value="";$("cerr").textContent="";$("dcode").showModal();$("code").focus()};
$("cno").onclick=()=>$("dcode").close();
function login(){if($("code").value.trim().toUpperCase()!==CO[cur].c){$("cerr").textContent="Code incorrect. Vérifiez votre code et réessayez.";return}
 $("dcode").close();D=ld("is_"+CO[cur].c)||{profile:null,items:[]};
 if(D.profile&&D.profile.phone){dash()}else{prof()}}
$("cok").onclick=login;$("code").onkeydown=e=>{if(e.key==="Enter")login()};

function prof(){$("pn").value=CO[cur].n;$("pe").value="";$("pt").value="";$("pq").value="";$("perr").textContent="";fillCt();fillCn();show("v-prof")}
function fillCt(){$("ct").innerHTML=Object.keys(W).map(k=>`<option>${esc(k)}</option>`).join("")}
function fillCn(){const q=$("pq").value.trim().toLowerCase();let rows=[];
 for(const k in W){if(!q&&k!==$("ct").value)continue;W[k].split(",").forEach(s=>{const i=s.lastIndexOf(":");rows.push([s.slice(0,i),s.slice(i+1)])})}
 if(q)rows=rows.filter(r=>r[0].toLowerCase().includes(q));
 $("cn").innerHTML=rows.map(r=>`<option value="${r[1]}">${esc(r[0])} (+${r[1]})</option>`).join("")||"<option value=''>Aucun pays trouvé</option>";
 setDial()}
function setDial(){dialC=$("cn").value;$("dial").textContent=dialC?"+"+dialC:"+"}
$("ct").onchange=()=>{$("pq").value="";fillCn()};$("pq").oninput=fillCn;$("cn").onchange=setDial;
$("pback").onclick=()=>show("v-home");
$("psave").onclick=()=>{const em=$("pe").value.trim(),nm=$("pn").value.trim(),ph=$("pt").value.replace(/\D/g,"");
 if(!/^\S+@\S+\.\S+$/.test(em)){$("perr").textContent="Entrez une adresse e-mail valide.";return}
 if(!nm){$("perr").textContent="Entrez le nom de l’entreprise.";return}
 if(!dialC||ph.length<6){$("perr").textContent="Choisissez votre pays et entrez votre numéro.";return}
 D.profile={email:em,company:nm,phone:"+"+dialC+" "+ph};save();dash()};

function dash(){syncUp();$("dlogo").src=CO[cur].l;$("dname").textContent=D.profile.company||CO[cur].n;
 if(!$("id1").value)$("id1").value=new Date().toISOString().slice(0,10);render();show("v-dash")}
$("out").onclick=()=>{cur=null;D=null;show(OWN?"v-owner":"v-home")};
$("iadd").onclick=()=>{const a=$("ia").value.trim(),p=+$("ip").value,s=$("id1").value,e=$("id2").value;
 if(!a||!(p>0)||!s||!e){$("ierr").textContent="Remplissez l’achat, le prix et les deux dates.";return}
 if(e<s){$("ierr").textContent="La date de paiement doit être après la date de début.";return}
 $("ierr").textContent="";D.items.push({a,p,s,e,paid:false});save();$("ia").value="";$("ip").value="";$("id2").value="";render()};
function render(){let max=0;const co=D.profile.company||CO[cur].n;
 $("list").innerHTML=D.items.length?D.items.map((x,i)=>{const d=x.paid?0:days(x.e),it=d*RATE;if(d>max)max=d;
  const tag=x.paid?'<span class="tag p">Payé</span>':d?`<span class="tag l">En retard de ${d} jour${d>1?"s":""}</span>`:'<span class="tag o">Dans les délais</span>';
  return `<div class="it${d?" l":""}"><div class="h"><span>${esc(x.a)}</span>${tag}</div>
  <div class="mut">Début : ${x.s.split("-").reverse().join("/")} · Paiement : ${x.e.split("-").reverse().join("/")}</div>
  <div>Prix dû : <b>${fm(x.p)}</b></div>${d?`<div class="int">Intérêts : ${d} × ${fm(RATE)} = ${fm(it)}<br>Total à payer : ${fm(x.p+it)}</div>`:""}
  <div class="acts">${x.paid?"":`<button class="btn g" data-pay="${i}">Marquer payé</button>`}<button class="btn o" data-del="${i}">Supprimer</button></div></div>`}).join(""):'<p class="mut">Aucun achat à crédit pour l’instant. Ajoutez le premier ci-dessus.</p>';
 $("alert").innerHTML=max?`<div class="al late" role="alert">${esc(co)} : vous êtes en retard de ${max} jour${max>1?"s":""}.</div><div class="int">Chaque jour de retard, ${fm(RATE)} d’intérêts s’ajoutent.</div>`:'<div class="al ok">Aucun retard. Vous êtes à jour.</div>';
 $("nbox").classList.toggle("hide",!max);D.maxLate=max}
$("list").onclick=e=>{const p=e.target.dataset.pay,d=e.target.dataset.del;
 if(p!==undefined){D.items[p].paid=true}else if(d!==undefined){D.items.splice(+d,1)}else return;save();render()};

function ntext(){const co=D.profile.company||CO[cur].n;return `${co}\n\nVous êtes en retard de ${D.maxLate} jour${D.maxLate>1?"s":""}. Vous n’avez pas payé : chaque jour, des intérêts de ${fm(RATE)} s’ajoutent.\n\nÀ chaque jour de retard, les intérêts augmentent. Vous n’êtes pas obligé de payer toute la somme d’un coup, mais payez le plus vite possible.`}
$("nopen").onclick=()=>{$("ntx").style.whiteSpace="pre-line";$("ntx").textContent=ntext();$("nerr").textContent="";$("dn").showModal()};
$("nclose").onclick=()=>$("dn").close();
$("npdf").onclick=async()=>{try{const J=window.jspdf.jsPDF,d=new J();
 d.addImage(LOGO,"PNG",15,12,62,21.4);d.setFontSize(22);d.setTextColor(214,40,40);d.text("Avis de retard",105,55,{align:"center"});
 d.setTextColor(20,20,20);d.setFontSize(13);d.text(d.splitTextToSize(ntext(),170),20,75);
 d.setFont(undefined,"bold");d.text("InvestiSoft",190,170,{align:"right"});
 const blob=d.output("blob");let dl=null;try{dl=window.claude&&await claude.use("downloads")}catch(e){}
 if(dl){await dl.save({filename:"avis-de-retard-investisoft.pdf",data:blob})}else{d.save("avis-de-retard-investisoft.pdf")}
 }catch(e){if(!e||e.code!=="declined")$("nerr").textContent="Le téléchargement n’a pas pu se faire. Réessayez."}};


$("sback").onclick=()=>show("v-dash");


document.querySelector(".pl").onclick=e=>{const b=e.target.closest("button");if(!b)return;dur=[b.dataset.d,b.dataset.p];[...b.parentNode.children].forEach(x=>x.setAttribute("aria-pressed",x===b))};
let pm="";
$("pay").onclick=e=>{if(!dur){e.preventDefault();$("serr").textContent="Choisissez d’abord une durée.";return}
 $("serr").textContent="";const co=D.profile.company||CO[cur].n;
 pm=`${co}\n\nNous voulons payer l’abonnement (${dur[0]}, ${fm(dur[1])}). Je vous ai déjà fait le dépôt, ou je veux vous faire le dépôt dès maintenant. Envoyez-moi votre numéro de téléphone.`;
 $("pmsg").textContent=pm;["pmsg","phint","pcopy"].forEach(i=>$(i).classList.remove("hide"));
 try{navigator.clipboard.writeText(pm)}catch(x){}};
$("pcopy").onclick=async()=>{try{await navigator.clipboard.writeText(pm);$("pcopy").textContent="Message copié"}catch(e){$("pcopy").textContent="Sélectionnez le message ci-dessus pour le copier"}};
const ACT="ABO-2026",OPEN=[9,30],CLOSE=[15,0];
let okc=false,OWN=false;
const fd=s=>s.split("-").reverse().join("/");
const today=()=>{const t=new Date();return t.getFullYear()+"-"+String(t.getMonth()+1).padStart(2,"0")+"-"+String(t.getDate()).padStart(2,"0")};
function subStat(){const s=D.sub;
 if(s&&s.exp>=today()){const n=Math.round((new Date(s.exp+"T00:00:00")-new Date(today()+"T00:00:00"))/864e5);
  $("actin").classList.add("hide");$("actok").classList.remove("hide");
  $("astat").textContent=`Abonnement actif jusqu’au ${fd(s.exp)} (${n} jour${n>1?"s":""} restant${n>1?"s":""}).`;return true}
 if(s){D.sub=null;save();$("aerr").textContent="Votre abonnement a expiré. Entrez un nouveau code pour le renouveler."}
 $("actin").classList.remove("hide");$("actok").classList.add("hide");return false}
function openSub(){["pmsg","phint","pcopy"].forEach(i=>$(i).classList.add("hide"));$("serr").textContent="";okc=false;$("ac").value="";$("ac").disabled=false;$("adbox").classList.add("hide");$("aok").textContent="Valider le code";$("aerr").textContent="";subStat();show("v-sub")}
$("tosub").onclick=openSub;
$("aok").onclick=()=>{
 if(!okc){if($("ac").value.trim().toUpperCase()!==ACT){$("aerr").textContent="Code incorrect. Vérifiez le code reçu et réessayez.";return}
  okc=true;$("ac").disabled=true;$("aerr").textContent="";$("ae").min=today();$("ae").value="";$("adbox").classList.remove("hide");$("aok").textContent="Valider la date";return}
 const e=$("ae").value;if(!e||e<today()){$("aerr").textContent="Choisissez une date d’expiration à partir d’aujourd’hui.";return}
 D.sub={exp:e};save();$("aerr").textContent="";subStat()};
function openCards(){if(!subStat()){show("v-sub");return}
 $("c3info").textContent=`Toutes les couleurs de vos cartes de réduction. Valables jusqu’au ${fd(D.sub.exp)}.`;
 const nm=esc(D.profile.company||CO[cur].n);
 $("gc").innerHTML=COLORS.map(c=>`<div class="gcard" style="background:${c[1]};color:${c[0]==="Jaune"?"#111":"#fff"}"><small>Carte de réduction</small><b>${nm}</b><span>${c[0]} · jusqu’au ${fd(D.sub.exp)}</span></div>`).join("")+`<div class="gcard off"><small>Carte de réduction</small><b>Orange</b><span>Non disponible</span></div>`;
 show("v-cards")}
$("to3").onclick=openCards;$("c3back").onclick=openSub;
const mi=a=>a[0]*60+a[1],fh=a=>a[0]+"h"+(a[1]?String(a[1]).padStart(2,"0"):"");
function isOpen(){if(OWN)return true;const n=new Date(),m=n.getHours()*60+n.getMinutes(),o=mi(OPEN),c=mi(CLOSE);return o<c?(m>=o&&m<c):(m>=o||m<c)}
$("hrs").textContent=`Le site est ouvert de ${fh(OPEN)} à ${fh(CLOSE)}.`;
function clock(){const op=isOpen(),cl=!$("v-closed").classList.contains("hide");
 if(!op&&!cl){$("dcode").close();$("dn").close();$("ctx").textContent=`Le site est ouvert de ${fh(OPEN)} à ${fh(CLOSE)}. Revenez pendant ces heures.`;show("v-closed")}
 else if(op&&cl){show(last)}}
clock();setInterval(clock,30000);
const nz=s=>s.normalize("NFD").replace(/[\u0300-\u036f\s]/g,"").toLowerCase();
const OWC="frejus350";
const fut=()=>{const t=new Date();t.setDate(t.getDate()+30);return t.getFullYear()+"-"+String(t.getMonth()+1).padStart(2,"0")+"-"+String(t.getDate()).padStart(2,"0")};
function prep(i){cur=i;D=ld("is_"+CO[i].c)||{profile:null,items:[]};if(!D.profile)D.profile={email:"",company:CO[i].n,phone:""}}
function ownRender(){$("ocos").innerHTML=CO.map((c,i)=>`<div class="it"><div class="h"><span>${esc(c.n)}</span><span class="tag o">${c.c}</span></div><div class="acts"><button class="btn" data-o="${i}">Ouvrir sans code</button></div></div>`).join("");$("oact").textContent=ACT;$("ohrs").textContent=`${fh(OPEN)} à ${fh(CLOSE)}`}
$("own").onclick=()=>{$("oc").value="";$("oerr").textContent="";$("downer").showModal();$("oc").focus()};
$("ono").onclick=()=>$("downer").close();
function ownLogin(){if(nz($("oc").value)!==OWC){$("oerr").textContent="Code incorrect. Vérifiez et réessayez.";return}
 $("downer").close();OWN=true;ownRender();ownAcc();ownDue();show("v-owner");clock()}
$("ook").onclick=ownLogin;$("oc").onkeydown=e=>{if(e.key==="Enter")ownLogin()};
$("ocos").onclick=e=>{const i=e.target.dataset.o;if(i===undefined)return;prep(+i);dash()};
$("o2").onclick=()=>{prep(0);openSub()};
$("o3").onclick=()=>{prep(0);const had=D.sub;if(!had)D.sub={exp:fut()};openCards();if(!had)D.sub=null};
$("oout").onclick=()=>{OWN=false;cur=null;D=null;show("v-home");clock()};
let DB=null;
let UID=null;(async()=>{try{if(window.claude){DB=await claude.use("db");const U=await claude.use("user");if(DB&&U)UID=await U.id()}}catch(e){}})();
function syncUp(){if(!DB||!UID||OWN)return;try{const list=CO.map(c=>{const l=ld("is_"+c.c);return l?{code:c.c,name:c.n,profile:l.profile||{},items:l.items||[],sub:l.sub?l.sub.exp:""}:null}).filter(Boolean);if(!list.length)return;DB.doc("companies/"+UID).set({list,at:Date.now()}).catch(()=>{})}catch(e){}}
function ownAcc(){const a=ld("is_owner")||{};$("on").value=a.n||"";$("oe").value=a.e||"";$("oh").textContent=a.n?"Espace propriétaire · "+a.n:"Espace propriétaire"}
$("osave").onclick=()=>{const n=$("on").value.trim(),e=$("oe").value.trim();
 if(!n||!/^\S+@\S+\.\S+$/.test(e)){$("oacc").textContent="Entrez votre nom et une adresse e-mail valide.";return}
 sv("is_owner",{n,e});$("oacc").textContent="";ownAcc();$("osave").textContent="Compte enregistré";setTimeout(()=>{$("osave").textContent="Enregistrer mon compte"},2000)};
async function ownDue(){const rows=[];
 let docs=[];if(DB){try{const s=await DB.collection("companies").get();docs=s.docs.map(x=>x.data()||{})}catch(e){}}
 for(const c of CO){const es=[];docs.forEach(x=>(Array.isArray(x.list)?x.list:[]).forEach(e=>{if(e&&e.code===c.c)es.push(e)}));
  if(!es.length){const l=ld("is_"+c.c);if(l)es.push({profile:l.profile,items:l.items,sub:l.sub?l.sub.exp:""})}
  if(es.length)es.forEach(e=>rows.push([c,e]));else rows.push([c,null])}
 $("dbn").textContent=DB?"Données envoyées par vos clients, mises à jour à chaque ouverture de cet écran.":"Les données partagées ne sont pas disponibles ici : seules les données de cet appareil sont affichées.";
 $("odue").innerHTML=rows.map(([c,d])=>{
  const it=(d&&Array.isArray(d.items))?d.items:[];let tot=0,late=false;
  const ls=it.map(x=>{const p=Number(x.p)||0,dd=x.paid?0:(days(String(x.e))||0),iv=dd*RATE;if(!x.paid){tot+=p+iv;if(dd)late=true}
   return `<div class="mut">• ${esc(x.a||"")} : ${x.paid?"payé":fm(p)+(dd?` · retard ${dd} j · intérêts ${fm(iv)}`:" · dans les délais")}</div>`}).join("");
  const pf=(d&&d.profile)||{};
  return `<div class="it${late?" l":""}"><div class="h"><span>${esc(c.n)}</span><span class="tag ${tot?"l":"o"}">${tot?"Doit "+fm(tot):"À jour"}</span></div><div class="mut">${esc(pf.email||"E-mail non renseigné")} · ${esc(pf.phone||"Téléphone non renseigné")}</div>${ls||'<div class="mut">Aucun achat à crédit.</div>'}<div class="mut">Abonnement : ${d&&d.sub?"jusqu’au "+esc(fd(String(d.sub))):"aucun"}</div></div>`}).join("")}
</script></body></html>
