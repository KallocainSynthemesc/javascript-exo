<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">
      Loop exercise - Min/Max du quatre des cinq entiers
    </div>
    <div class="content">
      <p>
        Étant donné cinq entiers positifs, trouvez les valeurs minimale et
        maximale qui peuvent être calculées en additionnant exactement quatre
        des cinq entiers. Entrée : [1,2,3,4,5]
      </p>
      <MonacoEditor
        code="let arr = [1,2,3,4,5]
let lowestSum = 0
let highestSum = 0"
        editorIndex="14"
      />
    </div>
  </div>
</template>

<style scoped></style>
