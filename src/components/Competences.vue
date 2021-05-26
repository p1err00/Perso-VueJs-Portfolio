<template>
    <div id="app">
        <div class="title">
            {{ title }}
        </div>
        <div class="desc">
            {{ desc }}
        </div> 
        <div class="content">
            <div class="content-left">
            <div class="competences line" v-for="competence in competences" v-bind:key="competence">
                <div class="paragraphe">
                    <div class="par-title">{{ competence.title }}</div>
                    <br />
                    <div class="par-resume">{{ competence.desc }}</div>
                </div>    
            </div>
        </div>
        <div class="separator">
                
            </div>
        <div class="content-right">
            <div class="competences line" v-for="aptitude in aptitudes" v-bind:key="aptitude">
                <div class="paragraphe">
                    <div class="par-title">
                        {{ aptitude.title }}
                    </div>
                    <div class="par-resume">
                        <span class="langage">{{ aptitude.langage }}</span>
                        <br/>
                        <span class="framework">{{ aptitude.framework }}</span>
                    </div>
                </div>
                
            </div>
        </div>
        </div>
    </div>
    
</template>

<script>
export default {
    name: 'Competences',
    data() {
        return {
            title: "Services",
            desc: "Mes competences et aptitudes",
            competences:[
                {"title" : "Gestion de projet", 
                "desc" : "De la réfléxion à la conception, je saurais mettre en place les moyens adequates pour la réalisation de chaque projet"},
                {"title" : "Developpement",
                "desc" : "Parmis tous les choix existants, je saurais selectionner les outils appropriés pour mener à bien mon developpement"},
                {"title" : "Formation",
                "desc" : "Dans un corps de métier en constante évolution, je saurais me former aux nouvelles méthodes et technologies qui s'y ajoutent"}
            ],
            aptitudes:[
               {"title" : "Developpement logiciel",
               "langage" : "C++, Java",
               "framework" : "QtCreacor, Eclipse"},
               {"title" : "Developpement Web",
               "langage" : "HTML, JavaScript, PHP",
               "framework" : "VueJs, Symfony, NodeJs"},
            ]
        }
    },
        methods:{

        }
}
</script>

<style scoped>
    #app{
        height: 130vh;
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        padding: 0 10% 10% 10%;
        background: rgba(236, 236, 236, 0.445);
        color: grey;
    }
    .title{
        font-size: 68px;
        border-bottom: 3px solid red;
    }
    .desc{
        margin-top: 30px;
        font-size: 28px;
    }
    .content{
        margin-top: 40px;
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        width: 100%;
    }
    .separator{
        border: 4px solid rgb(109, 109, 109);
        height: 100%;
    }
    .competences .paragraphe{
       width: 500px;
    }
    .line{
        box-shadow: 0 2px 20px #000;
        transition: .5s;
        background: linear-gradient(-45deg, transparent 40%, #ddd 50%, transparent 40%);
        background-size: 400% 400%;
        background-color: rgba(255,255,255,0.3);
        background-position: 90% 90%;
        animation: animate 2s ease infinite;
    }
    .line .paragraphe{
        background-size: auto 110%;
        background-position: center;
        transition: 2s;
    }

    @keyframes animate{
        to{
            background-position: 25% 25%;
        }
    }
    .paragraphe{
        margin-top: 20px;
        padding: 20px;
        width: 450px;
        border-bottom: 2px solid grey;
    }
    .par-title{
        font-size: 38px;
        width: 70%;
        margin: auto;
        border-bottom: 1px solid rgb(39, 39, 39);
        color: rgb(80, 80, 80);
    }
    .par-resume{
        font-size: 20px;
        filter: blur(5px);
        transition: all .3s;
        font-weight: bold;
    }
    .par-resume:hover{
        filter: blur(0);
    }
    .content-right{
        margin: auto;
    }
    .content-left{
        margin: auto;
    }


    @media (max-width: 1080px){
        #app{
            height: 100%;
        }
        .content{
            display: flex;
            flex-direction: column;
        }
        .competences .paragraphe{
            width: 200px;
        }
        .par-title{
            font-size: 25px;
            width: 100%;
        }
        .separator{
            margin-top: 20px;
        }
        .par-resume{
            font-size: 15px;
            filter: blur(0);
        }
    }
</style>