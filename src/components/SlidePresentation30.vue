<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">Loop + function exercise - FizzBuzz</div>
    <div class="content">
      <p>
        Écrivez un programme JavaScript qui itère les entiers de 1 à 100. Mais
        pour les multiples de trois, imprimez "Fizz" à la place du nombre et
        pour les multiples de cinq, imprimez "Buzz". Pour les nombres qui sont
        des multiples de trois et de cinq, imprimez "FizzBuzz".
      </p>
      <MonacoEditor code="" editorIndex="24" />
    </div>
  </div>
</template>

<style scoped></style>
