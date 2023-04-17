<script>
    export let link = ""
    export let src = ""
    export let description = ''
    let dialogbox

</script>
    <dialog bind:this={dialogbox} class="dialogbox"> 
        <button on:click={()=> {dialogbox.close()}} class="closebutton">
            <span class="material-symbols-outlined">close</span>
        </button>
    <img src={src} alt="" class="imagealert">
    <h2>{description}</h2>
    <h1>
        <a href={link}>{link}</a>
    </h1>
    </dialog>
        <button class="boxsquare" on:click={()=>{dialogbox.showModal()}}>
    <img src={src} alt="" class="image">
    <span class="centraltext clickfordetail"><span class="material-symbols-outlined">ads_click</span><span class="text">click for details</span> </span>
        </button>
    <style lang="scss">
        .boxsquare{
    margin: calc(20vw/8);
    width: calc(80vw/4);
    height: calc(80vw/4);
    background: #D9D9D9; box-shadow: 10px 20px 20px rgba(0, 0, 0, 0.25);
    border-color: none;
    border-radius: 10px;
    display: grid;
    justify-content: center;
    @media (max-width: 600px){
        margin: calc(20vw/4);
        width: calc(80vw/2);
        height: calc(80vw/2);
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
    @media (max-width: 600px){
    font-size: 0.6rem;
    filter: opacity(1);
    }
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
.imagealert{
    margin: calc(3vw/8);
    width: 60vw;
    @media (max-width: 600px){
        margin: calc(3vw/4);
        width: 80vw;
    }
}
.image{
    margin: calc(3vw/8);
    width: calc(18vw);
    height: calc(80vw/4 - 5vw);
    @media (max-width: 600px){
        margin: calc(3vw/4);
        width: calc(80vw/2 - 10vw);
        height: calc(80vw/2 - 10vw);
    }
}
.closebutton {
    display: flex;
    align-items: center;
    justify-content: center;
    width: 30px;
    height: 30px;
    border-color: red;
    border-style:solid;
    border-radius: 10px;
}
    h1, h2{
        font-family: 'Courier Prime', monospace;
    }
    
    .dialogbox {
        background: rgb(42,100,192);
        background: radial-gradient(circle, rgba(42,100,192,1) 0%, rgba(255,255,243,1) 0%, rgba(246,255,240,1) 48%, rgba(255,239,254,1) 100%); 
        border-color: dimgrey;
        animation: forwards 400ms moveopen;
    }
    @keyframes moveopen {
        0%{
            transform: scale(0.1,0.1) rotate(180deg);
        }
        100%{
            transform: scale(1,1);
        }
    }
    </style>