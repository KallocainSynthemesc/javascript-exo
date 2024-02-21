<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">If exercices - Présent dans un périmètre donné?</div>
    <div class="content">
      <MonacoEditor
        code="let num = 6;
let start = 5;
let end = 8;"
        editorIndex="2"
      />
    </div>
  </div>
</template>

<style scoped></style>
