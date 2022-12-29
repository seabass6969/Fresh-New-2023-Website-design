<script>
    let y
</script>

<svelte:window bind:scrollY={y}/>

<main>
    <div class="toptitle"><span class="toptext">Things always start with nothing</span></div>
<div class="textmoving"><p style="transform: translateX({y*-0.1}px)">DEV SVELTE CSS JAVASCRIPT GIT HTML PYTHON PROGRAMMING</p></div>
<div class="textmoving"><p style="transform: translateX(calc({y*0.1}px - 100px))">CEPHAS CEPHAS CEPHAS CEPHAS CEPHAS CEPHAS CEPHAS CEPHAS CEPHAS </p></div>
<div class="textmoving"><p style="transform: translateX({y*-0.1}px)">YOU'RE DEFINITELY NOT IN A CRAZY DUMPSTER FIRE!!! YOU'RE DEFINITELY</p></div>
<div class="center normalfont">

</div>
<div class="center normalfont">Hello <div class="wavehand">👋</div> </div>
    <div class="center normalfont">I learn programming, Linux and so much more by myself.</div>
    <div class="center normalfont">I would like to learn more!</div>
    <div class="center normalfont">Got question?  <a href="mailto:cephas@cephas.monster">Contact me</a></div>
    <div class="center normalfont">Project:</div>
    <div class="lefttwobox">
        <div class="boxsquare">
    <span class="centraltext clickfordetail"><span class="material-symbols-outlined">ads_click</span><span class="text">click for details</span> </span>
        </div>
        <div class="boxsquare">
    <span class="centraltext clickfordetail"><span class="material-symbols-outlined">ads_click</span><span class="text">click for details</span> </span>
        </div>
        <div class="boxsquare">
    <span class="centraltext clickfordetail"><span class="material-symbols-outlined">ads_click</span><span class="text">click for details</span> </span>
        </div>
        <div class="boxsquare">
    <span class="centraltext clickfordetail"><span class="material-symbols-outlined">ads_click</span><span class="text">click for details</span> </span>
        </div>
    </div>
</main>
<img src="/assets/ArrowDown.svg" alt="" class="floating">
<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Courier+Prime&family=Sacramento&display=swap');
.toptitle{
    display: flex;
    align-items: center;
    justify-content: center;
    font-family: 'Sacramento', cursive;
    font-size: 8rem; 
    height: 100vh;
    width: 100vw;
    background-color: black;
    color: white;
    user-select: none;
    @media (max-width: 600px){
        font-size: 5rem;
    }
}

.toptext{
    animation: red_line_across 1000ms alternate;
}
@keyframes red_line_across{
    from {
    filter: blur(10px);
    }
    to {
    filter: blur(0px);
    }
}
.boxsquare{
    margin: calc(20vw/8);
    width: calc(80vw/4);
    height: calc(80vw/4);
    background: #D9D9D9;
    box-shadow: 10px 20px 20px rgba(0, 0, 0, 0.25);
    border-radius: 10px;
    @media (max-width: 600px){
        margin: calc(20vw/4);
        width: calc(80vw/2);
        height: calc(80vw/2);
    }
}
.lefttwobox{
    display: grid;
    justify-content: center;
    grid-template-columns: auto auto auto auto;
    grid-template-rows: auto;
    @media (max-width: 600px){
        grid-template-columns: auto auto ;
        grid-template-rows: auto auto;
    }
}
.floating {
    position: absolute;
    width: 50px;
    height: 50px;
    left: 50vw;
    top: 90vh;
}
.textmoving p{
    font-family: 'Courier Prime', monospace;
    font-size: 3rem;
    transform: translateX(-65px);
    width: 1000vw;
    overflow-x: hidden;
    @media (max-width: 600px){
        font-size: 2rem;
    }
}
.center{
    width: 100vw;
    display: grid;
    justify-content: center;
    padding: 1px;
    grid-template-columns: auto auto;
}
.normalfont{
    font-family: 'Courier Prime', monospace;
    font-size: 1.5rem;
}
.wavehand{
    animation: infinite wavehand 5000ms;
}
@keyframes wavehand{
    0%{
        transform: rotate(0deg);
    }
    5%{
        transform: rotate(20deg);
    }
    10%{
        transform: rotate(0deg);
    }
    15%{
        transform: rotate(20deg);
    }
    20%{
        transform: rotate(0deg);
    }
    100%{
        transform: rotate(0deg);
    }
}
.centraltext{
    display: flex;
    align-items: center;
}
.boxsquare .text{
    font-family: 'Courier Prime', monospace;
    font-size: 0.8rem;
    filter: opacity(0);
}
.boxsquare:hover .text{
animation: opacity 0.6s ease-in forwards;
}
@keyframes opacity{
    0%{
        filter: opacity(0);
    }
    100%{
        filter: opacity(1);
    }
}
</style>