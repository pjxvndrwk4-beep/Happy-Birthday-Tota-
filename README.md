<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Birthday</title>

<style>
body{
  margin:0;
  font-family:Arial;
  overflow:hidden;
  background: linear-gradient(-45deg,#ff6a88,#ff99ac,#fbc2eb,#a6c1ee);
  background-size: 400% 400%;
  animation: bg 8s ease infinite;
  color:#111;
}

@keyframes bg{
  0%{background-position:0% 50%}
  50%{background-position:100% 50%}
  100%{background-position:0% 50%}
}

.page{
  display:none;
  min-height:100vh;
  align-items:center;
  justify-content:center;
  padding:20px;
}

.active{display:flex}

.card{
  max-width:850px;
  background:rgba(255,255,255,.85);
  padding:30px;
  border-radius:20px;
  box-shadow:0 10px 30px rgba(0,0,0,.2);
  text-align:center;
}

h1,h2,p{margin:10px 0}

p{
  font-size:22px;
  line-height:2;
  white-space:pre-wrap;
}

button{
  padding:10px 20px;
  border:none;
  border-radius:25px;
  cursor:pointer;
  font-size:16px;
  margin:5px;
}

.btns{
  display:flex;
  justify-content:space-between;
  margin-top:20px;
}

#gift{
  font-size:100px;
  cursor:pointer;
}
</style>
</head>

<body>

<div class="page active">
  <div class="card">
    <div id="gift" onclick="go(1)">🎁</div>
    <h1>Happy Birthday 🎂</h1>
    <h2>اضغطي على الهدية</h2>
  </div>
</div>

<script>
const texts=[
`انهاردة يوم مميز بلنسبالك وطبعا بلنسبالي انا كمان يمكن مكنتش ف حياتك ف يوم زي دا بس انا مبسوط اوي اني بشاركك اليوم دا احلى يوم ف الدنيا كلها عشان نيرفانا جت فييه🙈♥️♥️`,

`من ساعة ما دخلتي حياتي ونتي مغيراها ومخلياني مركز ف كل التواريخ يوم زي دا انا عمري ف حياتي ما هنسى انك جيتي فيه🙈🙈`,

`انا اه يمكن ف مرة اتلخبط ف اليوم دا وقولتلك انه 15مش1 بس انا كنت مفكر كدا من ساعتها ونا بركز ف التواريخ جداا♥️♥️`,

`عايزك تعرفي اني بحبك اوي اوي اوي فوق ما تتخيلي... انتي كل حاجة ليا♥️♥️♥️`,

`ف يوم زي دا عايز اقولك انا اسف على كل حاجة دايقتك🥺♥️`,

`كل سنة ونتي طيبة يا اجمل بنت ف الدنيا♥️
يارب اشوفك ناجحة ومبسوطة دايما😍♥️`
];

let idx = 0;

// create pages
for(let i=0;i<texts.length;i++){
  let d = document.createElement("div");
  d.className = "page";
  d.innerHTML = `
  <div class="card">
    <p>${texts[i]}</p>
    <div class="btns">
      <button onclick="back()" ${i==0?'disabled':''}>⬅️ رجوع</button>
      <button onclick="next()" ${i==texts.length-1?'disabled':''}>التالي ➡️</button>
    </div>
  </div>`;
  document.body.appendChild(d);
}

const pages = document.querySelectorAll(".page");

function show(){
  pages.forEach((p,i)=>p.classList.toggle("active",i===idx));
}

function go(i){ idx=i; show(); }
function next(){ if(idx<pages.length-1){ idx++; show(); } }
function back(){ if(idx>0){ idx--; show(); } }
</script>

<!-- 🎉 Confetti قوي -->
<script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

<script>
function fire(){
  confetti({
    particleCount: 150,
    spread: 100,
    startVelocity: 60,
    origin: { y: 0.2 }
  });
}

fire();
setInterval(fire, 1200);
</script>

</body>
</html>
