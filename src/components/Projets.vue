<template>
    <div id="projets">
        <splide :options="options">
            <splide-slide class="slide" v-for="projet in projets" v-bind:key="projet">
                <div class="card">
                    <div class="card-header">
                        <span class="title">{{projet.name}}</span>
                        <span class="card-date">
                            {{projet.date}}
                        </span>
                        <button class="button" v-on:click="more = !more">See more</button>
                    </div>
                    <transition name="scroll">
                        <div class="card-body" v-if="more != true">
                        
                            <p class="destinataire">
                                {{projet.destinataire}}
                            </p> 
                            <p class="desc">
                                {{projet.desc}}
                            </p>
                        </div>
                    </transition>
                    <div class="card-footer">
                        <span class="key">Technologies utilisées:</span>
                        <div class="footer">
                            <span class="techno">{{projet.techno}}</span>
                        </div>
                        <div class="link">
                            <a :href='projet.link' v-if="projet.link != ''">
                                <div class="tooltip">
                                    En savoir plus
                                    <span class="tooltiptext">{{ projet.tooltip }}</span>
                                </div>
                            </a>
                            
                            <a v-else></a>
                            
                        </div>
                    </div>
                    
                </div>
            </splide-slide>
    </splide>
    </div>
</template>

<script>
import { Splide, SplideSlide } from '@splidejs/vue-splide';
import '@splidejs/splide/dist/css/themes/splide-default.min.css';
export default {
    name: 'Projets',
    data(){
        return {
            projets:[
                {
                    "name": "Ummon",
                    "date": "2020 - 2021",
                    "destinataire": "Ummon HealthTech",
                    "desc": "Ummon est un logiciel médical déstiné à assister des médecins dans la lecture d'imagerie et la pose de diagnostique. Ce logiciel doit permettre d'analyser des images de microscope afin de détécter des anomalies notamment des cancers au niveau du col de l'uterus. Le but de ce projet était de développer une interface graphique capable de communiquer avec une API ainsi que gérer et stocker des données sur un serveur dedié.",
                    "techno": ["QtCreator", "Postman", "C++"],
                    "link": "https://www.ummonhealthtech.com/ummon/",
                    "tooltip": "Ummon site officiel"
                },
                {
                    "name": "Laboratoire VR",
                    "date": "2018",
                    "destinataire": "Université de Bourgogne - Facultée de Dijon",
                    "desc": "Afin d'accompagner et de former les étudiants en pharmacologie, la facultée de Dijon à mis en place un projet en Réalité Virtuelle de simulation de laboratoire. Le but de ce projet était de former les étudiants à utiliser les différentes machines de laboratoire sans prendre le risque d'engendrer des dommages ou des erreures sur de réèlles machines physiques, mais aussi de voir la réaction des étudiants lors de problèmes aléatoires (insecte, depart de feu, alarme incendie, etc...).",
                    "techno": ["Unity","C#"],
                    "link": ""
                },
                {
                    "name": "MGame",
                    "date": "2020",
                    "destinataire": "Projet personnel",
                    "desc": "Pour pouvoir faciliter la gestion des jeux présents sur mon ordinateur, j'ai développé une application capable de gérer une liste de logiciel, de les éxécuter et de récuperer et stocker des informations sur mon ordinateur.",
                    "techno": ["QtCreator","C++"],
                    "link": "https://github.com/p1err00/MGame",
                    "tooltip": "Depot github"
                },
                {
                    "name": "Alone",
                    "date": "2017",
                    "destinataire": "Projet personnel",
                    "desc": "Ce projet, bien qu'un peu ancien, visait à ameliorer et consolider mes compétences en programmation orienté objet en mettant en place un petit jeu de survie textuel dans un terminal windows, et par la suite l'implémenter dans une application mobile.",
                    "techno": ["Eclipse","Java"],
                    "link": "https://github.com/p1err00/Alone",
                    "tooltip": "Depot github"
                },
                {
                    "name": "Todolist",
                    "date": "2020",
                    "destinataire": "Projet personnel",
                    "desc": "Une todolist en Javascript communiquant avec une API developpé sous Flask",
                    "techno": ["Javascript", "Python", "Flask"],
                    "link": "https://github.com/p1err00/Todolist",
                    "tooltip": "Depot github"
                }
            ],
            more : true
        }
    },
    components:{
        Splide,
        SplideSlide
    },
    methods:{
        
    }
}
</script>

<style scoped>
#projets{
    height: 100vh;
    margin-top: 20vh;
    scroll-behavior: smooth;
}
a{
    color: #a05151;
    font-weight: bold;
  font-size: 26px;
}
.slide{
    height: 70vh;
}
.card{
    margin-left: 20%;
    margin-right: 20%;
    padding: 30px;
    text-align: left;
    background: rgba(83, 83, 83, 0);
    color: rgb(27, 25, 25);
    font-weight: bold;
    border: none;
    height: 100%;
}
.card-header{
    display: flex;
    flex-direction: column;
    padding-bottom: 5px;
    text-align: center;
    align-items: center;
    background-color: #ffb05c;
    color: #481c1c;
    border-top-left-radius: 15px;
    border-top-right-radius: 15px;;
}
.title{
    font-size: 48px;
    font-family: 'Merriweather', serif;
}
.card-date{
    font-size: 20px;
}
.button{
    background: none;
    color: grey;
    width: 150px;
    height: 40px;
}
.card-body{
    height: 100%;
}
.destinataire{
    font-size: 30px;
    margin-left: 20px;
    font-family: 'Arimo', sans-serif;
}
.desc{
    font-size: 18px;
    line-height: 33px;
    text-align: center;
    margin-left: 5%;
    margin-right: 5%;
}
.card-footer{
    border: none;
    text-align: center;
    font-family: 'Merriweather', serif;
    font-size: 24px;
    margin-top: 20px;
    background-color: #ffb05c;
    color: #481c1c;
    border-bottom-left-radius: 10px;
    border-bottom-right-radius: 10px;
}
.key{
    font-size: 22px;
}
.footer{
    display:flex;
    flex-direction: column;
}
.techno{
    padding-top: 20px;
}
.link{
    padding-top: 10px;
}
.scroll-enter-active {
  animation: scroll-in 1s;
}
.scroll-leave-active {
  animation: scroll-in 1s reverse;
}
@keyframes scroll-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
.tooltip {
  position: relative;
  display: inline-block;
  border-bottom: 1px dotted black;
  opacity: 1;
  font-family: 'Arimo', sans-serif;
  font-size: 20px;
  border: none;
}
.tooltip .tooltiptext {
  visibility: hidden;
  width: 120px;
  background-color: black;
  color: #fff;
  text-align: center;
  border-radius: 6px;
  padding: 5px 0;
  margin-left: 20px;
  /* Position the tooltip */
  position: absolute;
  z-index: 1;
}
.tooltip:hover .tooltiptext {
  visibility: visible;
  animation: display .3s;
}
@keyframes display {
    0%{
        opacity: 0;
    }
    100%{
        opacity: 1;
    }
}
</style>