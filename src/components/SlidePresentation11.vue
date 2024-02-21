<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Loop exercise</div>
    <div class="content">
      <p>
        Réécrire le programme: Un développeur débutant a écrit ce morceau de
        code sans connaître les boucles ( Loops). Pouvez-vous simplifier ce code
        ?
      </p>
      <MonacoEditor
        code='let array = ["Paris", "Toulouse", "Lyon", "Moissac", "Montauban", "Albi", "Figeac", "Caussade", "M&uuml;nchen", "Stuttgart", "N&uuml;rnberg"];
let text = array[0] + ", ";
text += array[1] + ", ";
text += array[2] + ", ";
text += array[3] + ", ";
text += array[4] + ", ";
text += array[5] + ", ";
text += array[6] + ", ";
text += array[7] + ", ";
text += array[8] + ", ";
text += array[9] + ", ";
text += array[10] + ", ";
//r&eacute;p&eacute;ter la m&ecirc;me chose encore et encore est ennuyeux. N&apos;y a-t-il pas un moyen plus simple ?

console.log(text);'
        editorIndex="6"
      />
    </div>
  </div>
</template>

<style scoped></style>
