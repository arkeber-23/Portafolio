<template>
    <div class="about">
        <div class="about-container">
            <img class="about-container-img" src="../assets/me.png" alt="img">
        </div>
        <div class="about-name">
            <h4> Eber Andrés Cabezas Valencia</h4>
            <span>Desarrollador de Software</span>
        </div>
        <div class="msg">
            <p>Desarrollador de software, con más de 2 años de experiencia enfocado al backend, apasionado de la tecnología
                en general y amante al aprendizaje autónomo. </p>
        </div>
    </div>
</template>

<script>
export default {
    setup() {


        return {}
    }
}
</script>

<style scoped>
.about {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.about-container {
    width: 350px;
    height: auto;
    overflow: hidden;
    filter: drop-shadow(0px 0px 8px rgba(255, 255, 255, 0.5));
}

.about-container-img {
    width: inherit;
    object-fit: contain;
}

.about-name {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    line-height: 4px;
    color: white;
    font-size: 1.5rem;
}

.about-name h4 {
    font-weight: bold;
}

.about-name span {
    font-size: 1rem;
}

.msg {
    margin-top: 2rem;
    padding: 0 1rem;
    text-align: justify;
    font-size: 1.2rem;
    color: white;
    width: 550px;
}


@media screen and (max-width:512px) {
    .about-container {
        width: 220px;
    }

    .about-container-img {
        width: inherit;
        object-fit: contain;
    }

    .about-name {
        font-size: .8rem;
    }

    .about-name span {
        font-size: .5rem;
    }

    .msg {
        width: 100%;
        font-size: 1rem;
    }

}
</style>