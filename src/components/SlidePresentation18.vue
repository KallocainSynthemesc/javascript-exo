<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Loop exercise - Trouver le plus grand nombre</div>
    <div class="content">
      <p>
        Écrire un code pour trouver le plus grand nombre dans un tableau (liste)
        en utilisant des boucles.
      </p>
      <MonacoEditor
        code="var arr = [2, 45, 3, 67, 34, 567, 34, 345, 123];"
        editorIndex="12"
      />
    </div>
  </div>
</template>

<style scoped></style>
