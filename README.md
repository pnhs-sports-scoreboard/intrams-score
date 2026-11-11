
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>IntramsScore | Official Scoring System</title>
<style>
:root {
  --navy:#101d38;
  --navy2:#192c50;
  --gold:#d6b15d;
  --light:#f5f6fa;
  --white:#fff;
  --muted:#8792a5;
  --border:#e5e8ef;
}
*{box-sizing:border-box}
body{
 margin:0;background:var(--light);color:#202b40;
 font-family:Arial,sans-serif;
}
header{
 background:linear-gradient(130deg,#0d1931,#20385f);
 color:white;padding:25px 6%;
 border-bottom:4px solid var(--gold);
}
.brand{display:flex;align-items:center;gap:14px}
.logo{
 width:49px;height:49px;border:2px solid var(--gold);
 color:var(--gold);border-radius:12px;
 display:grid;place-items:center;font-size:25px;
}
.brand h1{font-size:23px;margin:0;letter-spacing:1px}
.brand p{margin:5px 0 0;color:#c6cede;font-size:12px}
.header-bottom{
 display:flex;justify-content:space-between;
 align-items:center;gap:12px;flex-wrap:wrap;margin-top:25px;
}
.header-bottom h2{margin:0;font-size:25px}
.header-bottom p{color:#c6cede;margin:7px 0 0;font-size:13px}
.status{color:var(--gold);font-size:12px;letter-spacing:1px}
main{max-width:1250px;margin:25px auto;padding:0 18px}
.stats{
 display:grid;grid-template-columns:repeat(3,1fr);gap:15px;
}
.stat,.panel{
 background:white;border:1px solid var(--border);
 border-radius:13px;padding:20px;
 box-shadow:0 3px 12px #17274608;
}
.stat small{color:var(--muted);font-size:11px;letter-spacing:1px}
.stat strong{display:block;font-size:27px;margin-top:10px;color:var(--navy)}
.section-title{
 display:flex;justify-content:space-between;
 align-items:center;gap:10px;margin-bottom:17px;flex-wrap:wrap;
}
.section-title h3{margin:0;color:var(--navy);font-size:17px}
.panel{margin-top:20px}
button{
 border:0;border-radius:7px;padding:11px 15px;
 background:var(--navy);color:white;font-weight:bold;
 cursor:pointer;font-size:12px;
}
button:hover{opacity:.88}
button.gold{background:var(--gold);color:#17223a}
button.light{background:#edf0f5;color:var(--navy)}
button.danger{background:#fce9e9;color:#a33232}
input,select{
 padding:11px;border:1px solid var(--border);
 border-radius:7px;background:white;color:#202b40;
 min-width:0;width:100%;font-size:13px;
}
input:focus,select:focus{outline:2px solid #d6b15d80}
.team-grid{
 display:grid;grid-template-columns:repeat(2,1fr);gap:12px;
}
.team-item{
 display:flex;align-items:center;gap:9px;
 padding:12px;border:1px solid var(--border);
 border-radius:9px;background:#fafbfe;
}
.team-item input{flex:1}
.team-color{width:10px;height:10px;border-radius:50%;flex-shrink:0}
.table-wrap{overflow-x:auto}
table{border-collapse:collapse;width:100%;min-width:520px}
th{
 background:#f3f5f9;color:#64718a;
 text-align:left;font-size:10px;letter-spacing:1px;
 padding:13px;
}
td{padding:14px 13px;border-bottom:1px solid var(--border);font-size:13px}
.rank{font-weight:bold;color:#a27b27}
.total{font-weight:bold;color:var(--navy);font-size:16px}
.event-form{
 display:grid;grid-template-columns:2fr 1fr auto;gap:10px;
 margin-bottom:16px;
}
.event-card{
 border:1px solid var(--border);border-radius:10px;
 margin-top:13px;overflow:hidden;
}
.event-head{
 padding:14px;background:#f7f8fb;
 display:flex;justify-content:space-between;
 align-items:center;gap:10px;
}
.event-head strong{color:var(--navy);font-size:14px}
.event-head small{color:var(--muted)}
.event-body{padding:15px}
.placement-grid{
 display:grid;grid-template-columns:repeat(2,1fr);gap:12px;
}
.placement{display:flex;flex-direction:column;gap:6px}
.placement label{font-size:12px;font-weight:bold}
.event-footer{
 display:flex;justify-content:space-between;
 align-items:center;gap:10px;margin-top:15px;flex-wrap:wrap;
}
.event-footer small{color:var(--muted)}
.empty{text-align:center;color:var(--muted);padding:25px;font-size:13px}
footer{
 text-align:center;padding:28px;color:#8490a2;font-size:11px;
}
@media(max-width:600px){
 header{padding:20px}
 .stats{grid-template-columns:repeat(3,1fr);gap:7px}
 .stat{padding:12px}
 .stat strong{font-size:21px}
 .stat small{font-size:9px}
 .team-grid,.placement-grid{grid-template-columns:1fr}
 .event-form{grid-template-columns:1fr}
 .header-bottom h2{font-size:21px}
}
</style>
</head>
<body>

<header>
 <div class="brand">
  <div class="logo">🏆</div>
  <div>
   <h1>INTRAMSCORE</h1>
   <p>OFFICIAL INTRAMURALS SCORING SYSTEM</p>
  </div>
 </div>
 <div class="header-bottom">
  <div>
   <h2>Team Scoreboard</h2>
   <p>Track every event. Calculate every point. Celebrate every victory.</p>
  </div>
  <div class="status">● LIVE SCOREBOARD</div>
 </div>
</header>

<main>
 <div class="stats">
  <div class="stat">
   <small>TOTAL TEAMS</small>
   <strong id="teamCount">4</strong>
  </div>
  <div class="stat">
   <small>TOTAL EVENTS</small>
   <strong id="eventCount">0</strong>
  </div>
  <div class="stat">
   <small>TOP TEAM</small>
   <strong id="leader" style="font-size:17px">—</strong>
  </div>
 </div>

 <section class="panel">
  <div class="section-title">
   <h3>01 / TEAM MANAGEMENT</h3>
   <button class="gold" onclick="addTeam()">+ Add Team</button>
  </div>
  <div class="team-grid" id="teams"></div>
 </section>

 <section class="panel">
  <div class="section-title">
   <h3>02 / OVERALL LEADERBOARD</h3>
   <span style="font-size:11px;color:#8792a5">AUTOMATIC RANKING</span>
  </div>
  <div class="table-wrap">
   <table>
    <thead>
     <tr>
      <th>RANK</th><th>TEAM</th><th>EVENTS WON</th>
      <th>TOTAL POINTS</th>
     </tr>
    </thead>
    <tbody id="leaderboard"></tbody>
   </table>
  </div>
 </section>

 <section class="panel">
  <div class="section-title">
   <h3>03 / EVENT MANAGEMENT</h3>
  </div>
  <div class="event-form">
   <input id="eventName" placeholder="Enter sport or event name">
   <select id="eventCategory">
    <option>Sports</option>
    <option>Games</option>
    <option>Special Events</option>
    <option>Other</option>
   </select>
   <button class="gold" onclick="addEvent()">+ Add Event</button>
  </div>
  <div id="events">
   <div class="empty">No events added yet. Add your first event above.</div>
  </div>
 </section>

 <section class="panel">
  <div class="section-title">
   <h3>04 / POINTS SYSTEM</h3>
  </div>
  <div class="table-wrap">
   <table>
    <thead><tr><th>PLACEMENT</th><th>AWARDED POINTS</th></tr></thead>
    <tbody>
     <tr><td>🥇 1st Place</td><td><b>100 Points</b></td></tr>
     <tr><td>🥈 2nd Place</td><td><b>75 Points</b></td></tr>
     <tr><td>🥉 3rd Place</td><td><b>50 Points</b></td></tr>
     <tr><td>4th Place</td><td><b>25 Points</b></td></tr>
    </tbody>
   </table>
  </div>
 </section>
</main>

<footer>
 INTRAMSCORE · OFFICIAL TEAM SCORING SYSTEM<br>
 Excellence • Sportsmanship • Unity
</footer>

<script>
const colors=["#243d69","#a47d35","#637c9d","#92734c",
"#526b62","#75658f","#9b625c","#5e7780"];

let teams=[
 {id:1,name:"Team 1"},
 {id:2,name:"Team 2"},
 {id:3,name:"Team 3"},
 {id:4,name:"Team 4"}
];
let events=[];
let nextTeam=5;
let nextEvent=1;

function save(){
 localStorage.setItem("intramsScoreData",JSON.stringify({
  teams,events,nextTeam,nextEvent
 }));
}

function load(){
 try{
  const data=JSON.parse(localStorage.getItem("intramsScoreData"));
  if(data){
   teams=data.teams||teams;
   events=data.events||[];
   nextTeam=data.nextTeam||5;
   nextEvent=data.nextEvent||1;
  }
 }catch(e){}
}

function addTeam(){
 const name=prompt("Enter the new team name:");
 if(!name||!name.trim())return;
 if(teams.some(t=>t.name.toLowerCase()===name.trim().toLowerCase())){
  alert("This team name already exists.");return;
 }
 teams.push({id:nextTeam++,name:name.trim()});
 save();render();
}

function renameTeam(id,value){
 const team=teams.find(t=>t.id===id);
 if(!team)return;
 const name=value.trim();
 if(!name)return;
 if(teams.some(t=>t.id!==id&&t.name.toLowerCase()===name.toLowerCase())){
  alert("This team name already exists.");render();return;
 }
 team.name=name;
 save();render();
}

function addEvent(){
 const input=document.getElementById("eventName");
 const name=input.value.trim();
 if(!name){alert("Please enter an event name.");return;}
 if(teams.length<1){alert("Add at least one team first.");return;}
 events.push({
  id:nextEvent++,
  name,
  category:document.getElementById("eventCategory").value,
  places:{}
 });
 input.value="";
 save();render();
}

function deleteEvent(id){
 if(!confirm("Delete this event and its scores?"))return;
 events=events.filter(e=>e.id!==id);
 save();render();
}

const points={1:100,2:75,3:50,4:25};

function changePlace(eventId,teamId,value){
 const event=events.find(e=>e.id===eventId);
 if(!event)return;
 const place=value===""?null:Number(value);

 if(place!==null){
  const alreadyUsed=Object.entries(event.places).some(
   ([id,p])=>Number(id)!==teamId&&p===place
  );
  if(alreadyUsed){
   alert("This placement is already assigned to another team.");
   render();return;
  }
 }
 if(place===null)delete event.places[teamId];
 else event.places[teamId]=place;

 save();render();
}

function totals(){
 const result=teams.map(t=>{
  let total=0,wins=0;
  events.forEach(e=>{
   const p=e.places[t.id];
   if(p){
    total+=points[p]||0;
    if(p===1)wins++;
   }
  });
  return {...t,total,wins};
 });
 return result.sort((a,b)=>b.total-a.total||b.wins-a.wins);
}

function renderTeams(){
 document.getElementById("teams").innerHTML=teams.map((t,i)=>`
  <div class="team-item">
   <span class="team-color" style="background:${colors[i%colors.length]}"></span>
   <input aria-label="Team name" value="${escapeHTML(t.name)}"
    onchange="renameTeam(${t.id},this.value)">
  </div>
 `).join("");
}

function renderLeaderboard(){
 const sorted=totals();
 document.getElementById("leaderboard").innerHTML=sorted.length?
 sorted.map((t,i)=>`
  <tr>
   <td class="rank">${i+1===1?"🥇":i+1===2?"🥈":i+1===3?"🥉":i+1}</td>
   <td><b>${escapeHTML(t.name)}</b></td>
   <td>${t.wins}</td>
   <td class="total">${t.total} pts</td>
  </tr>
 `).join(""):`<tr><td colspan="4" class="empty">No teams yet.</td></tr>`;

 document.getElementById("teamCount").textContent=teams.length;
 document.getElementById("eventCount").textContent=events.length;
 document.getElementById("leader").textContent=
  sorted.length&&sorted[0].total>0?sorted[0].name:"—";
}

function renderEvents(){
 const container=document.getElementById("events");
 if(!events.length){
  container.innerHTML='<div class="empty">No events added yet. Add your first event above.</div>';
  return;
 }

 container.innerHTML=events.map(e=>{
  const sorted=teams.slice().sort((a,b)=>
   (e.places[a.id]||99)-(e.places[b.id]||99)
  );
  return `
   <div class="event-card">
    <div class="event-head">
     <div>
      <strong>${escapeHTML(e.name)}</strong><br>
      <small>${escapeHTML(e.category)}</small>
     </div>
     <button class="danger" onclick="deleteEvent(${e.id})">Delete</button>
    </div>
    <div class="event-body">
     <div class="placement-grid">
      ${teams.map(t=>`
       <div class="placement">
        <label>${escapeHTML(t.name)}</label>
        <select aria-label="Placement for ${escapeHTML(t.name)}"
         onchange="changePlace(${e.id},${t.id},this.value)">
         <option value="">Not assigned</option>
         ${[1,2,3,4].map(p=>`
          <option value="${p}" ${e.places[t.id]===p?"selected":""}>
           ${p}${p===1?"st":p===2?"nd":p===3?"rd":"th"} Place — ${points[p]} pts
          </option>
         `).join("")}
        </select>
       </div>
      `).join("")}
     </div>
     <div class="event-footer">
      <small>Results are automatically added to the leaderboard.</small>
     </div>
    </div>
   </div>
  `;
 }).join("");
}

function escapeHTML(value){
 return String(value).replace(/[&<>"']/g,c=>({
  "&":"&amp;","<":"&lt;",">":"&gt;",
  '"':"&quot;","'":"&#39;"
 }[c]));
}

function render(){
 renderTeams();
 renderLeaderboard();
 renderEvents();
}

load();
render();
</script>
</body>
</html>
