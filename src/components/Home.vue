<template>
    <div id="home">
        
        <img src="../assets/fontCodeRight.png" class="cornerImgRight" />
        <img src="../assets/fontCodeLeft.png" class="cornerImgLeft" />

        <div class="content">

            <div class="div-title">
                <h1><span class="main-title">{{ name }}</span></h1>
                <hr class="hr" />
            </div>
            <div class="content-resume">
                <div class="div-resume">

                    <span class="resume-title">{{ desc }}</span>
                </div>
                <HomeButton/>
            </div>
        </div>
    </div>
</template>

<script>
import HomeButton from './HomeButton.vue'
export default {
    name:'Home',
    components:{
        HomeButton
    },
    data(){
        return{
            name: "SIMON Pierre-Adrien",
            desc: '*.* Convertisseur algorithmiste en sciences technologiques 2.0 *.*'
        }
    }
}
</script>

<style scoped>
@media(max-width: 2850px) {
    

    #home{
        height: 100vh;
        font-family: initial;
        text-decoration: none;
        padding-top: 60px;
        background-color: #481c1c;
        scroll-behavior: smooth;
    }
    .cornerImgLeft{
        bottom: 5px;
        left: 30px;
        position: absolute;
        width: 50%;
        filter: blur(4px);
     }
    .cornerImgRight{
        top: 30px;
        position: absolute;
        width: 50%;
        right: 0;
        filter: blur(4px);
    }

    .content{
        padding-top: 285px;
    }
    .main-title{
        font-size: 5vw;
        font-weight: 800;
        letter-spacing: 8px;
        margin-bottom: 30px;
        position: relative;
        animation: text 3s 1;
        animation-fill-mode: forwards;
        overflow: hidden;
        transform: translate(50px, 50px);
    }
    @keyframes text{
        0%{
            color: #481c1c;
            margin-bottom: -100px;
            filter: blur(5px);
            z-index: 2;
        }
        30%{
            letter-spacing: 20px;
            margin-bottom: -100px;
            z-index: 2;
        }
        85%{
            letter-spacing: 8px;
            margin-bottom: -100px;
            z-index: 2;
        }
    }
    .resume-title{
        font-size: 1.6vw;
        padding: 15px;
    }
    .content-resume{
        animation: azerty 3s forwards;
    }
    @keyframes azerty{
        0%{
            filter: blur(10px);
        }
        100%{
            filter: blur(0);
        }
    }

    .div-resume .resume-title{
        text-transform: uppercase;
        display: block;
        overflow: hidden;
    }

    .resume-title{
        font-size: 18px;
        padding: 15px;
        animation: textResume 3s 1;
        animation-fill-mode: forwards;
    }
    @keyframes textResume{
        
    }
    .hr{
        border: 2px solid red;
        width: 60%;
        margin: auto;
        padding: auto;
        margin-bottom: 20px;
    }
    
}
    @media(max-width: 1080px){
        .content{
            padding-top: 200px;
        }

    }
    @media (max-width: 650px) {
        .content{
            padding-top: 200px;
        }
        .hr{
            position: absolute;
            margin-left: 20%;
        }
    }
    @media (max-width: 320px) {
        .content {
           padding-top: 160px;
        }
        .div-title{
            max-width: 100%;
            max-height: 60px;
            border: none;
        }
        .main-title{ 
            text-align: center;
            max-width: 100%;
            max-height: 50px;
            overflow: hidden;
            animation: text 3s 1;
            animation-fill-mode: forwards;
        }
        .hr{
            position: absolute;
            margin-left: 20%;
        }
        @keyframes text{
        0%{
            color: #481c1c;
            filter: blur(5px);
        }
        30%{
            letter-spacing: 20px;

        }
        85%{
            letter-spacing: 8px;

        }
    }
        .resume-title{
            margin-top: 8px;
            font-size: 4.6vw;
            text-align: center;
        }
    }


</style>