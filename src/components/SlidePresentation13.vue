<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Loop exercise</div>
    <div class="content">
      <p>
        J'aimerais boucler le tableau en arrière, mais quelque chose ne va pas.
        <b>Je ne vois pas l'erreur, pouvez-vous la résoudre ?</b>
      </p>
      <MonacoEditor
        code='let array = ["Paris", "Toulouse", "Lyon", "Moissac", "Montauban", "Albi", "Figeac", "Caussade", "M&uuml;nchen", "Stuttgart", "N&uuml;rnberg"];

for(let i = array.length; i &gt;= 0; i++){
  console.log(array[i]);
}
'
        editorIndex="8"
      />
    </div>
  </div>
</template>

<style scoped></style>
