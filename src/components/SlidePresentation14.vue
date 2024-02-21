<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Loop exercise</div>
    <div class="content">
      <p>
        Je ne comprends pas les boucles for... J'ai essayé la boucle while mais
        mon programme n'affiche aucune de mes villes.
        <b>Pouvez-vous le réparer ?</b>
      </p>
      <MonacoEditor
        code='let array = ["Paris", "Toulouse", "Lyon", "Moissac", "Montauban", "Albi", "Figeac", "Caussade", "M&uuml;nchen", "Stuttgart", "N&uuml;rnberg"];

let i = 0;
while(i &lt; array.length)
{
	console.log(array[i])
	i++;
}
'
        editorIndex="9"
      />
    </div>
  </div>
</template>

<style scoped></style>
