/* ---------- EXPÉRIENCES ---------- */
const JOBS=[
 {t:"Community Manager / Monteuse vidéo",c:"TF1",l:"Boulogne-Billancourt",d:"02.2026 — 09.2026",p:"Création de contenus vidéo engageants (2 vidéos par semaine) pour les réseaux sociaux de la Fondation, incluant tournage iPhone, montage sur Premiere Pro et adaptation des formats (LinkedIn, Instagram, TikTok).",tags:["Montage vidéo","Premiere Pro","Tournage iPhone","Réseaux sociaux","Formats courts"]},
 {t:"Assistante social media manager",c:"Orès Group",l:"Paris",d:"08.2024 — 12.2024",p:"Création de contenus engageants pour les plateformes digitales, en collaboration avec les équipes créatives selon la stratégie de marque. Gestion et modération des réseaux sociaux, planification et programmation des publications.",tags:["Social media","Création de contenus","Modération","Planification éditoriale"]},
 {t:"Créatrice de contenus digital pour les réseaux sociaux",c:"CANAL+",l:"Issy-les-Moulineaux",d:"08.2023 — 01.2024",p:"Création et partage de contenus pour les séries sur les réseaux sociaux, avec une planification stratégique des publications. Sélection des moments forts, production de vidéos et utilisation d'images pour créer des contenus accrocheurs.",tags:["Contenus séries","Production vidéo","Stratégie éditoriale","Réseaux sociaux"]},
 {t:"Community Manager",c:"Topito",l:"Paris",d:"01.2023 — 05.2023",p:"Management de la communauté (plus de 3 millions d'abonnés) du magazine web d'info-divertissement sur tous les réseaux sociaux (Facebook, Twitter, Instagram, YouTube). Suivi et reporting des performances.",tags:["Community management","Facebook","Twitter","Instagram","YouTube","Reporting"]},
 {t:"Assistante marketing",c:"Groupe Rocher (Petit Bateau, Natural Care)",l:"Paris",d:"04.2022 — 06.2022",p:"Soutien du Chef de Produit sur la coordination de projets de nouveaux lancements avec les équipes support. Analyse du marché, de la concurrence et des tendances. Veille réseaux sociaux, internet et blogs.",tags:["Marketing produit","Analyse marché","Veille","Coordination de projets"]}
];
document.getElementById('jobs').innerHTML=JOBS.map(j=>`
 <div class="job"><div><h4>${j.t}</h4><div class="co">${j.c}</div><div class="loc">${j.l}</div></div>
 <div class="date">${j.d}</div>
 <div><p>${j.p}</p><div class="tags">${j.tags.map(x=>`<span>${x}</span>`).join('')}</div></div></div>`).join('');

/* ---------- PROJETS : ICI TU AJOUTES TES CONTENUS ----------
 Chaque projet = { titre, legende, type, src }
   type "image"   → src = "mon-image.jpg" (vertical 9:16)
   type "video"   → src = "ma-video.mp4"  (vertical 9:16)
   type "youtube" → src = "https://www.youtube.com/embed/ID_DE_LA_VIDEO"
   type "image-h" / "video-h" / "youtube-h" → même chose en format horizontal 16:9
 Chaque série = { nom, items:[ ... ] }
 Copie-colle une ligne { ... }, pour ajouter un projet.
 Copie-colle un bloc { nom:..., items:[...] }, pour ajouter une série.
------------------------------------------------------------ */
const PROJETS={
 tf1:[
  {nom:"L'interview SPEEEEED — Des Boursiers de la Réussite",items:[
   {legende:"Lucie Algénir — Future productrice",type:"image",src:""},
   {legende:"Cynthia Lawson — Future ingénieure du son",type:"image",src:""},
   {legende:"Lorenzo Govi-Bartolomei — Futur journaliste",type:"image",src:""},
   {legende:"Selim Krouchi — Futur journaliste",type:"image",src:""}
  ]},
  {nom:"Les Verifs Top Chrono",items:[
   {legende:"Titre de la vidéo",type:"video",src:""}
  ]}
 ],
 canal:[
  {nom:"Contenus séries CANAL+",items:[
   {legende:"Nom de la série — type de contenu",type:"video",src:""},
   {legende:"Nom de la série — type de contenu",type:"video",src:""},
   {legende:"Nom de la série — type de contenu",type:"image",src:""}
  ]}
 ],
 ecole:[
  {nom:"Projets EFAP",items:[
   {legende:"Nom du projet — matière / année",type:"image-h",src:""},
   {legende:"Nom du projet — matière / année",type:"video-h",src:""}
  ]}
 ]
};

function media(it){
 const h=it.type.endsWith('-h'), k=it.type.replace('-h','');
 let inner='Ajoute ton contenu<br>(src vide)';
 if(it.src){
  if(k==='image') inner=`<img src="${it.src}" alt="${it.legende}" loading="lazy">`;
  else if(k==='video') inner=`<video src="${it.src}" controls playsinline preload="metadata"></video>`;
  else if(k==='youtube') inner=`<iframe src="${it.src}" allowfullscreen loading="lazy" title="${it.legende}"></iframe>`;
 }
 return `<figure class="card ${h?'h':''}"><figure>${inner}</figure><figcaption>${it.legende}</figcaption></figure>`;
}
Object.keys(PROJETS).forEach(k=>{
 document.getElementById('p-'+k).innerHTML=PROJETS[k].map(s=>`
  <div class="serie"><h5>${s.nom}</h5><div class="grid">
  ${s.items.map(it=>{const h=it.type.endsWith('-h');const m=media(it);
   return `<div class="card ${h?'h':''}">${m.replace(/^<figure class="card[^"]*">/,'').replace(/<\/figure>$/,'')}</div>`}).join('')}
  </div></div>`).join('');
});

/* ---------- MENU actif au scroll ---------- */
const links=[...document.querySelectorAll('#menu a')];
const ids=links.map(a=>document.querySelector(a.getAttribute('href')));
addEventListener('scroll',()=>{
 let i=0;ids.forEach((s,n)=>{if(s.getBoundingClientRect().top<innerHeight/2)i=n});
 links.forEach((a,n)=>a.classList.toggle('on',n===i));
},{passive:true});
