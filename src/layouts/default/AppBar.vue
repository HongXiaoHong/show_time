<template>
  <v-app-bar flat>
    <v-app-bar-title>
      <v-avatar class="me-10 ms-4" color="red" size="32">鸿</v-avatar>

      <v-btn v-for="link in links" :key="link" variant="text">
        {{ link }}
      </v-btn>
    </v-app-bar-title>
  </v-app-bar>
</template>

<script lang="ts" setup>
  //
  const links = ['projects', 'me']
</script>
