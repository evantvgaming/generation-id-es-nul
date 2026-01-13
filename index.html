const ideaEl = document.getElementById("idea");
const genBtn = document.getElementById("genBtn");
const copyBtn = document.getElementById("copyBtn");
const shareBtn = document.getElementById("shareBtn");
const toastEl = document.getElementById("toast");
const modeToggle = document.getElementById("modeToggle");
const countEl = document.getElementById("count");
const clearBtn = document.getElementById("clearBtn");

const storeKey = "badIdeas_history_v1";

const base = {
  objets: [
    "un grille-pain", "un parapluie", "une chaise", "un frigo", "un réveil",
    "une trottinette", "un micro-ondes", "un oreiller", "un aspirateur", "un casque audio"
  ],
  actions: [
    "qui insulte poliment", "qui fait l’inverse de sa fonction", "qui te juge en silence",
    "qui marche seulement quand il pleut", "qui se déclenche au pire moment",
    "qui demande un abonnement", "qui fait des bruits de dauphin", "qui veut être ton manager"
  ],
  buts: [
    "pour augmenter la productivité", "pour économiser l’énergie", "pour améliorer le sommeil",
    "pour impressionner tes voisins", "pour remplacer les réunions", "pour éviter de réfléchir",
    "pour rendre la vie plus compliquée", "pour le plaisir du chaos"
  ]
};

const ultra = {
  objets: [
    "un frigo émotionnel", "un clavier susceptible", "un GPS mythomane", "une brosse à dents connectée",
    "un tapis qui glisse exprès", "une sonnette qui fait des miaulements", "un pantalon intelligent (mais méchant)"
  ],
  actions: [
    "qui te facture à la syllabe", "qui change de langue au milieu", "qui te ghoste",
    "qui t’oblige à faire une mise à jour", "qui te propose une formation LinkedIn", "qui applaudit quand tu échoues"
  ],
  buts: [
    "pour ruiner ton estime de toi", "pour créer une startup inutile", "pour devenir viral 3 minutes",
    "pour provoquer la police du bon goût", "pour transformer ton salon en open-space"
  ]
};

function pick(arr){ return arr[Math.floor(Math.random() * arr.length)]; }

function loadHistory(){
  try { return JSON.parse(localStorage.getItem(storeKey) || "[]"); }
  catch { return []; }
}

function saveHistory(list){
  localStorage.setItem(storeKey, JSON.stringify(list.slice(0, 50)));
}

function setToast(msg){
  toastEl.textContent = msg;
  if (msg) setTimeout(() => { if (toastEl.textContent === msg) toastEl.textContent = ""; }, 1600);
}

function generateIdea(){
  const pack = modeToggle.checked ? ultra : base;
  const idea = `💡 ${pick(pack.objets)} ${pick(pack.actions)} ${pick(pack.buts)}.`;
  ideaEl.textContent = idea;

  const hist = loadHistory();
  hist.unshift({ idea, ts: Date.now() });
  saveHistory(hist);

  countEl.textContent = String(hist.length);
  return idea;
}

async function copyIdea(){
  const text = ideaEl.textContent.trim();
  if (!text) return;
  try {
    await navigator.clipboard.writeText(text);
    setToast("Copié ✅");
  } catch {
    setToast("Copie impossible (navigateur relou) 😤");
  }
}

async function shareIdea(){
  const text = ideaEl.textContent.trim();
  if (!text) return;

  if (navigator.share) {
    try {
      await navigator.share({ title: "Idée Nulle™", text });
      setToast("Partagé 📣");
      return;
    } catch {
      // user cancelled → no drama
      setToast("");
      return;
    }
  }

  // Fallback: copy to clipboard
  await copyIdea();
  setToast("Pas de partage natif → copié 📋");
}

function clearHistory(){
  localStorage.removeItem(storeKey);
  countEl.textContent = "0";
  setToast("Historique effacé 🧼");
}

(function init(){
  const hist = loadHistory();
  countEl.textContent = String(hist.length);
  genBtn.addEventListener("click", generateIdea);
  copyBtn.addEventListener("click", copyIdea);
  shareBtn.addEventListener("click", shareIdea);
  clearBtn.addEventListener("click", clearHistory);
})();
