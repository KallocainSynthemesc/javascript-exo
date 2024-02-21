<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Loop + function exercise - Caesar's cipher</div>
    <div class="content">
      <MonacoEditor
        code='let number1 = 5;
let number2 = 20;
//&eacute;crire la fonction ici
let result; //affecter le r&eacute;sultat de la fonction &agrave; la variable result.
console.log("Le minimum de ces deux nombres est: " + result);'
        editorIndex="26"
      />
    </div>
  </div>
</template>

<style scoped></style>
