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
            height: 25px;
        }
    }
    .floatdiv:hover .floattest {
        animation: forwards 1000ms floatingtextun;
    }
    @keyframes floatingtextun {
        0%{
            color: white 
        }
        100%{
            color:black 
        }
    }
    @keyframes floatingtext {
        0%{
            color:black 
        }
        100%{
            color: white 
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
        @media (max-width: 600px){
            width: 40vw;
            height: 25px;
        }
    }
    .floating {
        position:relative;
        width: 50px;
        height: 50px;
        animation: forwards 1000ms unhoverfloat;
        @media (max-width: 600px){
            width: 25px;
            height: 25px;
        animation: forwards 1000ms unhoverfloatphone;
        }
    }
    .floatdiv:hover .floating{
        animation: forwards 1000ms hoverfloat;
        @media (max-width: 600px){
            animation: forwards 1000ms hoverfloatphone;
        }
    }
    @keyframes hoverfloatphone {
        0%{
            left: -25vw;
        }
        100%{
            left: 0;
            // left: calc(20vw - 25px)
        }
    }
    @keyframes unhoverfloatphone {
        0%{
            left: 0;
            // left: calc(20vw - 25px)
        }
        100%{
            left: -25vw;
        }
    }
    @keyframes hoverfloat {
        0%{
            left: -17vw;
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
            left: -17vw;
        }
    }
</style>