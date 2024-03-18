<template>
  <v-card class="mx-auto rounded-0">
    <v-layout>
      
      <v-app-bar color="" density="compact">
        
        <!-- <template v-slot:prepend>
          <v-app-bar-nav-icon></v-app-bar-nav-icon>
        </template> -->

        <v-app-bar-title>Dashboard</v-app-bar-title>
        <div class=" d-flex ga-5 mr-5">
          <v-btn to="/">Home</v-btn>
          <v-btn to="/about">About</v-btn>
          
        </div>

        <template v-slot:append>
          <v-btn icon="mdi-theme-light-dark" @click="toggleTheme"></v-btn>
        </template>
      </v-app-bar>

      <v-main>

      </v-main>
    </v-layout>
  </v-card>
</template>

<script>
import { useTheme } from 'vuetify';
export default {
  setup() {
    const theme = useTheme();

    return {
      theme,
      toggleTheme: () => {
        const themeValue = theme.global.current.value.dark ? 'light' : 'dark';
        theme.global.name.value = themeValue;
      },
    };
  },
}

</script>