<template>
    <div id="contact">
        <div class="container-contact">
                <div class="card-contact">
                    <div class="card-body">
                        <i class="far fa-envelope logo-contact"></i>
                        <h5 class="card-title">Mail</h5>


                        <div class="card-text">
                            <p class="span-mail">pierro.adrien.simon@gmail.com</p>
                        </div>
                        <div class="card-link">
                            <a href="#" class="card-link">Copier</a>
                        </div>
                    </div>
                </div>

                <div class="card-contact">
                    <div class="card-body">
                        <i class="fas fa-mobile-alt logo-contact"></i>
                        <h5 class="card-title">Phone</h5>

                        <div class="card-text">

                            <p class="span-phone">06.07.08.09.10</p>
                        </div>
                        <div class="card-link">
                            <a href="#" class="card-link">Copier</a>
                        </div>
                    </div>
                </div>

                <div class="card-contact">
                    <div class="card-body">
                        <i class="fab fa-github logo-contact"></i>
                        <h5 class="card-title">Github</h5>

                        <div class="card-text">

                            <p class="span-git">www.gitMesCouilles.com</p>
                        </div>
                        <div class="card-link">
                            <a href="#" class="card-link">Copier</a>
                        </div>
                    </div>
                </div>
            </div>
        
    </div>
</template>

<script>
export default {
    name: 'Contact'
}
</script>

<style scoped>
.footer-section{
    position: relative;
}
.container-contact{
    display: flex;
    justify-content: space-around;
    padding-top: 150px;
    background: #232427;
    padding: 100px;
    bottom: 0;
    font-family: initial;
    border-top: 15px double grey;
}
.card-contact:hover{
    animation: cardContact 1s forwards;
}
@keyframes cardContact{
    0%{
        transform: translate(0, 0);
    }
    100%{
        transform: translate(0, -20%);
    }
}
.card-contact{
    width: 18rem;
    text-align: center;
    border-radius: 15px;
    background: white;
}
.card-title{
    margin-bottom: 20px;
}

.card-text{
    border-top: 1px solid black;
    border-bottom: 1px solid grey;
    padding-top: 20px;
    padding-bottom: 18px;
}
.card-link{
    margin-top: 20px;
}
.logo-contact{
    font-size: 30px;
}
</style>