<script setup>
  import css from "./Table.module.css"
</script>

<template>
  <div :class="css.table__section">
    <div :class="css.table__item">
      <div :class="css.table__content">
        <div><slot></slot></div>
      </div>
    </div>
  </div>
</template>
