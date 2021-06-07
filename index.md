---
layout: home
title: home
date: 2020-10-27
---



<div class="fireworks-container"></div> 
<div class="pyro retrotype-win" style="display:block;"></div>
<div>
    <div>
        <p>Sprite Chosen:<span id="sprite-chosen"></span></p>
            <small>
                <i class="fas fa-arrow-left fa-sm"></i> A
                <i class="fas fa-arrow-right fa-sm"></i> D
                <i class="fas fa-arrow-up fa-sm"></i> W
                <i class="fas fa-arrow-down fa-sm"></i> S
            </small>
        <br><br><br>
        <small>
            <i class="fas fa-palette fa-sm" id="prvo"></i>
            theme
            <br>
            <i class="fas fa-user-astronaut fa-sm"  onclick="changeSprite();"></i>
            sprite
            <br>
            <i class="far fa-compass fa-sm" id="chngmap"></i>
            map
        </small>
    </div>
    <div>
        <canvas class="center map"></canvas>
    </div>
</div>

<script>
    let prviBtn = document.getElementById('prvo');
    let btn = document.querySelector('#prvo');

    btn.addEventListener("click",function(){
        document.body.classList.toggle('theme1');
    });
</script>

<script>
function changeSprite() {
    let sprites = ['/assets/img/sprites/Gnome Soldier.png', '/assets/img/sprites/gnome-f-green_hat-SWEN.png','/assets/img/sprites/gnome-f-red_hat-SWEN.png','/assets/img/sprites/gnome-f-violet_hat-SWEN.png','/assets/img/sprites/gnome-m-green_hat-SWEN.png','/assets/img/sprites/gnome-m-red_hat-SWEN.png','/assets/img/sprites/orig-green_cap-SWEN.png','/assets/img/sprites/orig-red_cap-SWEN.png']

    var randomItem = sprites[Math.floor(Math.random()*sprites.length)];
    console.log(randomItem);
    loadImage(randomItem);
    console.log('[DEBUG] Sprite Changed');

    let name = randomItem.split("/",5)[4]
    let final = name.split(".png",1);
    document.getElementById('sprite-chosen').innerHTML = " " + final;
}
</script>

<script>
    let prvimBtn = document.getElementById('chngmap');
    let mbtn = document.querySelector('#chngmap');

    mbtn.addEventListener("click",function(){
        document.getElementsByClassName("map")[0].classList.toggle('map1');
    });
</script>