<script setup>
  import css from "./App.module.css";
  import {ref} from "vue";

  const text = ref("");
  const cards = ref(["card1", "card2", "card3", "card4"]);
</script>

<template>
  <input type="text" v-model="text">
  <template v-for="(card, index) in cards" :key="index">
    <div v-if="text === 'Все'">{{card}}, {{index}}</div>
    <div v-else-if="text === 'Чётные' && (index % 2) === 0">{{card}}, {{index}}</div>
    <div v-else-if="text === 'Нечётные' && (index % 2) !== 0">{{card}}, {{index}}</div>
  </template>
</template>


