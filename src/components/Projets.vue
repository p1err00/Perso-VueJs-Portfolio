<template>
    <div id="app">
        <splide :options="options">
            <splide-slide class="slide" v-for="projet in projets" v-bind:key="projet">
                <div class="card">
                    <div class="card-title">
                        {{projet.name}}
                        <span class="card-date">
                            {{projet.date}}
                        </span>
                    </div>
                    <div class="card-text">
                        <p class="destinataire">
                            <span class="bold">Destinataire :</span> 
                            {{projet.destinataire}}
                        </p>
                        <p class="desc">
                            {{projet.desc}}
                        </p>
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
                    "name": "aze",
                    "date": "2020",
                    "destinataire": "aze",
                    "desc": "aze aze azze azze aze aze"
                },
                {
                    "name": "qsd",
                    "date": "2020",
                    "destinataire": "qsd",
                    "desc": "qsd qsd qs dqss dqs sdqs"
                },
                {
                    "name": "wxc",
                    "date": "2020",
                    "destinataire": "wxc",
                    "desc": "wxcwxx wxc wxxc wxxc wxcwxxc"
                },
            ]
        }
    },
    components:{
        Splide,
        SplideSlide
    }
}
</script>

<style scoped>
#app{
    height: 100vh;
    margin-top: 50vh;
}
.slide{
    height: 60vh;
}
.card{
    height: 100%;
    margin-left: 20%;
    margin-right: 20%;
    padding: 30px;
    text-align: left;
    background-image: url("../assets/projets-font.jpg");
    color: white;
}
.card-title{
    display: flex;
    flex-direction: column;
    font-size: 38px;
}
.card-date{
    font-size: 20px;
}
.bold{
    font-style: oblique;
}
</style>