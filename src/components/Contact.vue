<template>
    <div id="contact">
        <h1>Contact</h1>
        <div class="content">
            <div class="b">
                <button><a href="./documents/CurriculumVitae.pdf" download="">CV</a></button>
            </div>
            <div class="b">
                <button class="github"><a href="https://github.com/p1err00/"><i class="fab fa-github"></i></a></button>
            </div>
            <div class="b">
                <button class="linkedin"><a href="https://www.linkedin.com/in/pierre-adrien-simon-6197a719a/"><i class="fab fa-linkedin-in"></i></a></button>
            </div>
        </div>
        <div class="infos">
            <a href="mailto:pierro.adrien.simon@gmail.com" class="key">{{ email }}</a>
            <p class="key">{{ tel }}</p>
        </div>
    </div>
</template>

<script>
export default {
    name: "Contact",
    data() {
        return {
            email: "pierro.adrien.simon@gmail.com",
            tel: "+33 (0)6.95.14.00.99",
            linkedin: "azeazeaze",
            github: "azeazeazze"
        }
    },
    methods:{
        githubRedirect(){
            document.location.href="https://github.com/p1err00/";
        }
    }
}
</script>
<style scoped>
    #contact{
        height: 50vh;;
        background: #481c1c;
        padding-top: 40px;
    }
    h1{
        font-size: 58px;
    }
    .content{
        display: flex;
        flex-direction: row;
        justify-content: space-evenly;
        align-items: center;
        margin: auto;
        margin-top: 40px;
        height: 100px;
    }
    .b{
        width: 100%;
    }
    button{
        border-radius: 50%;
        width: 60px;
        height: 60px;
        margin-top: 20px;
        margin-bottom: 20px;
        background: transparent;
        font-size: 24px;
        color:rgb(139, 96, 16);
        transition: .3s;
    }
    button:hover{
        width: 90px;
        height: 90px;
    }
    .key{
        font-size: 28px;
        margin-top: 20px;
        font-weight: bold;
    }
    a{
        color: rgb(197, 124, 39);
    }
    a:hover{
        text-decoration: none;
        color: #a05151;
    }

@media(max-width: 1900px){
    #contact{
        height: 80vh;
    }
}

@media(max-width: 1080px){
    #contact{
        height: 80vh;
    }
}

@media(max-width: 650px){
    #contact{
        height: 75vh;
    }
}
@media(max-width: 430px){
    #contact{
        height: 75vh;
    }
    .key{
        font-size: 20px;
    }
}
</style> 