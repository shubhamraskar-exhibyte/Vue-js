<template class="">
  <v-carousel hide-delimiters class="mb-6">
    <v-carousel-item src="https://cdn.vuetifyjs.com/images/cards/docks.jpg" cover></v-carousel-item>

    <v-carousel-item src="https://cdn.vuetifyjs.com/images/cards/hotel.jpg" cover></v-carousel-item>

    <v-carousel-item src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg" cover></v-carousel-item>
  </v-carousel>

  
  <Card tmp="25" cel="21" cap="1tn"></Card>

  <v-otp-input length="7"></v-otp-input>

</template>

<script>
data: () => ({
  rules: [
    value => !!value || 'Required.',
    value => (value && value.length >= 3) || 'Min 3 characters',
  ],

})
</script>