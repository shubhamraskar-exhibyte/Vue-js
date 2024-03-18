<template>
  <NuxtLayout>
    <v-app>
      <v-main>
        <AppBar />
        <v-container class="min-h-screen">
          <RouterView />
        </v-container>
      </v-main>
    </v-app>
  </NuxtLayout>
</template>

<script setup></script>