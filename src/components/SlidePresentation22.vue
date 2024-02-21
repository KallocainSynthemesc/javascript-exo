<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Function - negatif ou zero</div>
    <div class="content">
      <p>Vérifier si un nombre est positif, négatif ou zéro</p>
      <MonacoEditor code='isNaN("123ABC");' editorIndex="16" />
    </div>
  </div>
</template>

<style scoped></style>
