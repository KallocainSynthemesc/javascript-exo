<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Loop exercise - Somme des éléments</div>
    <div class="content">
      <p>
        Étant donné un tableau d'entiers, trouvez la somme de ses éléments.
        entrée : [1, 2, 3, 4, 10, 11]; sortie: 31
      </p>
      <MonacoEditor
        code=" let arr = [1, 2, 3, 4, 10, 11];
 let sum = arr[0]"
        editorIndex="13"
      />
    </div>
  </div>
</template>

<style scoped></style>
