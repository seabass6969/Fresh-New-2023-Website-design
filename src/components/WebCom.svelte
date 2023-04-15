<script>
    export let link = ""
    export let src = ""
</script>

        <div class="boxsquare">
    <a href={link}>
    <img src={src} alt="" class="image">
    </a>
    <span class="centraltext clickfordetail"><span class="material-symbols-outlined">ads_click</span><span class="text">click for details</span> </span>
        </div>
    <style lang="scss">
        .boxsquare{
    margin: calc(20vw/8);
    width: calc(80vw/4);
    height: calc(80vw/4);
    background: #D9D9D9;
    box-shadow: 10px 20px 20px rgba(0, 0, 0, 0.25);
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
span{
    user-select: none;
}
    </style>