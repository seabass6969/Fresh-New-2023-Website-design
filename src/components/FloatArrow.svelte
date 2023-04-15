<div class="floatdiv">
    <div class="floattest">Scroll Down for more</div>
    <img src="/assets/ArrowDown.svg" alt="" class="floating">
</div>
<style lang="scss">
    .floattest {
        font-family: 'Courier Prime', monospace;
        font-size: 1.3rem;
        user-select: none;
        position: absolute;
        color: black;
        width: 40vw;
        height: 50px;
        display: flex;
        align-items: center;
        justify-content: center;
        animation: forwards 1000ms floatingtext;
        @media (max-width: 600px){
            font-size: 0.7rem;
        }
    }
    .floatdiv:hover .floattest {
        animation: forwards 1000ms floatingtextun;
    }
    @keyframes floatingtextun {
        0%{
            color:black 
        }
        100%{
            color: white 
        }
    }
    @keyframes floatingtext {
        0%{
            color: white 
        }
        100%{
            color:black 
        }
    }
    .floatdiv{
        position: absolute;
        width: 40vw;
        height: 50px;
        left: 30vw;
        top: 90vh;
        display:flex;
        align-items: center;
        justify-content: center;
        color: white;
    }
    .floating {
        position:relative;
        width: 50px;
        height: 50px;
        animation: forwards 1000ms hoverfloat;
    }
    .floatdiv:hover .floating{
        animation: forwards 1000ms unhoverfloat;
    }
    @keyframes hoverfloat {
        0%{
            left: -16vw;
        }
        100%{
            left: 0;
            // left: calc(20vw - 25px)
        }
    }
    @keyframes unhoverfloat {
        0%{
            left: 0;
            // left: calc(20vw - 25px)
        }
        100%{
            left: -16vw;
        }
    }
</style>