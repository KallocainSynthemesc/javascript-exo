<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Date - 1er janvier</div>
    <div class="content">
      <p>
        Écrivez un programme JavaScript pour trouver si le 1er janvier est un
        dimanche entre 2014 et 2050. Indice : Vous pouvez appeler getDay() sur
        un objet Date et il vous donnera le jour représenté sous forme de
        nombre. <b>Le dimanche est le numéro 0</b>.
      </p>
      <MonacoEditor
        code="for (let year = 2014; year &lt;= 2050; year++)
{
  
}"
        editorIndex="34"
      />
    </div>
  </div>
</template>

<style scoped></style>
