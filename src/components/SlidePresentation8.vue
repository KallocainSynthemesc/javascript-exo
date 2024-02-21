<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">
      If exercices - multiplication et la somme de deux nombres
    </div>
    <div class="content">
      <p>
        Étant donné deux nombres entiers, affiche leur produit seulement si le
        produit est égal ou inférieur à 1000, sinon affiche leur somme.
      </p>
      <MonacoEditor
        code="let num1 = 20;
let num2= 30;
"
        editorIndex="4"
      />
    </div>
  </div>
</template>

<style scoped></style>
