<template>
  <div class="main">
    <About></About>
    <Skils></Skils>
  </div>
  <Project></Project>
  <Redsocial></Redsocial>
</template>

<script>
import About from './components/about.vue';
import Project from './components/project.vue';
import Redsocial from './components/redsocial.vue';
import Skils from './components/skils.vue';
export default {
  components: {
    About,
    Project,
    Redsocial,
    Skils
  },
}
</script>
<style scoped>
.main {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 2rem;
}

@media screen and (max-width:512px) {
  .main {
    padding: .1rem;
  }
}
</style>