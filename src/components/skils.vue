<template>
    <div class="skils">

        <div class="skils-g">
            <h4>Frontend</h4>
            <img src="../assets/icons/bootstrap.svg" alt="">
            <img src="../assets/icons/css.svg" alt="">
            <img src="../assets/icons/html.svg" alt="">
            <img src="../assets/icons/vue.svg" alt="">
            <img src="../assets/icons/tailwind-css.svg" alt="">
            <img src="../assets/icons/js.svg" alt="">
        </div>
        <div class="skils-g">
            <h4>Backend</h4>
            <img src="../assets/icons/jav.svg" alt="">
            <img src="../assets/icons/spring.svg" alt="">
            <img src="../assets/icons/php.svg" alt="">
        </div>

        <div class="skils-g">
            <h4>Otras Tecnolog&iacute;as</h4>
            <img src="../assets/icons/git.svg" alt="">
            <img src="../assets/icons/linux.svg" alt="">
            <img src="../assets/icons/mysql.svg" alt="">
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
.skils {
    width: inherit;
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    text-align: center;
    gap: 1rem;
}


.skils-g {
    display: block
}

.skils-g h4 {
    color: white;
    font-size: 1.2rem;
    font-style: italic;
}

img {
    width: 40px;
    margin: 0 2px;
    cursor: pointer;
}

@media screen and (max-width:512px) {
    .skils {
        width: inherit;
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 1rem;
    }
}
</style>