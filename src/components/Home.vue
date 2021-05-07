<template>
    <div id="app">
        
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
                <div class="main-button">
                    <a href="#portfolio" class="discover-button">Decouvrir</a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name:'Home',
    components:{
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
    #app{
        height: 100vh;
        font-family: initial;
        text-decoration: none;
        padding-top: 60px;
        background-color: #481c1c;
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
    @keyframes rotate{
        0%{
            filter: blur(5px);
        }
        100%{
            transform: rotate(360deg);
        }
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
    .hr2{
        border: 2px solid red;
        width: 36%;
        margin: auto;
        padding: auto;
        margin-bottom: 20px;
    }
    .hr3{
        border: 2px solid red;
        width: 40%;
        margin: auto;
        padding: auto;
        margin-bottom: 20px;
    }

    .main-button{
    margin-left: auto;
    margin-right: auto;
    text-align: center;
    margin-top: 20px;
    display: inline-block;
    text-decoration: none;
}
.discover-button{
    font-size: 30px;
    text-transform: uppercase;
    text-decoration: none;
    color: #2a2b2f;
    padding: 15px 25px;
}
.discover-button:hover{
    text-decoration: none;
    color: black;
}
.main-button::before{
    content: '';
    position: absolute;
    width: 0;
    height: 0;
    transform: translate(3%, -11%);
    background: transparent;
    border: 2px solid transparent;
    text-decoration: none;
}
.main-button:hover:before{
    animation: animate 1s linear forwards;
}
@keyframes animate{
    0%{
        width: 0;
        height: 0;
        border-top-color: #000;
        border-right-color: transparent;
        border-bottom-color: transparent;
        border-left-color: transparent;
        
    }
    50%{
        width: 200px;
        height: 0;
        border-top-color: #000;
        border-right-color: #000;
        border-bottom-color: transparent;
        border-left-color: transparent;
        
    }
    100%{
        width: 200px;
        height: 60px;
        border-top-color: #000;
        border-right-color: #000;
        border-bottom-color: transparent;
        border-left-color: transparent;
        z-index: -1;
    }
}




.main-button::after{
    content: '';
    position: absolute;
    width: 0;
    height: 0;
    transform: translate(-105%, -24%);
    background: transparent;
    border: 5px solid transparent;
    padding-bottom: 5px;
}
.main-button:hover:after{
    animation: animate2 1s linear forwards;
}
@keyframes animate2{
    0%{
        width: 0;
        height: 0;
        border-top-color: transparent;
        border-right-color: transparent;
        border-bottom-color: transparent;
        border-left-color: #000;
        
    }
    50%{
        width: 200px;
        height: 0;
        border-top-color: transparent;
        border-right-color: transparent;
        border-bottom-color: #000;
        border-left-color: #000;
        
    }
    100%{
        width: 200px;
        height: 60px;
        border-top-color: transparent;
        border-right-color: transparent;
        border-bottom-color: #000;
        border-left-color: #000;
        text-decoration: none;
        z-index: -1;
    }
}

</style>