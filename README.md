# Birthday
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>🎁 Happy Birthday</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

body{
    font-family:Arial, Helvetica, sans-serif;
    background:linear-gradient(135deg,#ff9ecf,#ffd6ec,#fff);
    overflow-x:hidden;
    text-align:center;
    color:#fff;
}

.container{
    min-height:100vh;
    display:flex;
    justify-content:center;
    align-items:center;
    flex-direction:column;
    padding:20px;
}

h1{
    font-size:3rem;
    margin-bottom:15px;
}

p{
    font-size:1.1rem;
    max-width:700px;
    line-height:1.7;
}

.gift{
    width:180px;
    height:180px;
    margin:40px;
    cursor:pointer;
    position:relative;
    animation:bounce 2s infinite;
}

.box{
    width:180px;
    height:120px;
    background:#ff4d88;
    position:absolute;
    bottom:0;
    border-radius:10px;
}

.lid{
    width:190px;
    height:35px;
    background:#ff1f6a;
    position:absolute;
    top:25px;
    left:-5px;
    border-radius:8px;
    transition:.8s;
}

.ribbon-v{
    width:22px;
    height:180px;
    background:#ffd700;
    position:absolute;
    left:79px;
}

.ribbon-h{
    width:180px;
    height:22px;
    background:#ffd700;
    position:absolute;
    top:75px;
}

.open .lid{
    transform:rotate(-25deg) translateY(-70px);
}

#surprise{
    display:none;
    animation:fade 2s;
}

img{
    width:220px;
    border-radius:15px;
    margin:15px;
    box-shadow:0 10px 20px rgba(0,0,0,.25);
}

video{
    width:320px;
    max-width:90%;
    margin-top:20px;
    border-radius:15px;
}

button{
    padding:12px 25px;
    border:none;
    border-radius:30px;
    background:white;
    color:#ff2b73;
    font-size:18px;
    cursor:pointer;
    margin-top:25px;
}

button:hover{
    transform:scale(1.05);
}

.heart{
    position:fixed;
    color:#ff0066;
    animation:float 6s linear infinite;
    opacity:.8;
}

@keyframes float{
    from{
        transform:translateY(100vh) scale(.5);
    }
    to{
        transform:translateY(-100px) scale(1.6);
    }
}

@keyframes fade{
    from{opacity:0;}
    to{opacity:1;}
}

@keyframes bounce{
    50%{
        transform:translateY(-10px);
    }
}
</style>

</head>

<body>

<div class="container">

<h1>🎉 Happy Birthday ❤️</h1>

<p>
I made something just for you.<br><br>
Click the gift below when you're ready. 🎁
</p>

<div class="gift" onclick="openGift()" id="gift">
<div class="lid"></div>
<div class="box"></div>
<div class="ribbon-v"></div>
<div class="ribbon-h"></div>
</div>

<div id="surprise">

<h1>❤️ Happy Birthday, My Love ❤️</h1>

<p>

Even though miles separate us today,
my heart is always with you.

I hope today brings you endless smiles,
beautiful moments,
and all the happiness you deserve.

Thank you for being part of my life.

I can't wait for the day
when I can celebrate your birthday beside you.

Until then...

Please keep smiling,
keep shining,
and remember someone far away
is thinking about you every single day.

❤️ Happy Birthday ❤️

</p>

<br>

<!-- Replace photo.jpg with your image -->
<img src="photo.jpg" alt="Our Photo">

<br>

<!-- Replace birthday.mp4 with your video -->
<video controls>
<source src="birthday.mp4" type="video/mp4">
</video>

<br>

<!-- Replace song.mp3 with your song -->
<audio controls autoplay loop>
<source src="song.mp3" type="audio/mpeg">
</audio>

<br>

<button onclick="alert('I Love You ❤️')">
One More Surprise 💝
</button>

</div>

</div>

<script>

function openGift(){

document.getElementById("gift").classList.add("open");

setTimeout(()=>{
document.getElementById("surprise").style.display="block";
},700);

for(let i=0;i<70;i++){

let heart=document.createElement("div");

heart.className="heart";

heart.innerHTML="❤";

heart.style.left=Math.random()*100+"vw";

heart.style.fontSize=(15+Math.random()*30)+"px";

heart.style.animationDuration=(3+Math.random()*5)+"s";

document.body.appendChild(heart);

}

}

</script>

</body>
</html>
