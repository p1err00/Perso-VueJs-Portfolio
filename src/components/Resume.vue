<template>
    <div id="resume">
        <div class="title-loader">
            <h2>Resume...</h2>
        </div>

            <div class="resume-content">
                <div class="imgDiv">
                    <img src="../assets/Aaa.jpg" />
                </div>
                    
                <p class="text">
                    <span class="acollade">{</span> Féru d'informatique depuis toujours, je met au profit des autres mes compétences dans ce domaine.
                    Que cela soit du développement web ou logiciel, frontend ou backend, ma curiosité et mon investissement me permettent 
                    de mener à bien chacun de mes projets. <span class="acollade">}</span>
                </p>

                
            </div>
            <div class="formation">
                <div class="card" v-for="formation in formations.slice().reverse()" v-bind:key="formation">
                    <div class="card-title">
                        <img src="../assets/degree.png" class="img-degree"/>
                        <span>
                            {{formation.name}}
                        </span>   
                        
                        <span class="border-down"></span>
                        <span class="card-date">
                            {{formation.date}}
                        </span>
                    </div>
                    <div class="card-text">
                        <p class="card-school">
                            {{formation.school}}
                        </p>
                        <p class="card-city">
                            {{formation.city}}
                            -
                            {{formation.cp}}
                        </p>    
                    </div>
                </div>
            </div>
    </div>
</template>
<script>
export default {
    name: 'Resume',
    components:{

    },
    data(){
        return{
            formations:[
                {
                    "name": "Licence DevOps",
                    "date": "2020 - 2021",
                    "school": "Pole formation 58-98",
                    "city": "Auxerre",
                    "cp" : "89000"
                },
                {
                    "name": "BTS SNIR",
                    "date": "2017 - 2020",
                    "school": "Lycée St Joseph-La Salle",
                    "city": "Dijon",
                    "cp" : "21000"
                },
                {
                    "name": "Bac STI2D",
                    "date": "2015 - 2017",
                    "school": "Lycée Gustave Eiffel",
                    "city": "Dijon",
                    "cp" : "21000"
                }
            ]
        }
    }
}
</script>
<style scoped>
    #resume{
        height: 120vh;
        width: 100%;
        padding-top: 100px;
        background: #fff;
        background-image: linear-gradient(#481c1c 10px, #fff 1%);
        font-family: consolas;
        align-items: center;
        scroll-behavior: smooth;
    }
    .resume-content{
        display: flex;
        justify-content: space-around;
        align-items: center;
        margin: 0 6% 0 5%;
        
    }
    .imgDiv{
        margin-right: 20px;
        padding-right: 50px;
    }
    img{
        border-radius: 14px;
        width: 100%;
    }
    .title-loader{
        position: absolute;
        display: flex;
        justify-content: center;
        width: 100%;
    }
    .title-loader:after{
        content: '';
        position: revert;
        top:0;
        right: 0;
        width: 4px;
        height: 70px;
        animation: blinkCursor 0.3s steps(3) infinite;
        background: black;
    }
    .title-loader h2{
        position: relative;
        text-transform: uppercase;
        overflow: hidden;
        animation: typing 5s steps(9) infinite;
    }
    
    h2{
        font-size: 4em;
        margin-bottom: 40px;
        letter-spacing: 5px;
        color: rgb(69, 178, 221);
    }
    
    @keyframes blinkCursor {
        0%, 75%{
            opacity: 1;
        }
        76%, 100%{
            opacity: 0;
        }
    }
    
    @keyframes typing {
        0%,90%,100%{
            width: 0;
            
        }
        30%, 60%{
            width: 350px;
        }
    }
    .text{
        font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
        font-size: 30px;
        line-height: 65px;
        border-left: 2px solid red;
        color: #000;
        letter-spacing: 3px;
        margin-top: 80px;
    }
    .acollade{
        font-size: 58px;
        color: rgb(228, 104, 228);
    }
    .formation{
        width: 100%;
        margin-top: 60px;
        display: flex;
        justify-content: space-between;
        padding-left: 10%;
        padding-right: 10%;
    }
    .card{
        
        padding-left: 15px;
        padding-top:20px;
        margin:10px;
        background: #ffb05c;
        color: #481c1c;
        border-radius: 15px;
        overflow: hidden;
        transition: all .2s;
        z-index: 1;
    }
    .card .card-title{
        height: 300px;
        width: 100%;
    }
    .card-title{
        width: 100%;
        display: flex;
        flex-direction: column;
        font-size: 48px;
        text-align: center;
    }
    .img-degree{
        width: 150px;
        height: 150px;
        margin-top: 0;
        transition: all .2s;
        margin: auto;
    }
    .card-date{
        margin-top: 10px;
        font-size: 14px;
    }
    .card-text{
        margin-top:10px;
    }
    .card-school{
        font-size:26px;
    }
    .card-city{
        margin-left: 10px;
        font-size: 20px;
    }
    .border-down{
        border: 4px solid #A75102;
        margin-right: 20%;
        margin-left: 20%;
    }
    .card:hover img{
        width: 50px;
        height: 50px;
    }
    @media (max-width: 1900px){
        #resume{
            height: 200vh;
        }
        .img-degree{
            transition: none;
        }
    }
    @media(max-width: 1080px){
        #resume{
            height: 200vh;
        }
        img{
            display: none;
        }
        .text{
            font-size: 2.6vw;
            padding-left: 20px;
        }
        .card{
            height: 420px;
        }
        .card .card-title{
            height: 150px;
        }
        .card-title{
            font-size: 28px;
        }
        .card-text{
            margin-top:0;
        }
    }
    @media (max-width: 620px) {
        #resume{
            height: 200vh;
        }
        .resume-content{
            display: flex;
            flex-direction: column;
        }
        .text{
            font-size: 4.6vw;
            border: none;
            text-align: center;
            line-height: 40px;
        }
        img{
            display: none;
        }
        .formation{
            display: flex;
            flex-direction: column;
        }
        .card{
            height: 200px;
            width: 100%;
        }
        .card-title{
            font-size: 25px;
        }

    }
    @media (max-width: 340px){
        #resume{
            height: 300vh;
        }
    }
</style>