<template>
  <div class="d-flex ga-5">
    <v-card title="Tem" class="text-center pa-3" width="500">
      {{tmp}}
    </v-card>
    <v-card title="Cel" class="text-center pa-3" width="500">
      {{ cel }}
    </v-card>
    <v-card title="Cap" class="text-center pa-3" width="500">
      {{ cap }}
    </v-card>
  </div>

</template>

<script setup>
defineProps({
  tmp: String,
  cel: String,
  cap: String
})
</script>