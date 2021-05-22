<template>
    <aside class="suggestion__container">
        <div class="my__profile-suggestion">
            <span class="my__user-suggestion">
                <img class="my__photo-suggestion" src="./img/perfil-instagram.jpg" alt="foto de perfil">
                <span>
                    <a href="#">isasanchis</a>
                    <p>Isabella Sanchis</p>
                </span>
            </span>
            <button class="btn__suggestion">Mudar</button>
        </div>
        
        <div class="suggestion__text">
            <p>Sugestões para você</p>
            <button class="btn__suggestion--text">Ver tudo</button>
        </div>

        <div class="users__suggestions" v-for="user in userSugestoes" :key="user.nome">
            <span class="users__container--suggestion">
                <a href="#"><img :src="user.img" :alt="user.nome" class="users__photo"></a>
                <p>{{ user.nome }}</p>
            </span>
                <button class="btn__suggestion">Seguir</button>
        </div>

        <p class="about">Sobre • Ajuda • Imprensa • API • Carreiras • Privacidade • Termos • Localizações • Principais contas • Hashtags • Idioma</p>
        <p class="about">© 2021 INSTAGRAM DO FACEBOOK</p>
    </aside>
</template>

<script>
export default {
    data() {
        return {
            userSugestoes: [
                {nome: 'lanadelrey', img: 'https://yt3.ggpht.com/ytc/AAUvwngL1-yEH9uO1VP3CfBY-qdnTfxaERGvmU5qH9tkUA=s900-c-k-c0x00ffffff-no-rj'},
                {nome: 'theweeknd', img: 'https://conteudo.imguol.com.br/c/entretenimento/cd/2019/11/29/theweeknd-1575032257568_v2_450x450.png'},
                {nome: 'shawnmendes', img: 'https://studiosol-a.akamaihd.net/uploadfile/letras/fotos/1/7/d/9/17d9503ff91fb415b7b9cab8ecbb543e.jpg'},
                {nome: 'avrillavigne', img: 'https://pbs.twimg.com/media/EqrBNf9XYAcPsqy.jpg'},
                {nome: 'netflix', img: 'https://imagens.canaltech.com.br/empresas/670.400.jpg'}
            ]
        }
    }
}
</script>

<style>
.suggestion__container{
    padding: 20px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 25%;
    height: 470px;
    margin-top: 6%;
}
.my__profile-suggestion {
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.my__user-suggestion {
    display: flex;
    align-items: center;
    margin-bottom: 10px;
}
.my__photo-suggestion {
    height: 4.2rem;
    border-radius: 50%;
    margin-right: 15px;
}
.my__user-suggestion a{
    color: black;
    font-weight: 500;
}
.my__user-suggestion p{
    color: rgb(158, 154, 154);
}
.btn__suggestion {
    background: none;
    border: none;
    font-weight: 500;
    font-size: 12px;
    color: #38d3e7;
    cursor: pointer;
}

.suggestion__text {
    display: flex;
    justify-content: space-between;
    color: rgb(158, 154, 154);
    font-weight: 500;
    margin-bottom: 8px;
}
.btn__suggestion--text {
    background: none;
    border: none;
    font-weight: 500;
    font-size: 12px;
    color: black;
    cursor: pointer;
}

/* SUGESTÃO - PERFIS */
.users__suggestions {
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-weight: 500;
}

.users__container--suggestion {
    display: flex;
    align-items: center;
}

.users__photo {
    height: 2.7rem;
    border-radius: 50%;
    padding: 1px;
    border: 2px solid #ec4958;
    margin-right: 10px;
}
.about {
    margin-top: 10px;
    color: rgb(209, 209, 209);
    font-size: 11px;
    font-weight: 500;
    width: 100%;
}

</style>