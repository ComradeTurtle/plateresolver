<script setup>
defineProps({
  pref: Object,
})
</script>

<template>
  <StructuresFlex v-if="pref?.matches !== 'unknown'" row justify="evenly" class="bg-neutral-800 border-2 rounded border-gray-400 p-4 gap-1">
    <h1>Το πρόθεμα <span class="font-bold">{{ pref?.pref }}</span> αντιστοιχεί {{ pref?.matches.includes(',') ? 'στις περιοχές' : 'στην περιοχή' }}: <span class="font-bold">{{pref?.matches}}</span></h1>
  </StructuresFlex>

  <StructuresFlex v-else row justify="around" class="bg-red-900 border-2 rounded border-red-400 p-4">
    <h1>Το πρόθεμα {{ pref?.pref }} δεν έχει αντιστοιχία</h1>
  </StructuresFlex>
</template>
