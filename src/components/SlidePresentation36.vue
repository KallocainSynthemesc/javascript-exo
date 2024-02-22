<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">
      Loop + function - Un nombre entier dans l'ordre inverse.
    </div>
    <div class="content">
      <p>
        par exemple, si l'int donné est 7536, la sortie sera 6357. Indice : Nous
        avons besoin d'au moins les opérateurs %, *, // et +. Si vous voulez
        tricher, nous avons aussi la fonction
        <a
          href="https://developer.mozilla.org/fr/docs/Web/JavaScript/Reference/Global_Objects/Math/floor"
          >Math.floor(x/y).</a
        >
      </p>
      <MonacoEditor code="" editorIndex="27" />
    </div>
  </div>
</template>

<style scoped></style>
