<template>
  <v-app>
    <v-toolbar app fixed>
      <v-toolbar-title>FOOD FOLKS</v-toolbar-title>
      <div class="flex-grow-1"></div>
      <v-toolbar-items>
        <v-btn text>Log in</v-btn>
        <v-btn text>Sign in</v-btn>
      </v-toolbar-items>
    </v-toolbar>
    <Home />
  </v-app>
</template>

<script>
import Home from './views/Home';

export default {
  name: 'App',
  components: {
    Home,
  },
  data: () => ({  
    //
  }),
};
</script>
