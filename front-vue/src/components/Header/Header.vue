<script setup>
import {computed, inject} from "vue";
import css from "./Header.module.css"
</script>

<template>
  <div :class="css.header">
    <div :class="css.header__content">
      <p><slot></slot></p>
    </div>
  </div>
</template>
