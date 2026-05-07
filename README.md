<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Naniiicuts</title>

<style>
body {
    margin:0;
    font-family: 'Poppins', sans-serif;
    background:#0a0a0a;
    color:white;
    text-align:center;
    overflow-x:hidden;
}

/* PARTICLE BG */
canvas {
    position:fixed;
    top:0;
    left:0;
    z-index:-1;
}

/* CONTAINER */
.container {
    max-width:400px;
    margin:auto;
    padding:40px 20px;
}

/* PROFILE */
.profile img {
    width:120px;
    height:120px;
    border-radius:50%;
    border:3px solid #7a5cff;
    box-shadow:0 0 25px #7a5cff;
}

.profile h1 {
    margin:10px 0;
}

/* BUTTONS */
.btn {
    display:block;
    width:100%;
    margin:12px 0;
    padding:14px;
    border-radius:12px;
    text-decoration:none;
    color:white;
    background:#111;
    border:1px solid #7a5cff;
    box-shadow:0 0 10px #7a5cff;
    transition:0.3s;
}

.btn:hover {
    background:#7a5cff;
    box-shadow:0 0 30px #7a5cff;
    transform:scale(1.05);
}

/* SPOTIFY */
.spotify {
    margin-top:20px;
    border-radius:15px;
    overflow:hidden;
    box-shadow:0 0 25px #7a5cff;
}

/* FLOATING PLAYER */
.mini {
    position:fixed;
    bottom:15px;
    right:15px;
    width:180px;
    box-shadow:0 0 20px #7a5cff;
}

/* FLOATING WHATSAPP */
.whatsapp {
    position:fixed;
    bottom:15px;
    left:15px;
    background:#25D366;
    padding:12px 15px;
    border-radius:50%;
    font-size:20px;
    color:white;
    text-decoration:none;
    box-shadow:0 0 20px #25D366;
}

/* CAPTION */
.caption {
    margin-top:20px;
    font-size:13px;
    color:#aaa;
}
</style>
</head>

<body>

<canvas id="bg"></canvas>

<div class="container">

<div class="profile">
<img src="YOUR_IMAGE_LINK_HERE">
<h1>Naniiicuts</h1>
<p>Cinematic Editor • Viral Reels</p>
</div>

<a href="https://www.instagram.com/tonyyy.aep" class="btn">Instagram</a>
<a href="https://t.me/+916302959250" class="btn">Telegram</a>
<a href="https://open.spotify.com/playlist/6cbeD8QfZBKmvPQZ1ZO0F0" class="btn">Spotify</a>

<a href="https://wa.me/916302959250?text=Hey%20I%20want%20editing" class="btn">dm me </a>

<div class="spotify">
<iframe src="https://open.spotify.com/embed/playlist/6cbeD8QfZBKmvPQZ1ZO0F0"
width="100%" height="152"></iframe>
</div>

<div class="caption">
Turning clips into cinema 🎬<br>
DM for edits ⚡
</div>

</div>

<!-- MINI PLAYER -->
<div class="mini">
<iframe src="https://open.spotify.com/embed/playlist/6cbeD8QfZBKmvPQZ1ZO0F0"
width="100%" height="80"></iframe>
</div>

<!-- WHATSAPP FLOAT -->
<a href="https://wa.me/916302959250?text=Hey%20I%20want%20editing" class="whatsapp">💬</a>

<script>
const canvas = document.getElementById('bg');
const ctx = canvas.getContext('2d');
canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

let particles = [];
for(let i=0;i<70;i++){
particles.push({x:Math.random()*canvas.width,y:Math.random()*canvas.height});
}

function draw(){
ctx.clearRect(0,0,canvas.width,canvas.height);
ctx.fillStyle="#7a5cff";
particles.forEach(p=>{
p.y+=0.4;
if(p.y>canvas.height) p.y=0;
ctx.beginPath();
ctx.arc(p.x,p.y,2,0,Math.PI*2);
ctx.fill();
});
requestAnimationFrame(draw);
}
draw();
</script>

</body>
</html>
