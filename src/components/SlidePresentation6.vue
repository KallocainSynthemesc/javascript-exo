<script setup>
import MonacoEditor from "@/components/interactive/MonacoEditor.vue";
</script>
<template>
  <div class="slide">
    <div class="heading">
      If exercices - Vérifier si une année est bissextile ou non
    </div>
    <div class="content">
      <p>
        trouver si l'année donnée est une année bissextile ou non en utilisant
        les opérateurs %, !=, && et ||.
      </p>
      <ul>
        <li>
          Si l'année est divisible par 4 et non divisible par 100, alors
          l'impression "année bissextile".
        </li>
        <li>
          Ou si l'année est divisible par 400, alors on imprime "année
          bissextile".
        </li>
        <li>Sinon afficher "pas une année bissextile".</li>
      </ul>
      <MonacoEditor code="let year = 2000;" editorIndex="3" />
    </div>
  </div>
</template>

<style scoped></style>
