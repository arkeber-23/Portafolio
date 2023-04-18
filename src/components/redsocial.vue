<template>
    <div class="red-social">
        <a href="https://www.linkedin.com/in/eber-andres-cabezas-valencia-10a0b2239/" target="_blank">
            <IconBrandLinkedin color="#1f618d" :size="48"></IconBrandLinkedin>
        </a>
        <a href="https://github.com/arkeber-23" target="_blank">
            <IconBrandGithub color="#1f618d" :size="48"></IconBrandGithub>
        </a>
        <a href="https://www.instagram.com/evercabezasvalencia/" target="_ba">
            <IconBrandInstagram color="#1f618d" :size="48"></IconBrandInstagram>
        </a>
        <a href="https://twitter.com/ever_cabezas" target="_blank">
            <IconBrandTwitter color="#1f618d" :size="48"></IconBrandTwitter>
        </a>
    </div>
</template>
<script>
import { IconBrandLinkedin } from "@tabler/icons-vue";
import { IconBrandGithub } from "@tabler/icons-vue";
import { IconBrandInstagram } from "@tabler/icons-vue";
import { IconBrandTwitter } from "@tabler/icons-vue";
export default {
    components: {
        IconBrandLinkedin,
        IconBrandGithub,
        IconBrandInstagram,
        IconBrandTwitter,
    },
};
</script>
<style scoped>
.red-social {
    box-shadow: 0 4px 30px rgba(255, 255, 255, 0.2);
    backdrop-filter: blur(4.7px);
    -webkit-backdrop-filter: blur(4.7px);
    position: fixed;
    right: 5px;
    top: 4rem;
    width: 50px;
    height: 500px;
    border-top-left-radius: 10px;
    border-bottom-left-radius: 10px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 1.5rem;
}
</style>
