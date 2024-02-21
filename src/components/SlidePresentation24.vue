<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Function - le plus grand de deux nombres</div>
    <div class="content">
      <p>
        Écrivez une fonction min qui prend deux arguments et renvoie le plus
        grand.
      </p>
      <MonacoEditor
        code='let number1 = 5;
let number2 = 20;
//&eacute;crire la fonction ici
let result; //affecter le r&eacute;sultat de la fonction &agrave; la variable result.
console.log("Le minimum de ces deux nombres est: " + result);'
        editorIndex="18"
      />
    </div>
  </div>
</template>
