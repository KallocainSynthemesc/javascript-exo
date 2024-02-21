<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">String - Forme abrégée</div>
    <div class="content">
      <p>
        Écrivez une fonction JavaScript pour convertir une chaîne de caractères
        en forme abrégée. Exemple: Kilian Schropp devient Kilian S. Astuce :
        utiliser split() et charAt()
      </p>
      <MonacoEditor code="" editorIndex="33" />
    </div>
  </div>
</template>

<style scoped></style>
