<template>
  <v-card>
    <v-tabs v-model="tab" bg-color="secondary">
      <v-tab value="one">Content 1</v-tab>
      <v-tab value="two">Content 1</v-tab>
      <v-tab value="three">Content 1</v-tab>
    </v-tabs>

    <v-card-text>
      <v-window v-model="tab">
        <v-window-item value="one">
          <v-card subtitle="This is a subtitle" text="This is content" title="Title Content 1"></v-card>
        </v-window-item>

        <v-window-item value="two">
          <v-card>
            <template v-slot:title>
              Title Content 2
            </template>

            <template v-slot:subtitle>
              This is a subtitle
            </template>

            <template v-slot:text>
              This is content
            </template>
          </v-card>
        </v-window-item>

        <v-window-item value="three">
          <v-card>
            <v-card-item>
              <v-card-title>Title Content 3</v-card-title>

              <v-card-subtitle>This is a subtitle</v-card-subtitle>
            </v-card-item>

            <v-card-text>
              This is content
            </v-card-text>
          </v-card>
        </v-window-item>
      </v-window>
    </v-card-text>
  </v-card>

  <div class="text-center mt-6 d-flex ga-5 justify-center">
    <v-progress-circular :model-value="value" :rotate="360" :size="100" :width="15" color="teal">
      {{ value }}
    </v-progress-circular>

    <v-progress-circular :model-value="value" :rotate="360" :size="100" :width="15" color="primary">
      {{ value }}
    </v-progress-circular>

    <v-progress-circular :model-value="value" :rotate="360" :size="100" :width="15" color="red">
      {{ value }}
    </v-progress-circular>

    <v-progress-circular :model-value="value" :rotate="360" :size="100" :width="15" color="pink">
      {{ value }}
    </v-progress-circular>
  </div>

</template>

<script>
export default {
  data: () => ({
    tab: null,
    interval: {},
    value: 0,
  }),
  beforeUnmount() {
    clearInterval(this.interval)
  },
  mounted() {
    this.interval = setInterval(() => {
      if (this.value === 100) {
        return (this.value = 0)
      }
      this.value += 10
    }, 1000)
  },
}
</script>