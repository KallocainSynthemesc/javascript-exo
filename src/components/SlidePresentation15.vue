<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Loop exercise</div>
    <div class="content">
      <p>
        Je veux faire une boucle dans mon tableau et m'arrêter au milieu. Ma
        solution fonctionne, mais elle est plus compliquée qu'elle ne devrait
        l'être. <b>Pouvez-vous la rendre plus simple ?</b>
      </p>
      <MonacoEditor
        code='let array = ["Paris", "Toulouse", "Lyon", "Moissac", "Montauban", "Albi", "Figeac", "Caussade", "M&uuml;nchen", "Stuttgart", "N&uuml;rnberg"];

let i = 0;
while(i &lt; array.length)
{
  if(i &lt;= array.length/2) //peut-&ecirc;tre d&eacute;placer le contr&ocirc;le if quelque part ?
  {
    console.log(array[i]);
    i++;
  }
  else{
    i++;
  }
}
'
        editorIndex="10"
      />
    </div>
  </div>
</template>

<style scoped></style>
