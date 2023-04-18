<template>
    <h1>Proyectos</h1>
    <div class="conten">
        <div class="all-card" v-for="repo in repos">
            <div class="card">
                <div class="card_name">
                    <span>{{ repo.name }}</span>
                </div>
                <div class="card_link">
                    <a :href="repo.url" target="_blank">Ver</a>
                </div>
                <div class="card_leng">
                    <span> Hecho en {{ repo.leng }}</span>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
import { reactive, onMounted } from 'vue';
export default {
    setup() {
        const repos = reactive([])

        onMounted(async () => {
            const resp = await fetch('https://api.github.com/users/arkeber-23/repos')
            const data = await resp.json();
            data.map((d) => repos.push({ name: d.full_name.split("/")[1], url: d.html_url, leng: d.language }))
        })

        return { repos }
    }
}
</script>

<style  scoped>
h1 {
    color: white;
    font-size: 2rem;
    font-weight: bold;
    font-style: italic;
}

.conten {
    height: 250px;
    overflow-x: scroll;
    overflow-y: scroll;
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: .5rem;
    padding: .3rem;
    box-shadow: 0 4px 30px rgba(255, 255, 255, 0.2);
    border-radius: 8px;
}


.all-card {
    border-radius: 8px;
    width: 250px;
    height: 150px;
    padding: 1rem 0;
    justify-self: center;
}

.card {
    word-break: break-all;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    background: #09304b;
    border-radius: 8px;
    padding: .3rem;
}

.card:hover {
    background: #0d5e97d3;
}

.card_name span {
    font-size: 1.1rem;
    color: white;
    font-weight: bold;

}

.card_link a {
    text-decoration: none;
    color: white;
}

.card_link a:hover {
    color: #ffffff;
    font-size: .9rem;
    font-weight: bold;
    filter: drop-shadow(0px 0px 4px rgb(25, 255, 255));
}

.card_leng span {
    padding: .5rem;
    color: white;
    font-size: 1rem;
    font-style: italic;
    font-weight: bold;
}

@media screen and (max-width:512px) {
    h1 {
        font-size: 1.2rem;
    }

    .conten {
        overflow-x: hidden;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
    }

}
</style>