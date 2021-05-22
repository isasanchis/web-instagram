<template>
    <div class="stories__container">
        <div class="profiles__stories" v-for="perfil in perfilStories" :key="perfil.nome">
            <div class="profiles__content">
                <a href="#"><img :src="perfil.img" :alt="perfil.nome" class="foto__perfil--stories"></a>
                <p>{{ perfil.nome }}</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            perfilStories: [
                {nome: 'merida', img: 'https://i.pinimg.com/originals/d1/c5/79/d1c579b41054aec85bb871dbe8af5622.jpg'},
                {nome: 'marypoppins', img: 'https://i.pinimg.com/originals/e1/ff/e5/e1ffe5d846735a360c16a744aeaebc0d.jpg'},
                {nome: 'emerald', img: 'https://i.pinimg.com/originals/51/3a/2d/513a2d4343551dc7931b286fc8c5be8b.jpg'},
                {nome: 'sleepingbeauty', img: 'https://i.pinimg.com/originals/24/98/57/249857d96526a2081447d6b51cdd5929.jpg'},
                {nome: 'lerigo', img: 'https://www.justlia.com.br/wp-content/uploads/2014/10/disney-ilustra%C3%A7%C3%B5es-retratos-hero%C3%ADnas-elsa.jpg'},
                {nome: 'mulan', img: 'https://i.pinimg.com/originals/a7/15/b6/a715b6012ceca66b435110a690e88077.jpg'},
                {nome: 'rapunzel', img: 'https://i.pinimg.com/originals/0f/10/19/0f1019505170b1946bc280dedfe7df59.jpg'},
                // {nome: 'belle', img: 'https://i.pinimg.com/originals/85/70/8e/85708efb522e2dd836954edc2d0be49e.jpg'},
            ],
        }
    },
}
</script>

<style>
/* STORIES */
.stories__container {
    background-color: #fff;
    padding: 12px;
    margin: 30px 0px;
    border: 1px solid #cbcccc;
    display: flex;
    justify-content: space-around;
    text-align: center;
    border-radius: 3px;
    margin-top: 15%;
}
.profiles__stories {
    text-overflow: ellipsis;
    white-space: nowrap; 
    overflow: hidden;
    text-align: center;
    width: 100%;
}
.profiles__content {
    margin-left: 8px;
}
.profiles__stories p {
    font-size: 12px;
    text-overflow: ellipsis;
    white-space: nowrap; 
    overflow: hidden;
    width: 100%;
}
.foto__perfil--stories {
    height: 4.5rem;
    border-radius: 50%;
    padding: 1px;
    border: 2px solid #ec4958;
}
</style>