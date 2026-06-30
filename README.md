<!DOCTYPE html>
<html lang="ar" dir="rtl"><head><meta charset="UTF-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>Happy Birthday</title>
<style>
body{margin:0;font-family:Arial;background:linear-gradient(135deg,#ffb6d9,#fff0f7,#ffe7f2,#ffd6e7);background-size:400% 400%;animation:bg 12s infinite;color:#111;overflow:hidden}
@keyframes bg{0%{background-position:0 50%}50%{background-position:100% 50%}100%{background-position:0 50%}}
.page{display:none;min-height:100vh;align-items:center;justify-content:center;padding:30px;position:relative;z-index:2}
.active{display:flex}.card{max-width:850px;background:rgba(255,255,255,.82);backdrop-filter:blur(5px);padding:35px;border-radius:20px;box-shadow:0 10px 30px rgba(0,0,0,.15)}
h1,h2,p{text-align:center;color:#111}p{font-size:24px;line-height:2;white-space:pre-wrap}.btns{display:flex;justify-content:space-between;margin-top:25px}
button{padding:12px 24px;border:none;border-radius:30px;font-size:18px;cursor:pointer}#gift{font-size:120px;text-align:center;cursor:pointer}
.balloon,.heart,.spark,.conf{position:fixed;pointer-events:none}
.balloon{width:26px;height:34px;border-radius:50%;background:#ff6fa8;animation:up 10s linear infinite}
.balloon:after{content:"";position:absolute;left:50%;top:34px;width:1px;height:30px;background:#999}
.heart{font-size:20px;animation:float 8s linear infinite}.spark{width:4px;height:4px;background:#fff;border-radius:50%;box-shadow:0 0 10px #fff;animation:tw 2s infinite}.conf{width:8px;height:8px;animation:fall 6s linear infinite}
@keyframes up{from{transform:translateY(110vh)}to{transform:translateY(-20vh)}}@keyframes float{from{transform:translateY(110vh)}to{transform:translateY(-20vh)}}@keyframes tw{50%{opacity:.2;transform:scale(.5)}}@keyframes fall{from{transform:translateY(-10vh) rotate(0)}to{transform:translateY(110vh) rotate(720deg)}}
</style></head><body>
<div class="page active"><div class="card"><div id="gift" onclick="go(1)">🎁</div><h1>Happy Birthday Nirvana 🎂</h1><h2>1 / 7 / 2004</h2><p>اضغطي على الهدية 🤍</p></div></div>
<script>
for(let i=0;i<15;i++){let b=document.createElement('div');b.className='balloon';b.style.left=Math.random()*100+'vw';b.style.animationDelay=Math.random()*10+'s';b.style.background=['#ff6fa8','#ffd166','#7bdff2','#b8f2e6'][i%4];document.body.appendChild(b);}
for(let i=0;i<25;i++){let h=document.createElement('div');h.className='heart';h.innerHTML='💖';h.style.left=Math.random()*100+'vw';h.style.animationDelay=Math.random()*8+'s';document.body.appendChild(h);}
for(let i=0;i<40;i++){let s=document.createElement('div');s.className='spark';s.style.left=Math.random()*100+'vw';s.style.top=Math.random()*100+'vh';s.style.animationDelay=Math.random()*2+'s';document.body.appendChild(s);}
for(let i=0;i<80;i++){let c=document.createElement('div');c.className='conf';c.style.left=Math.random()*100+'vw';c.style.background=['#f66','#6cf','#fd6','#9f6','#f6f'][i%5];c.style.animationDelay=Math.random()*6+'s';document.body.appendChild(c);}
const texts=[
`انهاردة يوم مميز بلنسبالك وطبعا بلنسبالي انا كمان يمكن مكنتش ف حياتك ف يوم زي دا بس انا مبسوط اوي اني بشاركك اليوم دا احلى يوم ف الدنيا كلها عشان نيرفانا جت فييه🙈♥️♥️`,
`من ساعة ما دخلتي حياتي ونتي مغيراها ومخلياني مركز ف كل التواريخ يوم زي دا انا عمري ف حياتي ما هنسى انك جيتي فيه🙈🙈`,
`انا اه يمكن ف مرة اتلخبط ف اليوم دا وقولتلك انه 15مش1 بس انا كنت مفكر كدا من ساعتها ونا بركز ف التواريخ جداا من ساعة الموقف دا فا عمري ما هنسى حاجة زي دي ابداا♥️♥️`,
`عايزك تعرفي ف يوم زي دا اني بحبك اوي اوي اوي فوق ما تتخيلي واني بموت فيكي انتي وبس انتي الوحيدة ال عرفتي تغيريني نفسي تعرفي اني عمري ما فكرت ولا هفكر ف حد غيرك نفسي تعرفي اني عمري ما حبيت قدك ولا هحبك قدك يا نيرفانا ف الدنياا كلهااا نفسي تعرفي انك حبيبتي وروحي ومفيش حد غيرك قاعد ومستريح وواخد مكانه ف قلبي غيرك انتي كل حاجة ليا♥️♥️♥️`,
`ف يوم زي دا عايز اقولك انا اسف اسف اسف ع اي حاجة عملتها دايقتك اسف ع كل حاجة عملتها حسستك انك مش مهمة عندي اسف ع كل حاجة عملتها حستتك انك مش موجودة ف حياتي اسف على كل حاجة يا نيرفانا انا بحبك وبموت فيكيي🥺♥️♥️♥️`,
`كل سنة ونتي طيبة يا اجمل واحن بنت ف الدنيا🌚♥️

كل سنة ونتي مميزة ومختلفة عن اي حد🥰♥️

كل سنة ونتي ناجحة ويارب اشوفك احسن دكتورة ف الدنيا😍♥️

بتمنى افضل اشوف ضحكتك دايما منورة الدنيا وتحققي كل ال نفسك فيه♥️

كل سنة ونتي طيبة يا حبيبتي وروح قلبي وافضل اشاركك اليوم دا🫂🥰♥️♥️♥️♥️♥️♥️`
];
let idx=0;
for(let i=0;i<texts.length;i++){let d=document.createElement('div');d.className='page';d.innerHTML=`<div class="card"><p>${texts[i]}</p><div class="btns"><button ${i==0?'disabled':''} onclick="back()">⬅️ رجوع</button><button ${i==texts.length-1?'disabled':''} onclick="next()">التالي ➡️</button></div></div>`;document.body.appendChild(d);}
const pages=document.querySelectorAll('.page');function show(){pages.forEach((p,n)=>p.classList.toggle('active',n===idx));}
function go(i){idx=i;show();}function next(){if(idx<pages.length-1){idx++;show();}}function back(){if(idx>1){idx--;show();}else if(idx===1){idx=0;show();}}
</script></body></html>
