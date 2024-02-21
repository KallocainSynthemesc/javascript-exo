<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">
      If exercices - premier et le dernier numéro d'une liste
    </div>
    <div class="content">
      <p>
        Ecrivez une fonction qui renvoie True si le premier et le dernier numéro
        d'une liste donnée sont identiques. Si les numéros sont différents, elle
        renvoie False.
      </p>
      <MonacoEditor
        code="let numbers_x = [10, 20, 30, 40, 10]
let numbers_y = [75, 65, 35, 75, 30]"
        editorIndex="5"
      />
    </div>
  </div>
</template>

<style scoped></style>
