<script setup>
import { ref } from 'vue'
import ExpandBox from './components/ExpandBox.vue';
import Card from './components/Card.vue';
import CardFull from './components/CardFull.vue'

  const caixas = [
    {id: 1, title: 'caixa 1'},
    {id: 2, title: 'caixa 2', qtde: 20},
    {id: 3, title: 'caixa 3', content: 'Conteúdo secreto da caixa 3'},
    {id: 4, title: 'caixa 4', content: 'Nubank', qtde: 5}
  ];

  const titulo = ref('Título');
  const qtde = ref(0);

</script>

<template>
  <h1>Slots</h1>

  <CardFull>
    Função: professor
    <template #header> 
      <h1>Eduardo da Silva Sauro</h1>
    </template>
    <template #footer>
      <p>Sou assim, professor</p>
    </template>
  </CardFull>

  <CardFull>
    Função: programador
    <template #header> 
      <h1>Zé da Silva</h1>
    </template>
  </CardFull>

  <Card>
    <h2>Eduardo</h2>
  </Card>

  <Card>
    <h2>Zé da Silva</h2>
    <p>Comedor de papel</p>
  </Card>
  <Card></Card>

  <hr />
  <h1>Props</h1>
  <!-- <ExpandBox title="Caixa 1" content="conteúdo 21" qtde="200000"/>
  <ExpandBox title="Caixa 2" content="conteúdo 12" qtde="35"/> -->

  <input type="text" v-model="titulo">
  <button @click="qtde++">+</button>
  
  <ExpandBox v-for="caixa in caixas" :key="caixa.id" v-bind="caixa" />

</template>

<style scoped>

</style>
