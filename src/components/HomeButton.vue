<template>
    <div>
        <a href="#resume">
            <span></span>
            <span></span>
            <span></span>
            <span></span>
            Decouvrir
        </a>
    </div>
</template>
<script>
export default {
    
}
</script>
<style scoped>
    div{
        scroll-behavior: smooth;
    }
    a{
        position: relative;
        display: inline-block;
        padding: 15px 30px;
        text-transform: uppercase;
        text-decoration: none;
        font-size: 24px;
        overflow: hidden;
        transition: .2s;
        color: #f8ca99;
    }
    a:hover{
        color: #57b617;
        background: #812d2d;
        box-shadow:0 0 10px #812d2d, 0 0 40px #812d2d, 0 0 80px #812d2d;
    }
    a span{
        position: absolute;
        display: block;
    }
    a span:nth-child(1){
        top: 0;
        left: -100%;
        width: 100%;
        height: 2px;
        background: linear-gradient(90deg, transparent, #000000);
    }
    a:hover span:nth-child(1){
        left: 100%;
        transition: 1s;
    }
    a span:nth-child(3){
        bottom: 0;
        right: -100%;
        width: 100%;
        height: 2px;
        background: linear-gradient(270deg, transparent, #000000);
    }
    a:hover span:nth-child(3){
        right: 100%;
        transition: 1s;
        transition-delay: .5s;
    }
    a span:nth-child(2){
        top: -100%;
        right: 0;
        width: 2px;
        height: 100%;
        background: linear-gradient(180deg, transparent, #000000);
    }
    a:hover span:nth-child(2){
        top: 100%;
        transition: 1s;
        transition-delay: .25s;
    }
    a span:nth-child(4){
        bottom: -100%;
        left: 0;
        width: 2px;
        height: 100%;
        background: linear-gradient(360deg, transparent, #000000);
    }
    a:hover span:nth-child(4){
        bottom: 100%;
        transition: 1s;
        transition-delay: .75s;
    }
    
</style>