<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">If exercices - isNan</div>
    <div class="content">
      <p>Vérifier si une variable est un nombre ou non</p>
      <p>
        Utiliser la fonction javascript intégrée
        <a
          href="https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/isNaN"
          >isNan().</a
        >
      </p>
      <MonacoEditor code='console.log(isNaN("123ABC"));' editorIndex="0" />
    </div>
  </div>
</template>

<style scoped></style>
