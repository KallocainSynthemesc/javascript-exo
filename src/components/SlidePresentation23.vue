<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Function - pair ou impair</div>
    <div class="content">
      <p>
        Écrivez une fonction qui dit, à partir d'une entrée, si un nombre est
        pair ou non. Conseil : utilisez l'opérateur %.
      </p>
      <MonacoEditor
        code="let variable = 3

function even(x) {
  //mettre la logic ici
}

console.log(even(variable))"
        editorIndex="17"
      />
    </div>
  </div>
</template>

<style scoped></style>
