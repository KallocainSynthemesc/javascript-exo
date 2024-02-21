<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Objects exercise - Écrivez un chat virtuel</div>
    <div class="content">
      <MonacoEditor
        code="const cat = {
  fatigue: 0,
  //ajouter les propri&eacute;t&eacute;s manquantes
  
  jouer: function() {
    this.fatigue += 5;
    //ajouter des champs qui pourraient changer lorsque vous jouez avec un chat
  },
  
  dormir: function() {
    this.fatigue -= 5;
  },
  //ajouter les methods manquantes
  
  state: function(){
    //imprimer l'&eacute;tat complet du chat ici
    console.log(this.fatigue)
  }
}

cat.jouer();
cat.state();"
        editorIndex="31"
      />
    </div>
  </div>
</template>

<style scoped></style>
