<script setup lang="ts">

type PostListType = {
  id: number;
  marca: string;
  modelo: string;
  ano: number;
  cor: string;
}

const listPosts: PostListType[] = [
  {
    "id": 1,
    "marca": "Toyota",
    "modelo": "Corolla",
    "ano": 2024,
    "cor": "Prata"
  },
  {
    "id": 2,
    "marca": "Honda",
    "modelo": "Civic",
    "ano": 2023,
    "cor": "Preto"
  },
  {
    "id": 3,
    "marca": "Ford",
    "modelo": "Mustang",
    "ano": 2025,
    "cor": "Vermelho"
  }
];
</script>

<template>
  <div class="post">
    <ul>
      <li v-for="post in listPosts" :key="post.id">{{ post.marca }}</li>
    </ul>
  </div>
</template>


<style scoped>
ul {
  list-style: none;
}
</style>