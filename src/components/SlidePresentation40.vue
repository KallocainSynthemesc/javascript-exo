<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Objects exercise - Suppression</div>
    <div class="content">
      <p>
        Écrivez un programme JavaScript pour supprimer la propriété rollno de
        l'objet suivant. Imprimez également l'objet avant et après la
        suppression de la propriété.
      </p>
      <MonacoEditor
        code='var prof =  { 
  name : "Kilian", 
  sclass : "Concepteur", 
  rollno : 12  
};
'
        editorIndex="30"
      />
    </div>
  </div>
</template>
