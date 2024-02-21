<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">If exercices - le plus grand de troi nombres</div>
    <div class="content">
      <p>
        Trouver le plus grand de troi nombres en utilisant l'opérateur "&lt;" et
        "&&" en JavaScript
      </p>
      <MonacoEditor
        code="let num1 = 3;
let num2 = 5;
let num3 = 4;"
        editorIndex="1"
      />
    </div>
  </div>
</template>

<style scoped></style>
