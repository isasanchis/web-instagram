<template>
    <div class="feed">
        <div class="content__container">
            
            <Stories />

            <div class="feed__container" v-for="feed in feeds" :key="feed.nomeUsuario"> 
                <div class="feed__user--container">
                    <div class="feed__user--content">
                        <a href="#"><img class="users__photo" :src="feed.fotoUsuario" alt="Foto do usuário"></a>
                        <a href="#" class="feed__user--name">{{ feed.nomeUsuario }}</a>
                    </div>
                    <a href="#"><p class="feed__dots">•••</p></a>
                </div>

                <span class="photo__feed--posted"><img :src="feed.fotoPostada" alt="Foto do feed" height="800" width="550"></span>

                <div class="icons__container--feed">
                    <span>
                        <a href="#"><img class="icons__feed--post" src="./img/heart.png" alt="Ícone de likes"></a>
                        <a href="#"><img class="icons__feed--post" src="./img/comment.png" alt="Ícone de comentário"></a>
                        <a href="#"><img class="icons__feed--post" src="./img/send.png" alt="Ícone de enviar"></a>
                    </span>
                    <a href="#"><img class="icons__feed--post" src="./img/bookmark.png" alt="Ícone de bookmark"></a>
                </div>
                    
                <div class="likes__posts">
                    <a href="#"><img class="icon__comment--post" src="https://i.pinimg.com/originals/a7/15/b6/a715b6012ceca66b435110a690e88077.jpg" alt="Ícone de comentário"></a>
                    <p>Curtido por <a href="#" class="users__liked--post">mulan</a> e <a href="#" class="users__liked--post">outras {{feed.pessoasCurtiram}} pessoas</a></p>
                </div>

                <span class="texts__posts">
                    <p><a href="#" class="users__liked--post">{{ feed.nomeUsuario }}</a> {{ feed.legendaFoto }} <a href="#"><span class="hashtags__posts">{{ feed.hashtag }}</span></a></p>
                    <p class="time__posted">Há {{ feed.time }} horas</p>
                </span>

                <hr>

                <span class="comments__space">
                    <a href="#"><img class="icon__happy" src="./img/happiness.png" alt="Ícone de feliz"></a>
                    <input type="text" placeholder="Adicione um comentário...">
                    <button>Publicar</button>
                </span>
            </div>
        </div>

        <Suggestions />

    </div>
</template>

<script>
import Stories from './Stories.vue'
import Suggestions from './Suggestions.vue'

export default {
    components: { Stories, Suggestions },
    props: ['perfilStories', 'userSugestoes'],
    data() {
        return {
            feeds: [
                    {fotoUsuario: 'https://www.justlia.com.br/wp-content/uploads/2014/10/disney-ilustra%C3%A7%C3%B5es-retratos-hero%C3%ADnas-elsa.jpg', nomeUsuario: 'lerigo', fotoPostada: 'https://i.pinimg.com/originals/0f/c9/bb/0fc9bbdb4a66a423f7efa2ecbd592211.jpg', pessoasCurtiram: '580', legendaFoto: 'Curtindo um dia de neve', hashtag: '#snow', time: '2'},
                    {fotoUsuario: 'https://i.pinimg.com/originals/24/98/57/249857d96526a2081447d6b51cdd5929.jpg', nomeUsuario: 'sleepingbeauty', fotoPostada: 'https://static.zerochan.net/Aurora.%28Sleeping.Beauty%29.full.3261280.jpg', pessoasCurtiram: '102', legendaFoto: 'Partiu tirar um cochilo!', hashtag: '#sono', time: '4'},
                    {fotoUsuario: 'https://i.pinimg.com/originals/0f/10/19/0f1019505170b1946bc280dedfe7df59.jpg', nomeUsuario: 'rapunzel', pessoasCurtiram: '47', fotoPostada: 'https://p4.wallpaperbetter.com/wallpaper/916/332/975/rapunzel-cartoon-walt-disney-tangled-wallpaper-preview.jpg', legendaFoto: 'Passando óleo de coco no cabelo <3', time: '5'},
            ],
        }
    }
}

</script>

<style>
/* ESTILO DA PÁGINA GERAL */
.feed {
    display: flex;
    justify-content: center;
    align-items: flex-start;
}

/* PARTE DE CIMA - CONTEÚDO DO USUÁRIO QUE POSTOU */
.feed__container {
    display: block;
    background:#fff;
    padding: 12px;
    border: 1px solid #cbcccc;
    border-radius: 3px;
    margin-bottom: 20px;
}

.feed__user--container {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.feed__user--content {
    display: flex;
    align-items: center;
}

.feed__user--name {
    color: black;
    font-weight: 600;
    margin-bottom: 4px;
}

.feed__dots {
    color: black;
    font-weight: 500;
    font-size: 14px;
}

/* FOTO POSTADA */

.photo__feed--posted {
    display: block;
    margin-top: 5px;
    margin-bottom: 3px;
    margin-left: -12px;
    margin-right: -12px;
}

/* PARTE DE BAIXO - LEGENDA DA FOTO, LIKES E COMENTÁRIOS */
.icons__container--feed {
    display: flex;
    justify-content: space-between;
}

.icons__feed--post {
    height: 1.6rem;
    margin-right: 13px;
    margin-top: 6px;
}

.likes__posts {
    margin: 8px 0;
    display: flex;
    align-items: center;
}

.icon__comment--post {
    height: 1.5rem;
    border-radius: 50%;
    margin-right: 5px;
}

.users__liked--post {
    color: black;
    font-weight: 500;
}

.hashtags__posts {
    color: rgb(48, 48, 240);
}

.time__posted {
    color: rgb(158, 154, 154);
    font-size: 10px;
    text-transform: uppercase;
    margin: 6px 0;
}

.comments__space {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 10px;
}

.icon__happy {
    height: 1.6rem;
}

.comments__space input{
    border: none;
    width: 100%;
    outline: none;
    margin-left: 10px;
}
.comments__space button{
    border: none;
    background: none;
    font-weight: 500;
    color: #38d3e7;
    cursor: pointer;
}

</style>