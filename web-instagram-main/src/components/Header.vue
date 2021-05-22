<template>
    <header class="header">
        <div class="header__container--logo">
            <img class="logo__insta" src="./img/instagram-logo.png" alt="Logo Instagram">
        </div>
        <div class="search__input">
            <input type="text" placeholder="Pesquisar">
        </div>

        <div class="icons__header--container">
            <a href="#"><img class="icons__header" src="./img/house.png" alt="Home"></a>
            <a href="#"><img class="icons__header" src="./img/messenger.png" alt="Messenger"></a>
            <a href="#"><img class="icons__header" src="./img/compass.png" alt="Descubra"></a>
            <a href="#"><img class="icons__header" src="./img/heart.png" alt="Likes"></a>
            <a href="#"><img class="foto-perfil" src="./img/perfil-instagram.jpg" alt="Foto de Perfil"></a>
        </div>
    </header>
</template>

<script>
export default {
    
}
</script>

<style scoped>
.header {
    background-color: #fff;
    border-bottom: 1px solid #cbcccc;
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    padding: 0.4%;
    position: fixed;
    width: 100%;
}
.logo__insta {
    height: 2.1rem;
    margin-top: 10px;
    margin-bottom: -1px;
}
.search__input input {
    font-weight: 300;
    text-align: center;
    border: 1px solid #cbcccc;
    border-radius: 2px;
    padding: 3px;
    background-color: #f3f3f3;
    width: 125%;
}
.search__input input:focus {
    outline: none;
}
.icons__header {
    height: 1.6rem;
    margin-right: 23px;
}
.foto-perfil {
    height: 1.6rem;
    border-radius: 50%;
}
</style>