<script setup lang="ts">
import { ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import PostList from './components/post/PostList.vue';

const message = ref('First VueJs contact');
const count = ref(0);
</script>

<template>
  <header>
    <div class="wrapper">
      <HelloWorld msg="Hello world!" />
    </div>
  </header>
  <div>
    <h1>{{ message }}</h1>
  </div>
  <h1>Outra mensagem</h1>
  <div>
    <button @click="count++">Adicionar</button>
    <h1>{{ count }}</h1>
    <button @click="count = 0">Limpar</button>
  </div>

  <div>
    <h1>Listagem de posts:</h1>
    <PostList />
  </div>
</template>

<style scoped>
header {
  line-height: 1.5;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>