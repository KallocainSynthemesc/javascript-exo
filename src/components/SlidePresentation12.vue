<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Loop exercise</div>
    <div class="content">
      <p>
        J'ai essayé d'implémenter une boucle for de l'exercice précédent. Pour
        une raison quelconque, la dernière valeur affichée sur la console est
        undefined. <b>Pouvez-vous me dire pourquoi et le corriger?</b>
      </p>
      <MonacoEditor
        code='let array = ["Paris", "Toulouse", "Lyon", "Moissac", "Montauban", "Albi", "Figeac", "Caussade", "M&uuml;nchen", "Stuttgart", "N&uuml;rnberg"];

for(let i = 0; i &lt;= array.length; i++){
  console.log(array[i]);
}
'
        editorIndex="7"
      />
    </div>
  </div>
</template>

<style scoped></style>
